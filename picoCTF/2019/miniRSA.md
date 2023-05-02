## Descripcion
Let's decrypt this: [ciphertext](https://jupiter.challenges.picoctf.org/static/eb5e6df8e14c52873cf88c582a1a4008/ciphertext)? Something seems a bit small.

## Pistas
RSA [tutorial](https://en.wikipedia.org/wiki/RSA_(cryptosystem))
How could having too small an e affect the security of this 2048 bit key?
Make sure you don't lose precision, the numbers are pretty big (besides the e value)

## Solucion
Despejar la solución con las formulas de RSA
m = raiz cubica de c
c = 2205316413931134031074603746928247799030155221252519872650080519263755075355825243327515211479747536697517688468095325517209911688684309894900992899707504087647575997847717180766377832435022794675332132906451858990782325436498952049751141

m = mpz(13016382529449106065894479374027604750406953699090365388203722801043052339225981)

Convertir a texto

## Bandera
picoCTF{n33d_a_lArg3r_e_d0cd6eae}'

## Notas



