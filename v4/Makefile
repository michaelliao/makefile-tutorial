# 变量 Variables

# 手动定义的 hello.o main.o
# OBJS = hello.o main.o
# 变成根据当前列出的*.c自动替换为*.o
OBJS = $(patsubst %.c,%.o,$(wildcard *.c))
TARGET = world.out

$(TARGET): $(OBJS)
	$(info OBJS = $(OBJS))
	cc -o $(TARGET) $(OBJS)

hello.o: hello.c
	cc -c hello.c

main.o: main.c hello.h
	cc -c main.c

clean:
	rm -f *.o $(TARGET)
