# Bandit Level 14 → 15

## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

## Datos de acceso a nivel
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

## Solución
````bash
bandit14@bandit:~$ nc localhost 30000

Wrong! Please enter the correct current password

bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
````

## Notas adicionales


## Referencias
