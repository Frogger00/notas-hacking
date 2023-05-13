## Descripcion
The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/f9abc386dfb1309e687344783f208b20/need-for-speed).

## Pistas
What is the final key?

## Solucion
```bash
chmod +x need-for-speed
gdb need-for-speed
set disassembly-flavor intel
disassemble main
break main
info breakpoints
run
disassemble main
call (int) get_key()
call (int) print_flag()
```

## Bandera
PICOCTF{Good job keeping bus #190ca38b speeding along!}

## Notas



