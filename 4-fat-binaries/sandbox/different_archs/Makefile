main.arm.s: main.c
	clang -S main.c -arch armv7 -o main.arm.s

main.x86_64.s: main.c
	clang -S main.c -o main.x86_64.s

main.arm.o: main.c
	clang -c main.c -arch armv7 -o main.arm.o

main.x86_64.o: main.c
	clang -c main.c -o main.x86_64.o
