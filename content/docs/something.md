# Certified
## nmap
```
PORT      STATE    SERVICE       REASON      VERSION
53/tcp    open     domain        syn-ack     Simple DNS Plus
88/tcp    open     kerberos-sec  syn-ack     Microsoft Windows Kerberos (server time: 2024-11-03 08:58:57Z)
135/tcp   open     msrpc         syn-ack     Microsoft Windows RPC
139/tcp   open     netbios-ssn   syn-ack     Microsoft Windows netbios-ssn
389/tcp   open     ldap          syn-ack     Microsoft Windows Active Directory LDAP (Domain: certified.htb0., Site: Default-First-Site-Name)
| ssl-cert: Subject: commonName=DC01.certified.htb
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:DC01.certified.htb
| Issuer: commonName=certified-DC01-CA/domainComponent=certified
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2024-05-13T15:49:36
| Not valid after:  2025-05-13T15:49:36
| MD5:   4e1f97f07c0ad0ec52e15f63ec55f3bc
| SHA-1: 28e24c68aa00dd8bee91564b33fea345116b3828
| -----BEGIN CERTIFICATE-----
| MIIGPzCCBSegAwIBAgITeQAAAAIvfMdjJV9GkQAAAAAAAjANBgkqhkiG9w0BAQsF
| ADBMMRMwEQYKCZImiZPyLGQBGRYDaHRiMRkwFwYKCZImiZPyLGQBGRYJY2VydGlm
| aWVkMRowGAYDVQQDExFjZXJ0aWZpZWQtREMwMS1DQTAeFw0yNDA1MTMxNTQ5MzZa
| Fw0yNTA1MTMxNTQ5MzZaMB0xGzAZBgNVBAMTEkRDMDEuY2VydGlmaWVkLmh0YjCC
| ASIwDQYJKoZIhvcNAQEBBQADggEPADCCAQoCggEBAMx/FhgH36heOUjpNhO4JWYX
| E0zDwpKfx3dfqvEqTvIfRLpptNUCfkaeZijP+YAlUMNSNUvgFLZ7yuZf3ubIcEv8
| wXMlABwpVxe3NtOzLXQhNypU/W53DgYZoD9ueC3ob6f4jI6dN6jKt4gV/pBmoX3i
| Ky0XmrIaMkO8W20gzJtf8RaZYChHzhilGs3TwkKmBkZFt4+KeTkCbBE4T8zka8l6
| 52hfOhdz5YOU82eviJuTQqaprVtognmW6EV2C7laO+UvQy2VwZc9L+6A42t5Pz2E
| e+28xaBIGAgNn5TMcS+oJC0qhnAFNazT2X4p0aq3WBlF5BMwadrEwk59t4VcRc0C
| AwEAAaOCA0cwggNDMC8GCSsGAQQBgjcUAgQiHiAARABvAG0AYQBpAG4AQwBvAG4A
| dAByAG8AbABsAGUAcjAdBgNVHSUEFjAUBggrBgEFBQcDAgYIKwYBBQUHAwEwDgYD
| VR0PAQH/BAQDAgWgMHgGCSqGSIb3DQEJDwRrMGkwDgYIKoZIhvcNAwICAgCAMA4G
| CCqGSIb3DQMEAgIAgDALBglghkgBZQMEASowCwYJYIZIAWUDBAEtMAsGCWCGSAFl
| AwQBAjALBglghkgBZQMEAQUwBwYFKw4DAgcwCgYIKoZIhvcNAwcwHQYDVR0OBBYE
| FPTg6Uo2pYQv7jJTC9x7Reo9CbVVMB8GA1UdIwQYMBaAFOz7EkAVob3H0S47Lk1L
| csBi3yv1MIHOBgNVHR8EgcYwgcMwgcCggb2ggbqGgbdsZGFwOi8vL0NOPWNlcnRp
| ZmllZC1EQzAxLUNBLENOPURDMDEsQ049Q0RQLENOPVB1YmxpYyUyMEtleSUyMFNl
| cnZpY2VzLENOPVNlcnZpY2VzLENOPUNvbmZpZ3VyYXRpb24sREM9Y2VydGlmaWVk
| LERDPWh0Yj9jZXJ0aWZpY2F0ZVJldm9jYXRpb25MaXN0P2Jhc2U/b2JqZWN0Q2xh
| c3M9Y1JMRGlzdHJpYnV0aW9uUG9pbnQwgcUGCCsGAQUFBwEBBIG4MIG1MIGyBggr
| BgEFBQcwAoaBpWxkYXA6Ly8vQ049Y2VydGlmaWVkLURDMDEtQ0EsQ049QUlBLENO
| PVB1YmxpYyUyMEtleSUyMFNlcnZpY2VzLENOPVNlcnZpY2VzLENOPUNvbmZpZ3Vy
| YXRpb24sREM9Y2VydGlmaWVkLERDPWh0Yj9jQUNlcnRpZmljYXRlP2Jhc2U/b2Jq
| ZWN0Q2xhc3M9Y2VydGlmaWNhdGlvbkF1dGhvcml0eTA+BgNVHREENzA1oB8GCSsG
| AQQBgjcZAaASBBBTwp5mQoxFT6ExYzeAVBiughJEQzAxLmNlcnRpZmllZC5odGIw
| TgYJKwYBBAGCNxkCBEEwP6A9BgorBgEEAYI3GQIBoC8ELVMtMS01LTIxLTcyOTc0
| Njc3OC0yNjc1OTc4MDkxLTM4MjAzODgyNDQtMTAwMDANBgkqhkiG9w0BAQsFAAOC
| AQEAk4PE1BZ/qAgrUyzYM5plxxgUpGbICaWEkDkyiu7uCaTOehQ4rITZE1xefpHW
| VVEULz9UqlozCQgaKy3BRQsUjMZgkcQt0D+5Ygnri/+M3adcYWpJHsk+gby/JShv
| ztRj1wS/X6SEErDaf9Nw0jgZi3QCaNqH2agxwj+oA+mCMd5mBq7JtWcCI3wQ3xuE
| aOEd9Q86T/J4ZdGC+8iQKt3GrvHzTEDijK9zWxm8nuftG/AyBU0N23xJCLgWZkQU
| fgVn+2b7pjWIPAWdZv8WqcJV1tinG0oM83wgbg3Nv3ZeoEwDCs5MgYprXNImNGtI
| zQY41iYatWCKZW54Ylno2wj9tg==
|_-----END CERTIFICATE-----
|_ssl-date: 2024-11-03T09:00:26+00:00; +6h47m23s from scanner time.
445/tcp   open     microsoft-ds? syn-ack
464/tcp   open     kpasswd5?     syn-ack
593/tcp   open     ncacn_http    syn-ack     Microsoft Windows RPC over HTTP 1.0
636/tcp   filtered ldapssl       no-response
9389/tcp  filtered adws          no-response
49666/tcp open     msrpc         syn-ack     Microsoft Windows RPC
49667/tcp open     msrpc         syn-ack     Microsoft Windows RPC
49677/tcp filtered unknown       no-response
49678/tcp filtered unknown       no-response
49681/tcp filtered unknown       no-response
49708/tcp filtered unknown       no-response
49731/tcp filtered unknown       no-response
Service Info: Host: DC01; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 50458/tcp): CLEAN (Timeout)
|   Check 2 (port 25261/tcp): CLEAN (Timeout)
|   Check 3 (port 41863/udp): CLEAN (Timeout)
|   Check 4 (port 12583/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
|_clock-skew: mean: 6h47m22s, deviation: 0s, median: 6h47m22s
| smb2-security-mode: 
|   311: 
|_    Message signing enabled and required
| smb2-time: 
|   date: 2024-11-03T08:59:49
|_  start_date: N/A

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 22:13
Completed NSE at 22:13, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 22:13
Completed NSE at 22:13, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 22:13
Completed NSE at 22:13, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 114.01 seconds
```
### kerbrute
```./kerbrute_linux_amd64 userenum --dc 10.10.11.41 -d certified.htb  /usr/share/seclists/Usernames/xato-net-10-million-usernames.txt```

