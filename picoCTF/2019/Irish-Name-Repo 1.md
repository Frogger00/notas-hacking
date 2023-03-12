## Descripcion
There is a website running at `https://jupiter.challenges.picoctf.org/problem/39720/` ([link](https://jupiter.challenges.picoctf.org/problem/39720/)) or http://jupiter.challenges.picoctf.org:39720. Do you think you can log us in? Try to see if you can login!

## Pistas
There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
Try to think about how the website verifies your login.

## Solucion
Inspeccionar la pagina de login para encontrar el elemento oculto y cambiar su valor para inyectar sql en la base de datos del servidor.
Ingresar con: ' or '1'='1

## Bandera
picoCTF{s0m3_SQL_c218b685}

## Notas


