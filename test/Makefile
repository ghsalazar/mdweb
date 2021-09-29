all: hello.c hello.md

hello.c: hello.mdw
	sh ../src/mdtangle -R $@ $< > $@

hello.md: hello.mdw
	sh ../src/mdweave $< > $@

clean:
	rm -f hello.c hello.md
