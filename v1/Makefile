# 第一条规则是默认执行规则 x: m, c
x.txt: m.txt c.txt
	cat m.txt c.txt > x.txt

# m: a, b
m.txt: a.txt b.txt
	cat a.txt b.txt > m.txt

clean:
	rm -f m.txt
	rm -f x.txt

cd:
	pwd
	cd ..
	pwd

cd_ok:
	pwd; \
	cd ..; \
	pwd

no_output:
	@echo 'not display'
	echo 'will display'

has_error:
	rm zzz.txt
	echo 'ok'

ignore_error:
	-rm zzz.txt
	echo 'ok'
