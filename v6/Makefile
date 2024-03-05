# 列出所有 .c 文件:
SRCS = $(wildcard *.c)

# 根据SRCS生成 .o 文件列表:
OBJS = $(SRCS:.c=.o)

# 根据SRCS生成 .d 文件列表:
DEPS = $(SRCS:.c=.d)

TARGET = world.out

# 默认目标:
$(TARGET): $(OBJS)
	cc -o $@ $^

# xyz.d 的规则由 xyz.c 生成:
%.d: %.c
	rm -f $@; \
	cc -MM $< >$@.tmp; \
	sed 's,\($*\)\.o[ :]*,\1.o $@ : ,g' < $@.tmp > $@; \
	rm -f $@.tmp

# 模式规则:
%.o: %.c
	$(CC) -c -o $@ $<

clean:
	rm -rf *.o *.d $(TARGET)

# 引入所有 .d 文件:
include $(DEPS)
