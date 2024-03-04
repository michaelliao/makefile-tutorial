# 使用隐式规则 Implicit Rules

world.out: hello.o main.o
	cc -o world.out hello.o main.o

# 自动创建 .o 文件的隐式规则:
# xyz.o: xyz.c
#     cc -c -o xyz.o xyz.c

clean:
	rm -f *.o *.out
