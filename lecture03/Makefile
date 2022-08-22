SOURCE=		hello.c hello-asm.s
TARGET=		hello hello-asm

all:		$(TARGET)

%:		%.c
	gcc -g -gdwarf-2 -std=gnu99 -Wall -o $@ $<

%:		%.s
	as -o $@.o $<
	ld -o $@ -e main $@.o 

clean:
	rm -f $(TARGET) *.o
