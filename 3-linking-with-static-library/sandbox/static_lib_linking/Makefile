lib_objects: $(wildcard lib/*.c)
	for file in $^; do clang -c $$file -o $$file.o; done

lib.a: lib_objects
	ar -rcs lib.a lib/*.o

main.o:
	clang -c main.c -o main.o

link: lib.a main.o
	ld -lSystem main.o lib.a lib/sum.c.o 
