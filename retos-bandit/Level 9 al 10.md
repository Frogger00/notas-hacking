# Bandit Level 9 → 10

## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Datos de acceso a nivel
EN632PlfYiZbn3PhVK3XOGSlNInNE00t

## Solución
```bash
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ file data.txt
data.txt: data
bandit9@bandit:~$ strings data.txt | grep ==
c========== the
h;========== password
========== isT
n.E========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```

## Notas adicionales
| comando | descripcion |
|------------|-------------|
	| ls |  lista archivos |
| cat | muestra el contenido de un archivo |
| cd | moverse entre directorios |
| grep | encontrar patrones |
| string | cadenas en archivos |

## Referencias

