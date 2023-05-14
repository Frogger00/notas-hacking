## Descripcion
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message.Download the corrupted message [here](https://artifacts.picoctf.net/c/192/message.txt).

## Pistas
Split the message up into blocks of 3 and see how the first block is scrambled

## Solucion
Abrir el mensaje corrupto
heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V091B0AE}2

Separar en bloques de 3 letras
heT fl  g a s i icp CTo {7F 4NR P05 1N5 _16 _35 P3X 51N 3_V 091 B0A E}2

Se puede observar un patrón en las letras
En cada bloque poner la última letra en la primer posición
The flag is picoCTF{7R4N5P051N6_15_3XP3N51V3_109AB02E}

## Bandera
picoCTF{7R4N5P051N6_15_3XP3N51V3_109AB02E}

## Notas




