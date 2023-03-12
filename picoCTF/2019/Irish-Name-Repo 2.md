## Descripcion
There is a website running at `https://jupiter.challenges.picoctf.org/problem/52849/` ([link](https://jupiter.challenges.picoctf.org/problem/52849/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:52849

## Pistas
The password is being filtered.

## Solucion
Inspeccionar la pagina de login para encontrar el elemento oculto y cambiar su valor para inyectar sql en la base de datos del servidor.
Ingresar con: admin' --

## Bandera
picoCTF{m0R3_SQL_plz_fa983901}

## Notas