nothing interesting
![image](https://github.com/user-attachments/assets/e23a5c8f-455b-4170-b5aa-e07810f903db)
oh crap
### smb
```
nxc smb 10.10.11.41 -u judith.mader -p judith09 --rid-brute
SMB         10.10.11.41     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:certified.htb) (signing:True) (SMBv1:False)
SMB         10.10.11.41     445    DC01             [+] certified.htb\judith.mader:judith09 
SMB         10.10.11.41     445    DC01             498: CERTIFIED\Enterprise Read-only Domain Controllers (SidTypeGroup)                                                                                                               
SMB         10.10.11.41     445    DC01             500: CERTIFIED\Administrator (SidTypeUser)
SMB         10.10.11.41     445    DC01             501: CERTIFIED\Guest (SidTypeUser)
SMB         10.10.11.41     445    DC01             502: CERTIFIED\krbtgt (SidTypeUser)
SMB         10.10.11.41     445    DC01             512: CERTIFIED\Domain Admins (SidTypeGroup)
SMB         10.10.11.41     445    DC01             513: CERTIFIED\Domain Users (SidTypeGroup)
SMB         10.10.11.41     445    DC01             514: CERTIFIED\Domain Guests (SidTypeGroup)
SMB         10.10.11.41     445    DC01             515: CERTIFIED\Domain Computers (SidTypeGroup)
SMB         10.10.11.41     445    DC01             516: CERTIFIED\Domain Controllers (SidTypeGroup)
SMB         10.10.11.41     445    DC01             517: CERTIFIED\Cert Publishers (SidTypeAlias)
SMB         10.10.11.41     445    DC01             518: CERTIFIED\Schema Admins (SidTypeGroup)
SMB         10.10.11.41     445    DC01             519: CERTIFIED\Enterprise Admins (SidTypeGroup)
SMB         10.10.11.41     445    DC01             520: CERTIFIED\Group Policy Creator Owners (SidTypeGroup)
SMB         10.10.11.41     445    DC01             521: CERTIFIED\Read-only Domain Controllers (SidTypeGroup)
SMB         10.10.11.41     445    DC01             522: CERTIFIED\Cloneable Domain Controllers (SidTypeGroup)
SMB         10.10.11.41     445    DC01             525: CERTIFIED\Protected Users (SidTypeGroup)
SMB         10.10.11.41     445    DC01             526: CERTIFIED\Key Admins (SidTypeGroup)
SMB         10.10.11.41     445    DC01             527: CERTIFIED\Enterprise Key Admins (SidTypeGroup)
SMB         10.10.11.41     445    DC01             553: CERTIFIED\RAS and IAS Servers (SidTypeAlias)
SMB         10.10.11.41     445    DC01             571: CERTIFIED\Allowed RODC Password Replication Group (SidTypeAlias)                                                                                                               
SMB         10.10.11.41     445    DC01             572: CERTIFIED\Denied RODC Password Replication Group (SidTypeAlias)                                                                                                                
SMB         10.10.11.41     445    DC01             1000: CERTIFIED\DC01$ (SidTypeUser)
SMB         10.10.11.41     445    DC01             1101: CERTIFIED\DnsAdmins (SidTypeAlias)
SMB         10.10.11.41     445    DC01             1102: CERTIFIED\DnsUpdateProxy (SidTypeGroup)
SMB         10.10.11.41     445    DC01             1103: CERTIFIED\judith.mader (SidTypeUser)
SMB         10.10.11.41     445    DC01             1104: CERTIFIED\Management (SidTypeGroup)
SMB         10.10.11.41     445    DC01             1105: CERTIFIED\management_svc (SidTypeUser)
SMB         10.10.11.41     445    DC01             1106: CERTIFIED\ca_operator (SidTypeUser)
SMB         10.10.11.41     445    DC01             1601: CERTIFIED\alexander.huges (SidTypeUser)
SMB         10.10.11.41     445    DC01             1602: CERTIFIED\harry.wilson (SidTypeUser)
SMB         10.10.11.41     445    DC01             1603: CERTIFIED\gregory.cameron (SidTypeUser)
```
## bloodhound
./bloodhound.py -ns "10.10.11.41" -d "certified.htb" -u "judith.mader" -p "judith09" -k

