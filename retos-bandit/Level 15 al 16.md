# Bandit Level 15 → 16

## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

## Datos de acceso a nivel
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

## Solución
````bash
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Mar  6 22:20:05 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Mar  6 22:20:05 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Mar  6 22:19:05 2023 GMT; NotAfter: Mar  6 22:20:05 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEPdp+IzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMzA2MjIxOTA1WhcNMjMwMzA2MjIyMDA1WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCg
jgIA2qmltEjw3vzUIAIK1fNai6bUromNC2zbcJgAZn0jVUuSu7vMKMPPDw8TUCqf
o3qbbhF76+KI3LojgYirZ+eY41XWRL5s4QNC7ydPndsF/2PLDoWZY3gkxgePfhvC
FPQEzL6ATIV2xcAewQoh9ifdCm1ffjamFQ+7Sem/V+C7srnwUomZQwzB5GJS8wCz
U1M8YiAjBTrJpJQvWAVdYIBsDFq0MVxYAU5BoyHvKjBFB/CTDXuXFAjKI1wC8qj1
b0gCTcFi0gQNxREFhN9VMhntkOyU/8nXCMSg8EK7rI4WHjRx1XKBiLEKlSs2DKg6
DEakOfmlFUSIwkBAXG7bAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQAe
1/W5N0hlOOD6Rd+imZz0Y98aykyjrL6sXxRVFUAGiB06l4fQu6DjONEvdt7XyT8m
7eBdjUe9h+yg6/LrAXznCnViy5o3aDhygTonh8GT/O5EuXqeW9oMMJrad5bXnIWr
GAlQRb8Pzng+WiaF8ZJpvZZfxxFMHadYkt+ElWO30WgO1WFUCRTL9QoTheJGaoPV
qAVBl8kFViX7pKxPLTQVeTK/TSZHWlhwiNQaf/Uoj5HRrnNv7KyajRneEhRW0irk
FjPXWf8/OuvtGUkCykanVu5Jaa/h9HjxnXS/ktK35tArd8ulY2S7eoQnuGK66NNr
Qu4d71t3tUxj5XJS6z46
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
    Session-ID: 0275BE10D0921A1757F0B933A249ADB3823A466AD06C61052E68A548D7811649
    Session-ID-ctx:
    Resumption PSK: E395E0676A21663E67894A50B9E30990D2113818D8F43EFF652726D816A8A8A0CA696E6501CFEC0875F0BD5E2252D106
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 0a 44 21 89 48 d6 df a0-94 86 e2 cc a6 54 ac 7c   .D!.H........T.|
    0010 - 7a ee 9b c7 10 04 c3 c2-f0 85 31 94 c6 00 b1 a3   z.........1.....
    0020 - cd 71 a1 83 5c 1d 10 4d-c3 8a 38 38 54 e2 b3 c0   .q..\..M..88T...
    0030 - 91 f6 86 64 b6 d3 1d 34-3d b7 10 b4 15 48 b8 02   ...d...4=....H..
    0040 - 1d ee 3d 13 19 91 b9 77-13 a4 cd d2 2a cd 9a 9a   ..=....w....*...
    0050 - ce b1 db 5b 62 b5 5a f5-3f b2 25 d4 db e2 e8 66   ...[b.Z.?.%....f
    0060 - 00 fe 71 68 e5 40 30 7f-69 60 30 9d 92 eb ab dc   ..qh.@0.i`0.....
    0070 - c9 11 41 11 51 09 1d 4e-84 b9 56 35 56 45 c9 05   ..A.Q..N..V5VE..
    0080 - eb db 1e 8a 5a d1 f8 6a-32 72 b6 c6 76 2b 9d ce   ....Z..j2r..v+..
    0090 - 3e 3a 7b b6 47 69 92 4e-5b bd ec c6 31 40 63 65   >:{.Gi.N[...1@ce
    00a0 - 5e 98 7d 6b cd 2b c7 8b-4f 2c bb 7b c9 24 7e fd   ^.}k.+..O,.{.$~.
    00b0 - b3 39 d9 8e 7a f3 88 ad-e8 ee ff e8 92 01 3b 65   .9..z.........;e
    00c0 - 94 4c d1 b6 fa ee cd 8e-2e 9f 3b b2 c4 09 a4 53   .L........;....S

    Start Time: 1678340245
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
    Session-ID: 3E8DA59EAD8AA89F4768667E5D1732726D937B103A9F98CC1CB5E83F8FA78461
    Session-ID-ctx:
    Resumption PSK: 8832C027BE0DE24985B56D570DA9E666977528A596865B9B28FDE37002FE4D7B8F6FF82E6EEB14F9017235BB991BDB13
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 0a 44 21 89 48 d6 df a0-94 86 e2 cc a6 54 ac 7c   .D!.H........T.|
    0010 - b5 40 19 3b e6 35 1e af-98 40 60 3f a5 66 5f 00   .@.;.5...@`?.f_.
    0020 - 83 6b 2c 69 84 19 d7 2f-11 7b b1 b0 11 0b a9 a8   .k,i.../.{......
    0030 - 61 d0 08 db ba c7 7b 8d-a5 ee 03 f3 60 35 be 6c   a.....{.....`5.l
    0040 - 0f 33 e0 d2 1c 12 bc 58-17 cb 32 76 36 bd ff 79   .3.....X..2v6..y
    0050 - 49 b2 8e b7 46 0d 56 05-d3 fd 66 71 75 2a c9 07   I...F.V...fqu*..
    0060 - 4f c0 8f 4d e8 f4 9e 4c-08 0d 71 4e 3b 84 15 2f   O..M...L..qN;../
    0070 - ae 9a ad cf 0e 99 21 22-78 df 6b b5 f5 4a 20 e9   ......!"x.k..J .
    0080 - f7 9d b3 f6 61 aa 1d e1-cf 96 43 bc a1 e7 e0 45   ....a.....C....E
    0090 - 3d 64 f5 31 64 f2 ea c6-34 fc 41 1b bc e6 34 bd   =d.1d...4.A...4.
    00a0 - 51 10 c6 ba f5 fd 9f 62-00 f9 68 b0 59 4c 36 05   Q......b..h.YL6.
    00b0 - a1 86 77 95 6b 15 df 1c-78 d5 1f bd 78 27 1a 8d   ..w.k...x...x'..
    00c0 - f5 d8 82 35 15 0f a0 da-a9 45 4b 33 04 c0 19 ff   ...5.....EK3....

    Start Time: 1678340245
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
````

## Notas adicionales


## Referencias

