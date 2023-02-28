# Bandit Level 3 → 4

## Objetivo
The password for the next level is stored in a hidden file in the inhere directory.

## Datos de acceso a nivel
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

## Solución
````bash
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ pwd
/home/bandit3
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ find
.
./.hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
````

## Notas adicionales
| comando | descripcion |
|------------|-------------|
	| ls |  lista archivos |
| cat | muestra el contenido de un archivo |
| pwd | muestra el directorio |
| cd | moverse entre directorios |

## Referencias
