OBJS = $(patsubst %.c,%.o,$(wildcard *.c))
TARGET = world.out

$(TARGET): $(OBJS)
	cc -o $(TARGET) $(OBJS)

# 模式匹配规则：当make需要目标 xyz.o 时，自动生成一条 xyz.o: xyz.c 规则:
%.o: %.c
	@echo 'compiling $<...'
	cc -c -o $@ $<

clean:
	rm -f *.o $(TARGET)
