# 生成可执行文件:
world.out: hello.o main.o
	cc -o world.out hello.o main.o

# 编译 hello.c:
hello.o: hello.c
	cc -c hello.c

# 编译 main.c:
main.o: main.c hello.h
	cc -c main.c

clean:
	rm -f *.o world.out
