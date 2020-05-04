OUTPUT = build
CC = gcc
SRC = $(wildcard *.c)
S_SRCS = main.c\
	 hello.c\
	 goodbye.c
OBJS = $(SRC:.c=.o)



all: main
.c.o:
	@echo "$(OBJS)"
	$(CC) -c -o $@ $^  
main: $(OBJS)
	mkdir $(OUTPUT)
	$(CC) -o $(OUTPUT)/main $(OBJS)
clean:
	rm $(wildcard *.o)
	rm -r $(OUTPUT)
run:
	./$(addprefix $(OUTPUT)/,main)
