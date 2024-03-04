# 使用隐式规则 Implicit Rules

world.out: hello.o main.o
	cc -o world.out hello.o main.o

# 自动创建 hello.o 文件的隐式规则:
# hello.o: hello.c
#     cc -c -o hello.o hello.c

# 以及 main.o 文件的隐式规则:
# ...

clean:
	rm -f *.o world.out
