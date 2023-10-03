AS      = as
LD      = ld
CC      = gcc

OBJCOPY = objcopy 
CHMOD   = chmod
RM      = rm

all: small.out

# Result
small.out: small.o
	$(OBJCOPY)  -O binary small.o small.out
	$(CHMOD)    +x small.out

# Object file
small.o: small.asm
	$(AS) -a --64 -o small.o small.asm

# Preprocessing
small.asm: 
	$(CC) -E small.S -o small.asm

clean:
	$(RM) -rf *.asm *.o *.out  