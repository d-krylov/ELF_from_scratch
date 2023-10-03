AS      = as
LD      = ld
CC      = gcc

OBJCOPY = objcopy 
CHMOD   = chmod
RM      = rm

all: printf.out

# Result
printf.out: printf.o
	$(OBJCOPY)  -O binary printf.o printf.out
	$(CHMOD)    +x printf.out

# Object file
printf.o: printf.asm
	$(AS) -a --32 -o printf.o printf.asm

# Preprocessing
printf.asm: 
	$(CC) -E printf.S -o printf.asm

clean:
	$(RM) -rf *.asm *.o *.out  