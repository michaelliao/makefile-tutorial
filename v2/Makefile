# 编译C程序

world.out: hello.o main.o
	cc -o world.out hello.o main.o

hello.o: hello.c
	cc -c hello.c

main.o: main.c hello.h
	cc -c main.c

clean:
	rm -f *.o *.out
