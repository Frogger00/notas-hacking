# Bandit Level 16 → 17

## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Datos de acceso a nivel
JQttfApK4SeyHwDlI9SXGR50qclOAil1

## Solución
````bash
bandit16@bandit:~$ nmap -v -A -T4 -p 31000-32000 localhost
Starting Nmap 7.80 ( https://nmap.org ) at 2023-03-09 05:56 UTC
NSE: Loaded 151 scripts for scanning.
NSE: Script Pre-scanning.
Initiating NSE at 05:56
Completed NSE at 05:56, 0.00s elapsed
Initiating NSE at 05:56
Completed NSE at 05:56, 0.00s elapsed
Initiating NSE at 05:56
Completed NSE at 05:56, 0.00s elapsed
Initiating Ping Scan at 05:56
Scanning localhost (127.0.0.1) [2 ports]
Completed Ping Scan at 05:56, 0.00s elapsed (1 total hosts)
Initiating Connect Scan at 05:56
Scanning localhost (127.0.0.1) [1001 ports]
Discovered open port 31691/tcp on 127.0.0.1
Discovered open port 31046/tcp on 127.0.0.1
Discovered open port 31518/tcp on 127.0.0.1
Discovered open port 31790/tcp on 127.0.0.1
Discovered open port 31960/tcp on 127.0.0.1
Completed Connect Scan at 05:56, 0.02s elapsed (1001 total ports)
Initiating Service scan at 05:56
Scanning 5 services on localhost (127.0.0.1)
Service scan Timing: About 20.00% done; ETC: 05:59 (0:02:44 remaining)
Completed Service scan at 05:57, 97.91s elapsed (5 services on 1 host)
NSE: Script scanning 127.0.0.1.
Initiating NSE at 05:57
Completed NSE at 05:57, 0.03s elapsed
Initiating NSE at 05:57
Completed NSE at 05:57, 0.06s elapsed
Initiating NSE at 05:57
Completed NSE at 05:57, 0.00s elapsed
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00016s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE     VERSION
31046/tcp open  echo
31518/tcp open  ssl/echo
| ssl-cert: Subject: commonName=localhost
| Subject Alternative Name: DNS:localhost
| Issuer: commonName=localhost
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha1WithRSAEncryption
| Not valid before: 2023-03-06T22:19:07
| Not valid after:  2023-03-06T22:20:07
| MD5:   6c1a 9c26 dc6b 90f7 21d7 3690 4a77 ee93
|_SHA-1: 71a8 ab56 11dd 3079 f8c5 c41c 334f 1ab9 6f0e ebb1
31691/tcp open  echo
31790/tcp open  ssl/unknown
| fingerprint-strings:
|   FourOhFourRequest, GenericLines, GetRequest, HTTPOptions, Help, Kerberos, LDAPSearchReq, LPDString, RTSPRequest, SIPOptions, SSLSessionReq, TLSSessionReq, TerminalServerCookie:
|_    Wrong! Please enter the correct current password
| ssl-cert: Subject: commonName=localhost
| Subject Alternative Name: DNS:localhost
| Issuer: commonName=localhost
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha1WithRSAEncryption
| Not valid before: 2023-03-06T22:19:06
| Not valid after:  2023-03-06T22:20:06
| MD5:   9ed8 683d a4aa 35ad 9086 9eb7 67d1 7d2d
|_SHA-1: ced0 4bb5 2cce 55d5 d6b1 00a5 6472 5101 ae93 65d7
31960/tcp open  echo
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port31790-TCP:V=7.80%T=SSL%I=7%D=3/9%Time=64097507%P=x86_64-pc-linux-gn
SF:u%r(GenericLines,31,"Wrong!\x20Please\x20enter\x20the\x20correct\x20cur
SF:rent\x20password\n")%r(GetRequest,31,"Wrong!\x20Please\x20enter\x20the\
SF:x20correct\x20current\x20password\n")%r(HTTPOptions,31,"Wrong!\x20Pleas
SF:e\x20enter\x20the\x20correct\x20current\x20password\n")%r(RTSPRequest,3
SF:1,"Wrong!\x20Please\x20enter\x20the\x20correct\x20current\x20password\n
SF:")%r(Help,31,"Wrong!\x20Please\x20enter\x20the\x20correct\x20current\x2
SF:0password\n")%r(SSLSessionReq,31,"Wrong!\x20Please\x20enter\x20the\x20c
SF:orrect\x20current\x20password\n")%r(TerminalServerCookie,31,"Wrong!\x20
SF:Please\x20enter\x20the\x20correct\x20current\x20password\n")%r(TLSSessi
SF:onReq,31,"Wrong!\x20Please\x20enter\x20the\x20correct\x20current\x20pas
SF:sword\n")%r(Kerberos,31,"Wrong!\x20Please\x20enter\x20the\x20correct\x2
SF:0current\x20password\n")%r(FourOhFourRequest,31,"Wrong!\x20Please\x20en
SF:ter\x20the\x20correct\x20current\x20password\n")%r(LPDString,31,"Wrong!
SF:\x20Please\x20enter\x20the\x20correct\x20current\x20password\n")%r(LDAP
SF:SearchReq,31,"Wrong!\x20Please\x20enter\x20the\x20correct\x20current\x2
SF:0password\n")%r(SIPOptions,31,"Wrong!\x20Please\x20enter\x20the\x20corr
SF:ect\x20current\x20password\n");

NSE: Script Post-scanning.
Initiating NSE at 05:57
Completed NSE at 05:57, 0.00s elapsed
Initiating NSE at 05:57
Completed NSE at 05:57, 0.00s elapsed
Initiating NSE at 05:57
Completed NSE at 05:57, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 98.49 seconds
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Mar  6 22:20:06 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Mar  6 22:20:06 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Mar  6 22:19:06 2023 GMT; NotAfter: Mar  6 22:20:06 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEJ75LfDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMzA2MjIxOTA2WhcNMjMwMzA2MjIyMDA2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCv
EdeEVzwpHCKsFqiCP5zC8GKGj1KH30I9YzOo80wNwzBTuRfV4p0Qo16xNyyqRrWm
H+xQrKDiBYswcs+kGAScbSWIksm4HajAvu/NnI5ou+dU+chGfAv+Anlf0OYhMHmA
HRMTZRGTipL0LaPqiHaCHGLD6iJcdwGrqpxQh6otFjvCjO1tvhAAb29S6hEsYbfc
D8x3PL2NqGGhl0tA7GrLufcFLVBfsnsp2nP6QIygoU3C41xtZ384PQDX7hZpJtKd
2FXTpgrH1Q+Ttp8BVO1FZfdD8AXoYb56cOGtHAcdHzbv+YGme8mceiNmZqLYBO6m
3nldnCkiUDd/yoc+lhz/AgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQCn
N6uyaQKbKXX5ya6qEdoYP6NG9wJNeQT7WrtIW9c1Pmea0XMP1KjXpQyd41pD/6rg
t03TvsQB54elCWVk83CDpyDOuyPrvMVVPeT3WNwyE99LT3J/saj+i5WjWm8iu16B
Qj4JflqPlIuuS4g7oC4+l8tRAi7MAtaWr24AdLyToRnhV9KPWyZx49F2vtw3P96X
LDoxdFYmnrZ9/jTYf8KJIIVz+D+SQnE2hxWnd8cqVgDOtCikbRD6acGAINFBKSzQ
IdnebbIPrYM231bJ7crT1nK+m0+NqC6nvTvXdvUBkQ1kS73C2V4Md9Q/cf5PDyp8
hJBls+S5ds1OdRukoyZZ
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: D47FCE89087415CDF1F31B8F11B918D4B134A879118AEE8A297E021C9B8F9287
    Session-ID-ctx:
    Resumption PSK: 7DC3ADE6386337FE148CBCE45FA655F0ECD00A5369AB16B7FE1ED56114B1A54AB55399E4BB7DF712F867817FFBADBD11
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 9c 21 04 a6 60 53 5f ac-6f 60 d2 67 ee 71 e7 0f   .!..`S_.o`.g.q..
    0010 - d1 2a f5 79 08 7f ad 54-ec 14 06 b6 b8 88 5a 86   .*.y...T......Z.
    0020 - 0d d5 54 f7 2f e1 13 f2-09 c5 cc 74 f8 f6 0d 24   ..T./......t...$
    0030 - ac 67 ba 55 59 06 28 74-63 92 47 7c 71 ce 09 29   .g.UY.(tc.G|q..)
    0040 - 70 e6 78 72 a1 85 f9 9e-0d cf b2 3b 0a a9 08 90   p.xr.......;....
    0050 - ea 60 86 b2 d5 02 d7 a0-44 89 81 ab 20 9a c1 ff   .`......D... ...
    0060 - 2d fe d7 af 40 d5 e4 4a-5f 3e 02 10 02 7e 43 33   -...@..J_>...~C3
    0070 - fb 6c 7e a3 e8 60 7f ae-d5 f8 c8 3b 07 c8 c7 ff   .l~..`.....;....
    0080 - 0d 48 1a ce 3e 8c d5 8b-1c 5d 70 b2 78 27 ca 13   .H..>....]p.x'..
    0090 - e1 4f 13 d2 2e 68 94 cb-78 a6 4c ed f3 d3 57 d2   .O...h..x.L...W.
    00a0 - 53 1b 90 47 9f 6d 4c cd-85 82 b5 ca fa f6 be 1a   S..G.mL.........
    00b0 - 70 bc 1a 9e 5a 8e 0e 46-8a 92 be 08 a8 94 23 53   p...Z..F......#S
    00c0 - bc 6f 8f c1 d3 65 8e c7-4c 1c 77 6c ab cc 7b 08   .o...e..L.wl..{.

    Start Time: 1678341513
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 49A37BEE6A70BC75F0867987D3064B5F9EB2182BD9D769474FDED7B2A6B4AE3A
    Session-ID-ctx:
    Resumption PSK: 6925BD910D6619E881D9621E381081A3B7FA0D8992984D465185EB643938E5A56F66BEEC30E50BAD0847D1A7D3E027A3
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 9c 21 04 a6 60 53 5f ac-6f 60 d2 67 ee 71 e7 0f   .!..`S_.o`.g.q..
    0010 - d4 e6 92 f6 a5 9f 33 c8-ca 6f 63 ad a6 d1 19 85   ......3..oc.....
    0020 - eb dc 5e a4 82 c3 65 58-51 a2 70 bd 3f ca b3 3c   ..^...eXQ.p.?..<
    0030 - cf 0f 5f ab 68 5c 85 1d-6a fb 76 2b 15 61 45 d3   .._.h\..j.v+.aE.
    0040 - 79 83 3a 0f af 5c 6f bd-1b 84 be 98 35 82 ef 90   y.:..\o.....5...
    0050 - de 39 ee 1f 95 91 58 45-c8 4b 3b 9d 94 db 77 a4   .9....XE.K;...w.
    0060 - 81 d7 47 0a 60 bb 9f 6d-db b8 39 6e 42 71 9a 5a   ..G.`..m..9nBq.Z
    0070 - 02 1d 78 7b 08 61 00 0a-aa ba 5a 7f 14 0f 00 bb   ..x{.a....Z.....
    0080 - fa b5 c9 bc bf 47 8e 89-7d da 84 20 00 6c db 1a   .....G..}.. .l..
    0090 - 50 fe bd 74 6e e4 54 a9-8f fa 69 a6 06 e1 ab 2d   P..tn.T...i....-
    00a0 - 39 5d ca 74 e6 b8 82 52-c5 b0 e2 7e ba 3f 39 4d   9].t...R...~.?9M
    00b0 - 77 79 97 17 aa 13 f6 c5-de 59 60 f6 03 00 fc fd   wy.......Y`.....
    00c0 - ae 2b a6 90 61 d0 1b 41-6e 3b 6a 0c 7d 1d fd 03   .+..a..An;j.}...

    Start Time: 1678341513
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed
bandit16@bandit:~$ mkdir /tmp/llave
bandit16@bandit:~$ cd /tmp/llave
bandit16@bandit:/tmp/llave$ nano llave.txt
Unable to create directory /home/bandit16/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit16@bandit:/tmp/llave$ chmod 600 llave.txt
bandit16@bandit:/tmp/llave$ ssh bandit17@localhost -p2220 -i llave.txt
bandit17@bandit:~$
````

## Notas adicionales


## Referencias

