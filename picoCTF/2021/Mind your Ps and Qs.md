## Descripcion
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/3cfeb09681369c26e3f19d886bc1e5d9/values)

## Pistas
Bits are expensive, I used only a little bit over 100 to save money

## Solucion
Factorizar la n dada con la página http://factordb.com/
Utilizar los valores obtenidos para p y q
Descifrar el mensaje
13016382529449106065927291425342535437996222135352905256639629442503647501498237
Convertir en texto

## Bandera
picoCTF{sma11_N_n0_g0od_45369387}

## Notas

