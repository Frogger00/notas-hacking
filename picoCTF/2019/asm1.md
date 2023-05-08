## Descripcion
What does asm1(0x8be) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/66c927e32f3d7be7a62d13a7c2250943/test.S)

## Pistas
assembly [conditions](https://www.tutorialspoint.com/assembly_programming/assembly_conditions.htm)

## Solucion
asm1:
	<+0>:	push   ebp --0x8be
	<+1>:	mov    ebp,esp --0x8be
	<+3>:	cmp    DWORD PTR [ebp+0x8],0x71c --MAYOR
	<+10>:	jg     0x512 <asm1+37> --JMP +37
	<+12>:	cmp    DWORD PTR [ebp+0x8],0x6cf
	<+19>:	jne    0x50a <asm1+29>
	<+21>:	mov    eax,DWORD PTR [ebp+0x8]
	<+24>:	add    eax,0x3
	<+27>:	jmp    0x529 <asm1+60>
	<+29>:	mov    eax,DWORD PTR [ebp+0x8]
	<+32>:	sub    eax,0x3
	<+35>:	jmp    0x529 <asm1+60>
	<+37>:	cmp    DWORD PTR [ebp+0x8],0x8be --IGUAL
	<+44>:	jne    0x523 <asm1+54> --NO JMP
	<+46>:	mov    eax,DWORD PTR [ebp+0x8] --eax=0x8be
	<+49>:	sub    eax,0x3 --eax=0x8bb
	<+52>:	jmp    0x529 <asm1+60> --JMP +60
	<+54>:	mov    eax,DWORD PTR [ebp+0x8] 
	<+57>:	add    eax,0x3 
	<+60>:	pop    ebp
	<+61>:	ret    --0x8bb

## Bandera
0x8bb

## Notas




