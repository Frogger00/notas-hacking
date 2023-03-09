# Bandit Level 26 → 27

## Objetivo
Good job getting a shell! Now hurry and grab the password for bandit27!

## Datos de acceso a nivel
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1

## Solución
````bash
C:\Users\Zarazua>ssh bandit26@bandit.labs.overthewire.org -p 2220
ECDSA host key for IP address '13.53.149.110' not in list of known hosts.
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit26@bandit.labs.overthewire.org's password:

  _                     _ _ _   ___   __
 | |                   | (_) | |__ \ / /
:shell
bandit26@bandit:~$ ls
bandit27-do  text.txt
bandit26@bandit:~$ ./bandit27-do id
uid=11026(bandit26) gid=11026(bandit26) euid=11027(bandit27) groups=11026(bandit26)
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
bandit26@bandit:~$
````

## Notas adicionales

## Referencias

