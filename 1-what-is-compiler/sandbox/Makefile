preprocessing: 
	clang -E main.c > main.i

compiling: preprocessing
	clang -S main.i -o main.s

assemble: compiling
	as main.s -o main.o

linking: assemble
	ld main.o -lSystem

all:
	clang main.c
