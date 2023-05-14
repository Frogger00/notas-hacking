## Descripcion
Can you solve this?What two positive numbers can make this possible: `n1 > n1 + n2 OR n2 > n1 + n2`
Enter them here `nc saturn.picoctf.net 58306`. [Source](https://artifacts.picoctf.net/c/456/flag.c

## Pistas
Integer overflow
Not necessarily a math problem

## Solucion
Al inspeccionar el código se puede observar que los números son enteros
Si se interoduce el mayor valor posibloe para un entero y el número 1 se desborda el entero
De esta forma se puede cumplir el problema
```bash
frogger00-picoctf@webshell:~$ nc saturn.picoctf.net 58306
n1 > n1 + n2 OR n2 > n1 + n2 
What two positive numbers can make this possible: 
1
2147483647
You entered 1 and 2147483647
You have an integer overflow
YOUR FLAG IS: picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_ccd078bd}
```

## Bandera


## Notas




