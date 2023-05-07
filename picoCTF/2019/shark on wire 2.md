## Descripcion
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

## Pistas
(None)

## Solucion
Filtrar los paquetes UDP del puerto 22
Utilizar las cabeceras de los paquetes para obtener un código
112 105 99 111 67 84 70 123 112 49 76 76 102 51 114 51 100 95 100 97 116 97 95 118 49 97 95 115 116 51 103 48 125
Convertir el código a decimal para obtener la bandera

## Bandera
picoCTF{p1LLf3r3d_data_v1a_st3g0}

## Notas



