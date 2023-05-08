## Descripcion
This vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://jupiter.challenges.picoctf.org/static/834acd392e0964a41f05790655a994b9/VaultDoor4.java)

## Pistas
Use a search engine to find an "ASCII table".
You will also need to know the difference between octal, decimal, and hexadecimal numbers.

## Solucion
Abrir el código fuente y extraer la clave cifrada
106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
Transformar los primeros números decimales a ASCII
jU5t_4_b
0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
Transformar de hexadecimal a ASCII
UnCh_0f_
0142, 0131, 0164, 063 , 0163, 0137, 0146, 064 ,
98, 89, 116, 51, 115, 95, 102, 52
bYt3s_f4
'a' , '8' , 'c' , 'd' , '8' , 'f' , '7' , 'e' ,
Separar los caracteres
a8cd8f7e

## Bandera
picoCTF{jU5t_4_bUnCh_0f_bYt3s_f4a8cd8f7e}

## Notas



