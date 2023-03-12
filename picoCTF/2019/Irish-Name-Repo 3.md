## Descripcion
There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/29132/` ([link](https://jupiter.challenges.picoctf.org/problem/29132/)) or http://jupiter.challenges.picoctf.org:29132. Try to see if you can login as admin!

## Pistas
Seems like the password is encrypted.

## Solucion
Inspeccionar la pagina de login para encontrar el elemento oculto y cambiar su valor para inyectar sql en la base de datos del servidor.
Se observa la contrasena ingresada en rot13.
Se inyecta el SQL en rot13.
Ingresar con: ' be '1'='1.

## Bandera
picoCTF{3v3n_m0r3_SQL_06a9db19}

## Notas


