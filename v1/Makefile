# 第一条规则是默认执行规则:
x.txt: m.txt c.txt
	cat m.txt c.txt > x.txt

m.txt: a.txt b.txt
	cat a.txt b.txt > m.txt

# clean 是一个伪目标:
clean:
	rm -f m.txt
	rm -f x.txt

# 多条命令是独立Shell执行的:
cd:
	pwd
	cd ..
	pwd

# 用 ; 分隔多条命令在一个Shell执行:
cd_ok:
	pwd; \
	cd ..; \
	pwd

# 用 @ 控制不打印命令本身:
no_output:
	@echo 'not display'
	echo 'will display'

# 执行出错后中断:
has_error:
	rm zzz.txt
	echo 'ok'

# 执行出错后忽略错误继续执行:
ignore_error:
	-rm zzz.txt
	echo 'ok'
