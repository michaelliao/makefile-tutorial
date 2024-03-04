# 默认目标:
all: world.out

# 列出所有 .c 文件:
SRCS = $(wildcard *.c)

# 根据SRCS生成 .o 文件列表:
OBJS = $(SRCS:.c=.o)

# xyz.d 的规则由 xyz.c 生成:
%.d: %.c
	rm -f $(@); \
	cc -MM $(<) >$(@).tmp; \
	sed 's,\($(*)\)\.o[ :]*,\1.o $(@) : ,g' < $(@).tmp > $(@); \
	rm -f $(@).tmp

world.out: $(OBJS)
	cc -o world.out $(OBJS)

clean:
	rm -rf *.o *.d *.out

# 引入所有 .d 文件:
include $(SRCS:.c=.d)
