# 模式规则 Pattern Rules

OBJS = $(patsubst %.c,%.o,$(wildcard *.c))

world.out: $(OBJS)
	$(info OBJS = $(OBJS))
	cc -o world.out $(OBJS)

# 模式匹配规则：当make需要规则 xyz.o 时，自动生成一条 xyz.o: xyz.c 规则:
%.o: %.c
	cc -c -o $(@) $(<)

clean:
	rm -f *.o *.out
