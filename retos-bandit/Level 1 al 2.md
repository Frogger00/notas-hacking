# Bandit Level 1 → 2

## Objetivo
The password for the next level is stored in a file called - located in the home directory.

## Datos de acceso a nivel
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

## Solución
````bash
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ whoami
bandit1
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
````

## Notas adicionales
| comando | descripcion |
|------------|-------------|
	| ls |  lista archivos |
| cat | muestra el contenido de un archivo |
| pwd | muestra el directorio |
| whoami | muestra el usuario actual |

## Referencias
