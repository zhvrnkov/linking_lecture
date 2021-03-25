input=main

compile:
	clang -c $(input).c

assembly_code:
	clang -S $(input).c -o $(input).s

object_file:
	clang -c $(input).c -o $(input).o

compile_lib:
	clang -c lib/lib.c

linking: object_file compile_lib
	ld -lSystem $(input).o lib.o -o $(input)
