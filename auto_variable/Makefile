all:main
main: $(wildcard *.o)
	gcc -o main $(wildcard *.o)
%.o:%.c
	gcc -c -o $@ $^
main1.o:main.c hello.c goodbye.c
	@echo "$@ $^"
	@echo "$<"
	@echo "$?"
	@echo "$*"
	@echo "$+"
	@echo "$|"
