# writeup office
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
| ssl-cert: Subject: commonName=DC.office.htb
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:DC.office.htb
| Issuer: commonName=office-DC-CA/domainComponent=office
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2023-05-10T12:36:58
| Not valid after:  2024-05-09T12:36:58
| MD5:   b83fab78db28734dde8411e9420f8878
| SHA-1: 36c4cedf91853d4c598c739a8bc7a0624458cfe4
| -----BEGIN CERTIFICATE-----
| MIIFyzCCBLOgAwIBAgITQAAAAAMdA83RpYN55AAAAAAAAzANBgkqhkiG9w0BAQsF
| ADBEMRMwEQYKCZImiZPyLGQBGRYDaHRiMRYwFAYKCZImiZPyLGQBGRYGb2ZmaWNl
| MRUwEwYDVQQDEwxvZmZpY2UtREMtQ0EwHhcNMjMwNTEwMTIzNjU4WhcNMjQwNTA5
| MTIzNjU4WjAYMRYwFAYDVQQDEw1EQy5vZmZpY2UuaHRiMIIBIjANBgkqhkiG9w0B
| AQEFAAOCAQ8AMIIBCgKCAQEA15Wa3dfyWK0+9iRvZ2H4VWeXwLq40Ee6jzcu8buW
| D/Hp4rubrQa5X2/iS3NdXMsxamygq4s7R5AJa9Ys3I7sm59ctlCo/vjVag0hbqhU
| 5qjBJ1GCQxdiaqRj3BqAO5Tbt9RUH9oeU/UQMzzUQqwKL/Z+twyh9aL6HDnbPXvM
| IeDewk5y/S6M8DlOc6ORZQfBg8NuroyiPYCNb1+WhednfBB0ahNFqzq2MTDLXMNM
| bLeX2zeO/+dgF1ohsQ9qhFyBtFSsaCMR33PMKNs7Iqji42+O5jVNCvUICelUroex
| 1VrC7ogW/JVSqHY4J+6mXZHJhn7xhu6rJKtFDHLeheheRQIDAQABo4IC4DCCAtww
| LwYJKwYBBAGCNxQCBCIeIABEAG8AbQBhAGkAbgBDAG8AbgB0AHIAbwBsAGwAZQBy
| MB0GA1UdJQQWMBQGCCsGAQUFBwMCBggrBgEFBQcDATAOBgNVHQ8BAf8EBAMCBaAw
| eAYJKoZIhvcNAQkPBGswaTAOBggqhkiG9w0DAgICAIAwDgYIKoZIhvcNAwQCAgCA
| MAsGCWCGSAFlAwQBKjALBglghkgBZQMEAS0wCwYJYIZIAWUDBAECMAsGCWCGSAFl
| AwQBBTAHBgUrDgMCBzAKBggqhkiG9w0DBzA5BgNVHREEMjAwoB8GCSsGAQQBgjcZ
| AaASBBA2idyIqAZET5Xm5iLN7Fc3gg1EQy5vZmZpY2UuaHRiMB0GA1UdDgQWBBRS
| FLVfJhlc3XkBccZHJjyKvpRS1TAfBgNVHSMEGDAWgBRgOpmCFktRJECTymSHaes3
| Vx3p9jCBxAYDVR0fBIG8MIG5MIG2oIGzoIGwhoGtbGRhcDovLy9DTj1vZmZpY2Ut
| REMtQ0EsQ049REMsQ049Q0RQLENOPVB1YmxpYyUyMEtleSUyMFNlcnZpY2VzLENO
| PVNlcnZpY2VzLENOPUNvbmZpZ3VyYXRpb24sREM9b2ZmaWNlLERDPWh0Yj9jZXJ0
| aWZpY2F0ZVJldm9jYXRpb25MaXN0P2Jhc2U/b2JqZWN0Q2xhc3M9Y1JMRGlzdHJp
| YnV0aW9uUG9pbnQwgb0GCCsGAQUFBwEBBIGwMIGtMIGqBggrBgEFBQcwAoaBnWxk
| YXA6Ly8vQ049b2ZmaWNlLURDLUNBLENOPUFJQSxDTj1QdWJsaWMlMjBLZXklMjBT
| ZXJ2aWNlcyxDTj1TZXJ2aWNlcyxDTj1Db25maWd1cmF0aW9uLERDPW9mZmljZSxE
| Qz1odGI/Y0FDZXJ0aWZpY2F0ZT9iYXNlP29iamVjdENsYXNzPWNlcnRpZmljYXRp
| b25BdXRob3JpdHkwDQYJKoZIhvcNAQELBQADggEBABw9WEKbYyfAE7PZ0Plb7lxB
| Ftvjpqh2Q9RkdSlxQNdWMfSsZozN6UNTG7mgJBB/T9vZpi8USJTGwf1EfygiDbm1
| yofBMvpqLAXg4ANvWXTDChYSumhlt7W+gJzTgWd4mgRp576acFojnNCqQRhYCD8r
| 6r/PIwlCDSwfLExxhQs7ZL3Jkqt/fP85ic3W9GuzwI9isPZmwsezP/korptA7utb
| sJHn2bydwf907VX2usW8yRmpuRZyvfsbYHYjJqFgohB5dh26ltEQz2vX6y4Mte4L
| 024aNx/gANh3F4gFXpGrAWdVxnHXc1QV9OVRHO+FAL30xdhosJ4D4HdRTDjCfqw=
|_-----END CERTIFICATE-----
|_ssl-date: TLS randomness does not represent time
443/tcp   open  ssl/http      syn-ack Apache httpd 2.4.56 (OpenSSL/1.1.1t PHP/8.0.28)
| ssl-cert: Subject: commonName=localhost
| Issuer: commonName=localhost
| Public Key type: rsa
| Public Key bits: 1024
| Signature Algorithm: sha1WithRSAEncryption
| Not valid before: 2009-11-10T23:48:47
| Not valid after:  2019-11-08T23:48:47
| MD5:   a0a44cc99e84b26f9e639f9ed229dee0
| SHA-1: b0238c547a905bfa119c4e8baccaeacf36491ff6
| -----BEGIN CERTIFICATE-----
| MIIBnzCCAQgCCQC1x1LJh4G1AzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDEwls
| b2NhbGhvc3QwHhcNMDkxMTEwMjM0ODQ3WhcNMTkxMTA4MjM0ODQ3WjAUMRIwEAYD
| VQQDEwlsb2NhbGhvc3QwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAMEl0yfj
| 7K0Ng2pt51+adRAj4pCdoGOVjx1BmljVnGOMW3OGkHnMw9ajibh1vB6UfHxu463o
| J1wLxgxq+Q8y/rPEehAjBCspKNSq+bMvZhD4p8HNYMRrKFfjZzv3ns1IItw46kgT
| gDpAl1cMRzVGPXFimu5TnWMOZ3ooyaQ0/xntAgMBAAEwDQYJKoZIhvcNAQEFBQAD
| gYEAavHzSWz5umhfb/MnBMa5DL2VNzS+9whmmpsDGEG+uR0kM1W2GQIdVHHJTyFd
| aHXzgVJBQcWTwhp84nvHSiQTDBSaT6cQNQpvag/TaED/SEQpm0VqDFwpfFYuufBL
| vVNbLkKxbK2XwUvu0RxoLdBMC/89HqrZ0ppiONuQ+X2MtxE=
|_-----END CERTIFICATE-----
|_ssl-date: TLS randomness does not represent time
|_http-server-header: Apache/2.4.56 (Win64) OpenSSL/1.1.1t PHP/8.0.28
|_http-title: 403 Forbidden
| tls-alpn: 
|_  http/1.1
445/tcp   open  microsoft-ds? syn-ack
464/tcp   open  kpasswd5?     syn-ack
593/tcp   open  ncacn_http    syn-ack Microsoft Windows RPC over HTTP 1.0
636/tcp   open  ssl/ldap      syn-ack Microsoft Windows Active Directory LDAP (Domain: office.htb0., Site: Default-First-Site-Name)
| ssl-cert: Subject: commonName=DC.office.htb
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:DC.office.htb
| Issuer: commonName=office-DC-CA/domainComponent=office
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2023-05-10T12:36:58
| Not valid after:  2024-05-09T12:36:58
| MD5:   b83fab78db28734dde8411e9420f8878
| SHA-1: 36c4cedf91853d4c598c739a8bc7a0624458cfe4
| -----BEGIN CERTIFICATE-----
| MIIFyzCCBLOgAwIBAgITQAAAAAMdA83RpYN55AAAAAAAAzANBgkqhkiG9w0BAQsF
| ADBEMRMwEQYKCZImiZPyLGQBGRYDaHRiMRYwFAYKCZImiZPyLGQBGRYGb2ZmaWNl
| MRUwEwYDVQQDEwxvZmZpY2UtREMtQ0EwHhcNMjMwNTEwMTIzNjU4WhcNMjQwNTA5
| MTIzNjU4WjAYMRYwFAYDVQQDEw1EQy5vZmZpY2UuaHRiMIIBIjANBgkqhkiG9w0B
| AQEFAAOCAQ8AMIIBCgKCAQEA15Wa3dfyWK0+9iRvZ2H4VWeXwLq40Ee6jzcu8buW
| D/Hp4rubrQa5X2/iS3NdXMsxamygq4s7R5AJa9Ys3I7sm59ctlCo/vjVag0hbqhU
| 5qjBJ1GCQxdiaqRj3BqAO5Tbt9RUH9oeU/UQMzzUQqwKL/Z+twyh9aL6HDnbPXvM
| IeDewk5y/S6M8DlOc6ORZQfBg8NuroyiPYCNb1+WhednfBB0ahNFqzq2MTDLXMNM
| bLeX2zeO/+dgF1ohsQ9qhFyBtFSsaCMR33PMKNs7Iqji42+O5jVNCvUICelUroex
| 1VrC7ogW/JVSqHY4J+6mXZHJhn7xhu6rJKtFDHLeheheRQIDAQABo4IC4DCCAtww
| LwYJKwYBBAGCNxQCBCIeIABEAG8AbQBhAGkAbgBDAG8AbgB0AHIAbwBsAGwAZQBy
| MB0GA1UdJQQWMBQGCCsGAQUFBwMCBggrBgEFBQcDATAOBgNVHQ8BAf8EBAMCBaAw
| eAYJKoZIhvcNAQkPBGswaTAOBggqhkiG9w0DAgICAIAwDgYIKoZIhvcNAwQCAgCA
| MAsGCWCGSAFlAwQBKjALBglghkgBZQMEAS0wCwYJYIZIAWUDBAECMAsGCWCGSAFl
| AwQBBTAHBgUrDgMCBzAKBggqhkiG9w0DBzA5BgNVHREEMjAwoB8GCSsGAQQBgjcZ
| AaASBBA2idyIqAZET5Xm5iLN7Fc3gg1EQy5vZmZpY2UuaHRiMB0GA1UdDgQWBBRS
| FLVfJhlc3XkBccZHJjyKvpRS1TAfBgNVHSMEGDAWgBRgOpmCFktRJECTymSHaes3
| Vx3p9jCBxAYDVR0fBIG8MIG5MIG2oIGzoIGwhoGtbGRhcDovLy9DTj1vZmZpY2Ut
| REMtQ0EsQ049REMsQ049Q0RQLENOPVB1YmxpYyUyMEtleSUyMFNlcnZpY2VzLENO
| PVNlcnZpY2VzLENOPUNvbmZpZ3VyYXRpb24sREM9b2ZmaWNlLERDPWh0Yj9jZXJ0
| aWZpY2F0ZVJldm9jYXRpb25MaXN0P2Jhc2U/b2JqZWN0Q2xhc3M9Y1JMRGlzdHJp
| YnV0aW9uUG9pbnQwgb0GCCsGAQUFBwEBBIGwMIGtMIGqBggrBgEFBQcwAoaBnWxk
| YXA6Ly8vQ049b2ZmaWNlLURDLUNBLENOPUFJQSxDTj1QdWJsaWMlMjBLZXklMjBT
| ZXJ2aWNlcyxDTj1TZXJ2aWNlcyxDTj1Db25maWd1cmF0aW9uLERDPW9mZmljZSxE
| Qz1odGI/Y0FDZXJ0aWZpY2F0ZT9iYXNlP29iamVjdENsYXNzPWNlcnRpZmljYXRp
| b25BdXRob3JpdHkwDQYJKoZIhvcNAQELBQADggEBABw9WEKbYyfAE7PZ0Plb7lxB
| Ftvjpqh2Q9RkdSlxQNdWMfSsZozN6UNTG7mgJBB/T9vZpi8USJTGwf1EfygiDbm1
| yofBMvpqLAXg4ANvWXTDChYSumhlt7W+gJzTgWd4mgRp576acFojnNCqQRhYCD8r
| 6r/PIwlCDSwfLExxhQs7ZL3Jkqt/fP85ic3W9GuzwI9isPZmwsezP/korptA7utb
| sJHn2bydwf907VX2usW8yRmpuRZyvfsbYHYjJqFgohB5dh26ltEQz2vX6y4Mte4L
| 024aNx/gANh3F4gFXpGrAWdVxnHXc1QV9OVRHO+FAL30xdhosJ4D4HdRTDjCfqw=
|_-----END CERTIFICATE-----
|_ssl-date: TLS randomness does not represent time
3268/tcp  open  ldap          syn-ack Microsoft Windows Active Directory LDAP (Domain: office.htb0., Site: Default-First-Site-Name)
| ssl-cert: Subject: commonName=DC.office.htb
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:DC.office.htb
| Issuer: commonName=office-DC-CA/domainComponent=office
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2023-05-10T12:36:58
| Not valid after:  2024-05-09T12:36:58
| MD5:   b83fab78db28734dde8411e9420f8878
| SHA-1: 36c4cedf91853d4c598c739a8bc7a0624458cfe4
| -----BEGIN CERTIFICATE-----
| MIIFyzCCBLOgAwIBAgITQAAAAAMdA83RpYN55AAAAAAAAzANBgkqhkiG9w0BAQsF
| ADBEMRMwEQYKCZImiZPyLGQBGRYDaHRiMRYwFAYKCZImiZPyLGQBGRYGb2ZmaWNl
| MRUwEwYDVQQDEwxvZmZpY2UtREMtQ0EwHhcNMjMwNTEwMTIzNjU4WhcNMjQwNTA5
| MTIzNjU4WjAYMRYwFAYDVQQDEw1EQy5vZmZpY2UuaHRiMIIBIjANBgkqhkiG9w0B
| AQEFAAOCAQ8AMIIBCgKCAQEA15Wa3dfyWK0+9iRvZ2H4VWeXwLq40Ee6jzcu8buW
| D/Hp4rubrQa5X2/iS3NdXMsxamygq4s7R5AJa9Ys3I7sm59ctlCo/vjVag0hbqhU
| 5qjBJ1GCQxdiaqRj3BqAO5Tbt9RUH9oeU/UQMzzUQqwKL/Z+twyh9aL6HDnbPXvM
| IeDewk5y/S6M8DlOc6ORZQfBg8NuroyiPYCNb1+WhednfBB0ahNFqzq2MTDLXMNM
| bLeX2zeO/+dgF1ohsQ9qhFyBtFSsaCMR33PMKNs7Iqji42+O5jVNCvUICelUroex
| 1VrC7ogW/JVSqHY4J+6mXZHJhn7xhu6rJKtFDHLeheheRQIDAQABo4IC4DCCAtww
| LwYJKwYBBAGCNxQCBCIeIABEAG8AbQBhAGkAbgBDAG8AbgB0AHIAbwBsAGwAZQBy
| MB0GA1UdJQQWMBQGCCsGAQUFBwMCBggrBgEFBQcDATAOBgNVHQ8BAf8EBAMCBaAw
| eAYJKoZIhvcNAQkPBGswaTAOBggqhkiG9w0DAgICAIAwDgYIKoZIhvcNAwQCAgCA
| MAsGCWCGSAFlAwQBKjALBglghkgBZQMEAS0wCwYJYIZIAWUDBAECMAsGCWCGSAFl
| AwQBBTAHBgUrDgMCBzAKBggqhkiG9w0DBzA5BgNVHREEMjAwoB8GCSsGAQQBgjcZ
| AaASBBA2idyIqAZET5Xm5iLN7Fc3gg1EQy5vZmZpY2UuaHRiMB0GA1UdDgQWBBRS
| FLVfJhlc3XkBccZHJjyKvpRS1TAfBgNVHSMEGDAWgBRgOpmCFktRJECTymSHaes3
| Vx3p9jCBxAYDVR0fBIG8MIG5MIG2oIGzoIGwhoGtbGRhcDovLy9DTj1vZmZpY2Ut
| REMtQ0EsQ049REMsQ049Q0RQLENOPVB1YmxpYyUyMEtleSUyMFNlcnZpY2VzLENO
| PVNlcnZpY2VzLENOPUNvbmZpZ3VyYXRpb24sREM9b2ZmaWNlLERDPWh0Yj9jZXJ0
| aWZpY2F0ZVJldm9jYXRpb25MaXN0P2Jhc2U/b2JqZWN0Q2xhc3M9Y1JMRGlzdHJp
| YnV0aW9uUG9pbnQwgb0GCCsGAQUFBwEBBIGwMIGtMIGqBggrBgEFBQcwAoaBnWxk
| YXA6Ly8vQ049b2ZmaWNlLURDLUNBLENOPUFJQSxDTj1QdWJsaWMlMjBLZXklMjBT
| ZXJ2aWNlcyxDTj1TZXJ2aWNlcyxDTj1Db25maWd1cmF0aW9uLERDPW9mZmljZSxE
| Qz1odGI/Y0FDZXJ0aWZpY2F0ZT9iYXNlP29iamVjdENsYXNzPWNlcnRpZmljYXRp
| b25BdXRob3JpdHkwDQYJKoZIhvcNAQELBQADggEBABw9WEKbYyfAE7PZ0Plb7lxB
| Ftvjpqh2Q9RkdSlxQNdWMfSsZozN6UNTG7mgJBB/T9vZpi8USJTGwf1EfygiDbm1
| yofBMvpqLAXg4ANvWXTDChYSumhlt7W+gJzTgWd4mgRp576acFojnNCqQRhYCD8r
| 6r/PIwlCDSwfLExxhQs7ZL3Jkqt/fP85ic3W9GuzwI9isPZmwsezP/korptA7utb
| sJHn2bydwf907VX2usW8yRmpuRZyvfsbYHYjJqFgohB5dh26ltEQz2vX6y4Mte4L
| 024aNx/gANh3F4gFXpGrAWdVxnHXc1QV9OVRHO+FAL30xdhosJ4D4HdRTDjCfqw=
|_-----END CERTIFICATE-----
|_ssl-date: TLS randomness does not represent time
3269/tcp  open  ssl/ldap      syn-ack Microsoft Windows Active Directory LDAP (Domain: office.htb0., Site: Default-First-Site-Name)
|_ssl-date: TLS randomness does not represent time
| ssl-cert: Subject: commonName=DC.office.htb
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:DC.office.htb
| Issuer: commonName=office-DC-CA/domainComponent=office
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2023-05-10T12:36:58
| Not valid after:  2024-05-09T12:36:58
| MD5:   b83fab78db28734dde8411e9420f8878
| SHA-1: 36c4cedf91853d4c598c739a8bc7a0624458cfe4
| -----BEGIN CERTIFICATE-----
| MIIFyzCCBLOgAwIBAgITQAAAAAMdA83RpYN55AAAAAAAAzANBgkqhkiG9w0BAQsF
| ADBEMRMwEQYKCZImiZPyLGQBGRYDaHRiMRYwFAYKCZImiZPyLGQBGRYGb2ZmaWNl
| MRUwEwYDVQQDEwxvZmZpY2UtREMtQ0EwHhcNMjMwNTEwMTIzNjU4WhcNMjQwNTA5
| MTIzNjU4WjAYMRYwFAYDVQQDEw1EQy5vZmZpY2UuaHRiMIIBIjANBgkqhkiG9w0B
| AQEFAAOCAQ8AMIIBCgKCAQEA15Wa3dfyWK0+9iRvZ2H4VWeXwLq40Ee6jzcu8buW
| D/Hp4rubrQa5X2/iS3NdXMsxamygq4s7R5AJa9Ys3I7sm59ctlCo/vjVag0hbqhU
| 5qjBJ1GCQxdiaqRj3BqAO5Tbt9RUH9oeU/UQMzzUQqwKL/Z+twyh9aL6HDnbPXvM
| IeDewk5y/S6M8DlOc6ORZQfBg8NuroyiPYCNb1+WhednfBB0ahNFqzq2MTDLXMNM
| bLeX2zeO/+dgF1ohsQ9qhFyBtFSsaCMR33PMKNs7Iqji42+O5jVNCvUICelUroex
| 1VrC7ogW/JVSqHY4J+6mXZHJhn7xhu6rJKtFDHLeheheRQIDAQABo4IC4DCCAtww
| LwYJKwYBBAGCNxQCBCIeIABEAG8AbQBhAGkAbgBDAG8AbgB0AHIAbwBsAGwAZQBy
| MB0GA1UdJQQWMBQGCCsGAQUFBwMCBggrBgEFBQcDATAOBgNVHQ8BAf8EBAMCBaAw
| eAYJKoZIhvcNAQkPBGswaTAOBggqhkiG9w0DAgICAIAwDgYIKoZIhvcNAwQCAgCA
| MAsGCWCGSAFlAwQBKjALBglghkgBZQMEAS0wCwYJYIZIAWUDBAECMAsGCWCGSAFl
| AwQBBTAHBgUrDgMCBzAKBggqhkiG9w0DBzA5BgNVHREEMjAwoB8GCSsGAQQBgjcZ
| AaASBBA2idyIqAZET5Xm5iLN7Fc3gg1EQy5vZmZpY2UuaHRiMB0GA1UdDgQWBBRS
| FLVfJhlc3XkBccZHJjyKvpRS1TAfBgNVHSMEGDAWgBRgOpmCFktRJECTymSHaes3
| Vx3p9jCBxAYDVR0fBIG8MIG5MIG2oIGzoIGwhoGtbGRhcDovLy9DTj1vZmZpY2Ut
| REMtQ0EsQ049REMsQ049Q0RQLENOPVB1YmxpYyUyMEtleSUyMFNlcnZpY2VzLENO
| PVNlcnZpY2VzLENOPUNvbmZpZ3VyYXRpb24sREM9b2ZmaWNlLERDPWh0Yj9jZXJ0
| aWZpY2F0ZVJldm9jYXRpb25MaXN0P2Jhc2U/b2JqZWN0Q2xhc3M9Y1JMRGlzdHJp
| YnV0aW9uUG9pbnQwgb0GCCsGAQUFBwEBBIGwMIGtMIGqBggrBgEFBQcwAoaBnWxk
| YXA6Ly8vQ049b2ZmaWNlLURDLUNBLENOPUFJQSxDTj1QdWJsaWMlMjBLZXklMjBT
| ZXJ2aWNlcyxDTj1TZXJ2aWNlcyxDTj1Db25maWd1cmF0aW9uLERDPW9mZmljZSxE
| Qz1odGI/Y0FDZXJ0aWZpY2F0ZT9iYXNlP29iamVjdENsYXNzPWNlcnRpZmljYXRp
| b25BdXRob3JpdHkwDQYJKoZIhvcNAQELBQADggEBABw9WEKbYyfAE7PZ0Plb7lxB
| Ftvjpqh2Q9RkdSlxQNdWMfSsZozN6UNTG7mgJBB/T9vZpi8USJTGwf1EfygiDbm1
| yofBMvpqLAXg4ANvWXTDChYSumhlt7W+gJzTgWd4mgRp576acFojnNCqQRhYCD8r
| 6r/PIwlCDSwfLExxhQs7ZL3Jkqt/fP85ic3W9GuzwI9isPZmwsezP/korptA7utb
| sJHn2bydwf907VX2usW8yRmpuRZyvfsbYHYjJqFgohB5dh26ltEQz2vX6y4Mte4L
| 024aNx/gANh3F4gFXpGrAWdVxnHXc1QV9OVRHO+FAL30xdhosJ4D4HdRTDjCfqw=
|_-----END CERTIFICATE-----
9389/tcp  open  mc-nmf        syn-ack .NET Message Framing
49664/tcp open  msrpc         syn-ack Microsoft Windows RPC
49668/tcp open  msrpc         syn-ack Microsoft Windows RPC
49681/tcp open  ncacn_http    syn-ack Microsoft Windows RPC over HTTP 1.0
51966/tcp open  msrpc         syn-ack Microsoft Windows RPC
51984/tcp open  msrpc         syn-ack Microsoft Windows RPC
56658/tcp open  msrpc         syn-ack Microsoft Windows RPC
Service Info: Hosts: DC, www.example.com; OS: Windows; CPE: cpe:/o:microsoft:windows

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
this web has robot file and have dir 
