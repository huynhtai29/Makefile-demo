OUTPUT = build
DIR = $(abspath ./)
CC = gcc

INC = $(addprefix ./,inc)
SRC = $(addprefix ./,src)
S_SRC = $(wildcard $(SRC)/*.c)
S_INC = $(wildcard $(INC)/*.h)
OBJS = $(S_SRC:.c=.o)

LIB = $(OUTPUT)/libbasic.a

all: proj lib main
%.o : %.c
	$(CC) -c -o $@ $^ -I$(INC)  
lib:$(OBJS)
	ar rs $(LIB) $(OBJS)
main:
	$(CC) -o $(OUTPUT)/main main.c  $(LIB) -I$(INC)
proj: 
	mkdir $(OUTPUT)
clean:
	rm $(OBJS)
	rm -r $(OUTPUT)
run:
	./$(addprefix $(OUTPUT)/,main)
