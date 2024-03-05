OBJS = $(patsubst %.c,%.o,$(wildcard *.c))
TARGET = world.out

$(TARGET): $(OBJS)
	cc -o world.out $(OBJS)

# 模式匹配规则：当make需要规则 xyz.o 时，自动生成一条 xyz.o: xyz.c 规则:
%.o: %.c
	@# 用info打印生成的规则
	$(info pattern rule -> $@: $<)
	cc -c -o $@ $<

clean:
	rm -f *.o $(TARGET)
