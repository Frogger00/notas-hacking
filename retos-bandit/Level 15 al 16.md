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
notAfter=Feb 21 06:20:29 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 06:20:29 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
     Start Time: 1676992546
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
bandit15@bandit:~$ 
````

## Notas adicionales


## Referencias

