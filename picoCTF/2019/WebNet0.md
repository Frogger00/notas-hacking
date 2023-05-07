## Descripcion
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

## Pistas
Try using a tool like Wireshark.
How can you decrypt the TLS stream?

## Solucion
El flujo de paquetes está encriptado
Utilizar el siguiente comando para desencriptar el flujo con la llave
```bash
ssldump -r capture.pcap -k picopico.key -d
```
Buscar la bandera en el resultado

## Bandera
picoCTF{nongshim.shrimp.crackers}

## Notas



