## Descripcion
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.

## Pistas
Try using a tool like Wireshark.
How can you decrypt the TLS stream?

## Solucion
El flujo de paquetes está encriptado
Utilizar el siguiente comando para desencriptar el flujo con la llave y guardar el resultado en un archivo
```bash
ssldump -r capture.pcap -k picopico.key -d > output
```
Buscar la bandera en el archivo obtenido

## Bandera
picoCTF{honey.roasted.peanuts}

## Notas



