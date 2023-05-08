## Descripcion
This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://jupiter.challenges.picoctf.org/static/a4018cec1446761cb2e8cce05db925fa/VaultDoor3.java)

## Pistas
Make a table that contains each value of the loop variables and the corresponding buffer index that it writes to.

## Solucion
Abrir el código fuente
La clave es de 32 caracteres
Se obtiene esta cadena: jU5t_a_sna_3lpm1 2g94c_u_4_m7ra41
El primer ciclo toma los primeros 8 caracteres: jU5t_a_s
El segundo ciclo toma los siguientes 8 caracteres y los invierte: 1mpl3_an
El tercer ciclo ordena 8 de los ultimos 16 caracteres: 29cu4mr 
El cuarto ciclo ordena los 8 caracteres faltantes: g4___7a1
jU5t_a_s1mpl3_an 4gr4m_4_u_c79a21

## Bandera
picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_c79a21}

## Notas



