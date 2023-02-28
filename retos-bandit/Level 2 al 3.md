# Bandit Level 2 → 3

## Objetivo
The password for the next level is stored in a file called spaces in this filename located in the home directory.

## Datos de acceso a nivel
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

## Solución
````bash
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ pwd
/home/bandit2
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$  cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
````

## Notas adicionales
| comando | descripcion |
|------------|-------------|
	| ls |  lista archivos |
| cat | muestra el contenido de un archivo |
| pwd | muestra el directorio |

## Referencias