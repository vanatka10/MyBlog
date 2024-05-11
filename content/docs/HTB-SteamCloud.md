i dont have anything to say so just do it

# nmap
```
# Nmap 7.93 scan initiated Fri May 10 13:10:41 2024 as: nmap -vvv -p 22,2379,2380,8443,10256,10250,10249 -sC -sV -oN rustscan/rustscan.txt 10.10.11.133
Nmap scan report for 10.10.11.133
Host is up, received conn-refused (0.058s latency).
Scanned at 2024-05-10 13:10:41 EDT for 102s

PORT      STATE SERVICE          REASON  VERSION
22/tcp    open  ssh              syn-ack OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
| ssh-hostkey: 
|   2048 fcfb90ee7c73a1d4bf87f871e844c63c (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCu4TNCZjLe74tZ0HyspkMaghndsvuXkZJa4lJBt9arqgkm6u2HI/RRdwbjE14au2u/YF89y23Q55iOGraA+9JjpyTzDPo3kxE/RisYzJaUDmzza+hqEeyTxXkZby9+DAhKm5UXs7M2CMDr3cwOPPQ96u/zUX0gDG3CfYw4fAi2TDGa6jU5KmGzIQz6SQR3Bv6IYLDwzNJ0nHNZ3jxSbFS3SsmTwK749GJLrv62wAf4uUL/Ihynl8cCG5aor6T0Fk44v/9ndfujznBvWaMYVPpf9B49XlD7OhXB5pCK2nPZrdze+ch6yhAM/vYrYA4sNk3IuFG3OCrDkVeUJn5sJKx5
|   256 46832b1b01db71646a3e27cb536f81a1 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBHVj7iKnl8SWdGz6J4F3kvpZjM1Tim0iHlUnQByS8xJYnfwttLxVwGb+aaGbRhOJu4mq9y4crwFh50rC9mAEHWo=
|   256 1d8dd341f3ffa437e8ac780889c2e3c5 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIHXIZpU9XbtZ2zvx8rFEYTfGp+8JCJx5lSiRNEcqUFG8
2379/tcp  open  ssl/etcd-client? syn-ack
| ssl-cert: Subject: commonName=steamcloud
| Subject Alternative Name: DNS:localhost, DNS:steamcloud, IP Address:10.10.11.133, IP Address:127.0.0.1, IP Address:0:0:0:0:0:0:0:1
| Issuer: commonName=etcd-ca
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2024-05-10T16:57:12
| Not valid after:  2025-05-10T16:57:12
| MD5:   cc8bf57afb67df7c2f9ec55ab0b37330
| SHA-1: f33fe4056b708845652e8e3bdd6b5e94677bb658
| -----BEGIN CERTIFICATE-----
| MIIDSzCCAjOgAwIBAgIIG3YGILpb//MwDQYJKoZIhvcNAQELBQAwEjEQMA4GA1UE
| AxMHZXRjZC1jYTAeFw0yNDA1MTAxNjU3MTJaFw0yNTA1MTAxNjU3MTJaMBUxEzAR
| BgNVBAMTCnN0ZWFtY2xvdWQwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIB
| AQCjLGidSGso3MyuDK+r6kUyqEL8YOOhytQdb7QMkn5eT7OzlLjIxwXtp5jKVwzt
| 66ATvlDBZBmrUOr1+R7iD+AcXQ5ZCmKsm8FZDdB44xb8ouOuJ7QYCpzwlqWWnbVJ
| ThdD6MuT0g+ryA+1MjgILt9IGxxAGKpVmWjrN/lsR0D+lpV4P8GJ2koHhYng0YvF
| Z+6LPeyEOHQi8+b16mCFHdJthvTlmVpIVikP5EXGUiJ40DGyUJdV6swb6s8ghd5W
| di5/2evO0pOVyHsADQF0VSYH8j/Ox8D060mxAMGRjayoHQFfH68smb1pVfzd/INX
| Q8zxcl8ddIc5Zulni8++0XVxAgMBAAGjgaEwgZ4wDgYDVR0PAQH/BAQDAgWgMB0G
| A1UdJQQWMBQGCCsGAQUFBwMBBggrBgEFBQcDAjAMBgNVHRMBAf8EAjAAMB8GA1Ud
| IwQYMBaAFA/i4zvuYJiviRmzVOFbTiD3r0ryMD4GA1UdEQQ3MDWCCWxvY2FsaG9z
| dIIKc3RlYW1jbG91ZIcECgoLhYcEfwAAAYcQAAAAAAAAAAAAAAAAAAAAATANBgkq
| hkiG9w0BAQsFAAOCAQEACogy0pN1UzA0BuA8dDKdMlWMqsrPSolLJfgyD0hyM9xX
| qYcXEXh2RBZVKobajetcK2RNBpB86NfJxboxYLk7Y1GCqzITiMn6pYXp+IKmIdEP
| ZLocg4SDpjYVIqIuO3QEjId3Uqk8EIrDM7/UfZ/vst0GEHEMX83o2Gix/PZrrM3P
| aEfEgUqm1mh6IggrdH308ZEUbcVk35/xRKkaRMwUj5v8EixGP5B6d2sqC1wFMR+d
| Tae4KBxDwLU7nXuSpawLfIotfQZEtIJ+QQLU9HzyPxD78dLz/P/q2NaW6v7fEVQ2
| IZUjT5l5YjMB9mqGFos1yz90vo1zs4vz1eUpUX8jGQ==
|_-----END CERTIFICATE-----
| tls-alpn: 
|_  h2
|_ssl-date: TLS randomness does not represent time
2380/tcp  open  ssl/etcd-server? syn-ack
| tls-alpn: 
|_  h2
|_ssl-date: TLS randomness does not represent time
| ssl-cert: Subject: commonName=steamcloud
| Subject Alternative Name: DNS:localhost, DNS:steamcloud, IP Address:10.10.11.133, IP Address:127.0.0.1, IP Address:0:0:0:0:0:0:0:1
| Issuer: commonName=etcd-ca
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2024-05-10T16:57:12
| Not valid after:  2025-05-10T16:57:12
| MD5:   8b7c127d23a8e526b1f2623259bb8e3c
| SHA-1: 1cf801974368873e0120c5b3262b3dd38815f8f6
| -----BEGIN CERTIFICATE-----
| MIIDSzCCAjOgAwIBAgIIcnrMZ6Ml6dcwDQYJKoZIhvcNAQELBQAwEjEQMA4GA1UE
| AxMHZXRjZC1jYTAeFw0yNDA1MTAxNjU3MTJaFw0yNTA1MTAxNjU3MTJaMBUxEzAR
| BgNVBAMTCnN0ZWFtY2xvdWQwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIB
| AQCx9cWpqgJME2oj3qbJbvrDXeT9Ehiga2umUQY0BwScfcau6X2kgx/zoKimXCwY
| B0NaBwfn+IPKD9UL606diP14YGKMuHsaBCgEVSb2T+KOtFBCnnY1k6QbJ8Tk+9DC
| EExor506eWJuYg3KSfeL3XmJeZyxAMIx9mVHrTSs5iU6hshSJMP08nYEd/SJlI9s
| eVuPg7hE6ePUcrqhYHoPZBZ6gw2m0Su+HsUa813/fEaR151aM9HsX7hBYFEhT3tK
| SBC/VkWpqAAgKKYb4QlNW2vXPUmSJWXULOf9BFibc8aAD6dALRw0eNOKn6o2U0HX
| abReFJDyxR52+LY0Work7MBTAgMBAAGjgaEwgZ4wDgYDVR0PAQH/BAQDAgWgMB0G
| A1UdJQQWMBQGCCsGAQUFBwMBBggrBgEFBQcDAjAMBgNVHRMBAf8EAjAAMB8GA1Ud
| IwQYMBaAFA/i4zvuYJiviRmzVOFbTiD3r0ryMD4GA1UdEQQ3MDWCCWxvY2FsaG9z
| dIIKc3RlYW1jbG91ZIcECgoLhYcEfwAAAYcQAAAAAAAAAAAAAAAAAAAAATANBgkq
| hkiG9w0BAQsFAAOCAQEAd0H0AlMW6FGyeOI9+VbukKnznEL5Eg02/XjUqbnz4fTK
| nJEKB1c166kwN0FVMWD0f8at+aYNi6J0aZ6s4YkBJAdEkP6GG9vJoOvSIMvqBtvh
| 4rzsqvip0ehee17Rf2fb7wDV0poBT4HgkBVyI23OBLkmRkID7SNHpnR5sw1KyG0v
| RPvqZFtHbfTfR9d7hOBbL96x+o0ZB5heZpXepvIeepoPbE8x1Dge0Clnm66iQ4/N
| E33ozpI3RTB4VilqWBH0FM6tpkJVoCuLG2g0y9xGT2SXV09o3W6C9g3M0I9SkJQa
| T5jmr0wsdDVmZZj/wL9U6t4N46S54hwqB2Kqal3IJg==
|_-----END CERTIFICATE-----
8443/tcp  open  ssl/https-alt    syn-ack
| fingerprint-strings: 
|   FourOhFourRequest: 
|     HTTP/1.0 403 Forbidden
|     Audit-Id: dabc8e4a-b7ba-425d-862b-f4a7032824b3
|     Cache-Control: no-cache, private
|     Content-Type: application/json
|     X-Content-Type-Options: nosniff
|     X-Kubernetes-Pf-Flowschema-Uid: 4c14edb6-9b3e-4277-9095-473b48b88cf1
|     X-Kubernetes-Pf-Prioritylevel-Uid: 85f78a7f-943b-45b8-b7e3-ebdfd040cca3
|     Date: Fri, 10 May 2024 17:05:54 GMT
|     Content-Length: 212
|     {"kind":"Status","apiVersion":"v1","metadata":{},"status":"Failure","message":"forbidden: User "system:anonymous" cannot get path "/nice ports,/Trinity.txt.bak"","reason":"Forbidden","details":{},"code":403}
|   GetRequest: 
|     HTTP/1.0 403 Forbidden
|     Audit-Id: 40a94efb-5a1a-4f71-84d2-787b7b4131f7
|     Cache-Control: no-cache, private
|     Content-Type: application/json
|     X-Content-Type-Options: nosniff
|     X-Kubernetes-Pf-Flowschema-Uid: 4c14edb6-9b3e-4277-9095-473b48b88cf1
|     X-Kubernetes-Pf-Prioritylevel-Uid: 85f78a7f-943b-45b8-b7e3-ebdfd040cca3
|     Date: Fri, 10 May 2024 17:05:53 GMT
|     Content-Length: 185
|     {"kind":"Status","apiVersion":"v1","metadata":{},"status":"Failure","message":"forbidden: User "system:anonymous" cannot get path "/"","reason":"Forbidden","details":{},"code":403}
|   HTTPOptions: 
|     HTTP/1.0 403 Forbidden
|     Audit-Id: b2b26701-1d23-4ab6-b43f-c9451ed5f25a
|     Cache-Control: no-cache, private
|     Content-Type: application/json
|     X-Content-Type-Options: nosniff
|     X-Kubernetes-Pf-Flowschema-Uid: 4c14edb6-9b3e-4277-9095-473b48b88cf1
|     X-Kubernetes-Pf-Prioritylevel-Uid: 85f78a7f-943b-45b8-b7e3-ebdfd040cca3
|     Date: Fri, 10 May 2024 17:05:54 GMT
|     Content-Length: 189
|_    {"kind":"Status","apiVersion":"v1","metadata":{},"status":"Failure","message":"forbidden: User "system:anonymous" cannot options path "/"","reason":"Forbidden","details":{},"code":403}
|_http-title: Site doesn't have a title (application/json).
| tls-alpn: 
|   h2
|_  http/1.1
| ssl-cert: Subject: commonName=minikube/organizationName=system:masters
| Subject Alternative Name: DNS:minikubeCA, DNS:control-plane.minikube.internal, DNS:kubernetes.default.svc.cluster.local, DNS:kubernetes.default.svc, DNS:kubernetes.default, DNS:kubernetes, DNS:localhost, IP Address:10.10.11.133, IP Address:10.96.0.1, IP Address:127.0.0.1, IP Address:10.0.0.1
| Issuer: commonName=minikubeCA
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2024-05-09T16:57:11
| Not valid after:  2027-05-10T16:57:11
| MD5:   84356318d2a0b27b886c559f8a2ec947
| SHA-1: 47e3419019c35a8d2dcd912f8214b1b7990e703f
| -----BEGIN CERTIFICATE-----
| MIID3DCCAsSgAwIBAgIBAjANBgkqhkiG9w0BAQsFADAVMRMwEQYDVQQDEwptaW5p
| a3ViZUNBMB4XDTI0MDUwOTE2NTcxMVoXDTI3MDUxMDE2NTcxMVowLDEXMBUGA1UE
| ChMOc3lzdGVtOm1hc3RlcnMxETAPBgNVBAMTCG1pbmlrdWJlMIIBIjANBgkqhkiG
| 9w0BAQEFAAOCAQ8AMIIBCgKCAQEAqVIkWoddbEfB4nVXfRtlutwSVGlgBOr2p6pF
| KtJ69IMTYGqBqo87BVzcnBh0ghqsK3ysvjcvPE23UArK6lcPvpImild697Fktqf+
| Dd3BGmF6VYapNhgcwBDSyXXRW6N3Yw5chHQ1wiI72wmLIHeWsIpS8so8NFI0Vlmu
| JErEkkVVH0Mv8pOZmfMbiV0KpBiu+rDWu/csHEvLflE4aMM0sBx5ram0c/jMdnnA
| YOA+Grxg1V6/2YlEvI/ZXjpVVmCp91kHXAnYr9OCbAleAy5huwA5I2Y8lFVSD9Kj
| Du23uzh3olI3xa4VEGbXjGzdlPZeQ0jTUVOwtpR6CVN7+5Al9wIDAQABo4IBHjCC
| ARowDgYDVR0PAQH/BAQDAgWgMB0GA1UdJQQWMBQGCCsGAQUFBwMBBggrBgEFBQcD
| AjAMBgNVHRMBAf8EAjAAMB8GA1UdIwQYMBaAFKlEoIQptW1GxgQZHDJpV6icF0wK
| MIG5BgNVHREEgbEwga6CCm1pbmlrdWJlQ0GCH2NvbnRyb2wtcGxhbmUubWluaWt1
| YmUuaW50ZXJuYWyCJGt1YmVybmV0ZXMuZGVmYXVsdC5zdmMuY2x1c3Rlci5sb2Nh
| bIIWa3ViZXJuZXRlcy5kZWZhdWx0LnN2Y4ISa3ViZXJuZXRlcy5kZWZhdWx0ggpr
| dWJlcm5ldGVzgglsb2NhbGhvc3SHBAoKC4WHBApgAAGHBH8AAAGHBAoAAAEwDQYJ
| KoZIhvcNAQELBQADggEBANtlLg03wHibhDidxxgmKEYt5WlkSAPnaRNHw7IC4kTc
| G35wOHpmAh7aIL1uhzYzpRZ0JBdKIE2b1/3Um4lOfQIdcLeEVzeOkC3PYS/FcE29
| TAnuEHb8H7seiDkheKsora7vvpyXoaMY+PvZXxmtWt/N9dhED1vzihTmVVMSiReO
| TfUJLBW0gP0VSTQGNnCVnlmsVwDuYVWyOGEGOwr8jwFgcopAAqxNkTqT1NGsEnPk
| Wn0f5ruj5GYmGVxZA09SaLFEOTHQa8MkaxPnLsLz1p//v7wJqOJ03A9RdeLDu2vW
| tXSdIvo/8ahaoWxJ7DgphNmzZbpXbOQXPxkg1rjNVTI=
|_-----END CERTIFICATE-----
|_ssl-date: TLS randomness does not represent time
10249/tcp open  http             syn-ack Golang net/http server (Go-IPFS json-rpc or InfluxDB API)
|_http-title: Site doesn't have a title (text/plain; charset=utf-8).
10250/tcp open  ssl/http         syn-ack Golang net/http server (Go-IPFS json-rpc or InfluxDB API)
|_http-title: Site doesn't have a title (text/plain; charset=utf-8).
| tls-alpn: 
|   h2
|_  http/1.1
|_ssl-date: TLS randomness does not represent time
| ssl-cert: Subject: commonName=steamcloud@1715360234
| Subject Alternative Name: DNS:steamcloud
| Issuer: commonName=steamcloud-ca@1715360234
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2024-05-10T15:57:14
| Not valid after:  2025-05-10T15:57:14
| MD5:   e62e89460428270fc0acc5877533e130
| SHA-1: 6adea5a4d86479ecf276c7f56ed49dad74b96943
| -----BEGIN CERTIFICATE-----
| MIIDKzCCAhOgAwIBAgIBAjANBgkqhkiG9w0BAQsFADAjMSEwHwYDVQQDDBhzdGVh
| bWNsb3VkLWNhQDE3MTUzNjAyMzQwHhcNMjQwNTEwMTU1NzE0WhcNMjUwNTEwMTU1
| NzE0WjAgMR4wHAYDVQQDDBVzdGVhbWNsb3VkQDE3MTUzNjAyMzQwggEiMA0GCSqG
| SIb3DQEBAQUAA4IBDwAwggEKAoIBAQDZEfCeXSW0ZpYrxHk0w3DxsbgrJJh3F1op
| IicrrGbABpA7sXIne6R6zyM7yaPLgvgPVreOI+Tzt3NhUwCi7oGVvXY8gTUzBpbS
| 0Z4xCLvNXU8xkTrmgnGJx0w4DMbFBz7aD89A3S/KUZxchcpMmLoblFhKopOM1uAC
| nhMvD8uUtFalsqPbUv+vpCGArUg5nsHigFuo19v17fUrHiXMl9XGtr0QsRjsR/ux
| jbwYvF4lssYCxImEwcOz2alhqnspFBoLB+xAgz5CgIoDE/nab8DYP69+jvzOZ2CB
| gosICMdfDRN/zR0fWBclpUYTjjrmWW+y941NdsmKqFwzvDGcryENAgMBAAGjbTBr
| MA4GA1UdDwEB/wQEAwIFoDATBgNVHSUEDDAKBggrBgEFBQcDATAMBgNVHRMBAf8E
| AjAAMB8GA1UdIwQYMBaAFCMA1C9eiFjBz+UtxNsU6hv5wroiMBUGA1UdEQQOMAyC
| CnN0ZWFtY2xvdWQwDQYJKoZIhvcNAQELBQADggEBABX87L5pbZv9wxy7Ia1vfkGc
| 9kc84SgnyHGeyyxqyjWlTlQ/tAykMZtBBwKFlwxIjUbuB8Znyq31Y8+9R++DtInV
| CCG/tJ0AZqh4zP5aYZY4bR3Yxwe0ASd9WaJ0iQK96H8C/pHgIwEZeEeb178UZzCs
| ShVd+Bc1Jebt7uTVSAeHG2wgwKJRx7FiUzN/AomE7os9AnXWk+TPN59k1AlGFjxT
| HLQ5wqPk5dF7ODeqAk93TB1VAcQKrFebNt/gNBQxbQdqC6u8OPipgVCgyqHyVVeb
| UMwXuvval8EespptOf+b4vV9Qmm3zbleYO3ThRnqTOVTV2rORALmG50lIsi4ip0=
|_-----END CERTIFICATE-----
10256/tcp open  http             syn-ack Golang net/http server (Go-IPFS json-rpc or InfluxDB API)
|_http-title: Site doesn't have a title (text/plain; charset=utf-8).
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port8443-TCP:V=7.93%T=SSL%I=7%D=5/10%Time=663E551E%P=x86_64-pc-linux-gn
SF:u%r(GetRequest,22F,"HTTP/1\.0\x20403\x20Forbidden\r\nAudit-Id:\x2040a94
SF:efb-5a1a-4f71-84d2-787b7b4131f7\r\nCache-Control:\x20no-cache,\x20priva
SF:te\r\nContent-Type:\x20application/json\r\nX-Content-Type-Options:\x20n
SF:osniff\r\nX-Kubernetes-Pf-Flowschema-Uid:\x204c14edb6-9b3e-4277-9095-47
SF:3b48b88cf1\r\nX-Kubernetes-Pf-Prioritylevel-Uid:\x2085f78a7f-943b-45b8-
SF:b7e3-ebdfd040cca3\r\nDate:\x20Fri,\x2010\x20May\x202024\x2017:05:53\x20
SF:GMT\r\nContent-Length:\x20185\r\n\r\n{\"kind\":\"Status\",\"apiVersion\
SF:":\"v1\",\"metadata\":{},\"status\":\"Failure\",\"message\":\"forbidden
SF::\x20User\x20\\\"system:anonymous\\\"\x20cannot\x20get\x20path\x20\\\"/
SF:\\\"\",\"reason\":\"Forbidden\",\"details\":{},\"code\":403}\n")%r(HTTP
SF:Options,233,"HTTP/1\.0\x20403\x20Forbidden\r\nAudit-Id:\x20b2b26701-1d2
SF:3-4ab6-b43f-c9451ed5f25a\r\nCache-Control:\x20no-cache,\x20private\r\nC
SF:ontent-Type:\x20application/json\r\nX-Content-Type-Options:\x20nosniff\
SF:r\nX-Kubernetes-Pf-Flowschema-Uid:\x204c14edb6-9b3e-4277-9095-473b48b88
SF:cf1\r\nX-Kubernetes-Pf-Prioritylevel-Uid:\x2085f78a7f-943b-45b8-b7e3-eb
SF:dfd040cca3\r\nDate:\x20Fri,\x2010\x20May\x202024\x2017:05:54\x20GMT\r\n
SF:Content-Length:\x20189\r\n\r\n{\"kind\":\"Status\",\"apiVersion\":\"v1\
SF:",\"metadata\":{},\"status\":\"Failure\",\"message\":\"forbidden:\x20Us
SF:er\x20\\\"system:anonymous\\\"\x20cannot\x20options\x20path\x20\\\"/\\\
SF:"\",\"reason\":\"Forbidden\",\"details\":{},\"code\":403}\n")%r(FourOhF
SF:ourRequest,24A,"HTTP/1\.0\x20403\x20Forbidden\r\nAudit-Id:\x20dabc8e4a-
SF:b7ba-425d-862b-f4a7032824b3\r\nCache-Control:\x20no-cache,\x20private\r
SF:\nContent-Type:\x20application/json\r\nX-Content-Type-Options:\x20nosni
SF:ff\r\nX-Kubernetes-Pf-Flowschema-Uid:\x204c14edb6-9b3e-4277-9095-473b48
SF:b88cf1\r\nX-Kubernetes-Pf-Prioritylevel-Uid:\x2085f78a7f-943b-45b8-b7e3
SF:-ebdfd040cca3\r\nDate:\x20Fri,\x2010\x20May\x202024\x2017:05:54\x20GMT\
SF:r\nContent-Length:\x20212\r\n\r\n{\"kind\":\"Status\",\"apiVersion\":\"
SF:v1\",\"metadata\":{},\"status\":\"Failure\",\"message\":\"forbidden:\x2
SF:0User\x20\\\"system:anonymous\\\"\x20cannot\x20get\x20path\x20\\\"/nice
SF:\x20ports,/Trinity\.txt\.bak\\\"\",\"reason\":\"Forbidden\",\"details\"
SF::{},\"code\":403}\n");
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Fri May 10 13:12:23 2024 -- 1 IP address (1 host up) scanned in 102.61 seconds
```
there are some strange port right
# 8443
![image](https://github.com/vanatka10/myblog/assets/126310360/e029d31e-4bb9-4c74-b29b-c5822541d3a4)

hmmm nothing interesting  

i use dirsearch to scan but still dont get anything interesting

```
403   311B   https://10.10.11.133:8443/api/2/explore/
403   326B   https://10.10.11.133:8443/api/apidocs/swagger.json
403   311B   https://10.10.11.133:8443/api/cask/graphql
403   345B   https://10.10.11.133:8443/api/2/issue/createmeta
403   342B   https://10.10.11.133:8443/api/package_search/v4/documentation
403   308B   https://10.10.11.133:8443/api/jsonws/invoke
403   326B   https://10.10.11.133:8443/api/spec/swagger.json
403   311B   https://10.10.11.133:8443/api/swagger/swagger
403   326B   https://10.10.11.133:8443/api/v1/swagger.json
403   326B   https://10.10.11.133:8443/api/swagger/ui/index
403   299B   https://10.10.11.133:8443/api/timelion/run
403   320B   https://10.10.11.133:8443/api/swagger/index.html
403   348B   https://10.10.11.133:8443/api/swagger/static/index.html
403   326B   https://10.10.11.133:8443/api/v1/swagger.yaml
403   326B   https://10.10.11.133:8443/api/v2/swagger.json
403   353B   https://10.10.11.133:8443/api/vendor/phpunit/phpunit/phpunit
403   350B   https://10.10.11.133:8443/api/v2/helpdesk/discover
403   326B   https://10.10.11.133:8443/api/v2/swagger.yaml
200     2B   https://10.10.11.133:8443/healthz
200   263B   https://10.10.11.133:8443/version
200   263B   https://10.10.11.133:8443/version/

```
because this port use tls certificate so i research something to enum

i see [this post](https://blog.projectdiscovery.io/a-hackers-guide-to-ssl-certificates-featuring-tlsx/)
```
tlsx -u https://10.10.11.133:8443 -san
```
this command use for reconnaissance to discover hostnames associated with a target domain
![image](https://github.com/vanatka10/myblog/assets/126310360/17779a17-adef-4d66-8f0c-839f143cf9d1)

some strange name right?, so what is it?
![image](https://github.com/vanatka10/myblog/assets/126310360/9d50fe56-ac20-48cb-abee-018f49725077)

briefly, Kubernetes is a portable, extensible, open source platform for managing containerized workloads and services

after researching, Kubernetes has something called pods and we can do some thing with that

following [this post](https://www.cyberark.com/resources/threat-research-blog/using-kubelet-client-to-attack-the-kubernetes-cluster) we can get rce

![image](https://github.com/vanatka10/myblog/assets/126310360/fd4fa2cb-9399-403e-93d0-5404e090d6fa)

# user
![image](https://github.com/vanatka10/myblog/assets/126310360/294c6973-d1aa-486e-9b16-db87d7512179)

# root
![image](https://github.com/vanatka10/myblog/assets/126310360/4ba53eaf-a132-4a70-8b2f-c699d840863b)
we are in container so we are root 

so how to escape this

