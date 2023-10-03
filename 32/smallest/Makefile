AS      = as
LD      = ld
CC      = gcc

OBJCOPY = objcopy 
CHMOD   = chmod
RM      = rm

all: smallest.out

# Result
smallest.out: smallest.o
	$(OBJCOPY)  -O binary smallest.o smallest.out
	$(CHMOD)    +x smallest.out

# Object file
smallest.o: smallest.asm
	$(AS) -a --32 -o smallest.o smallest.asm

# Preprocessing
smallest.asm: 
	$(CC) -E smallest.S -o smallest.asm

clean:
	$(RM) -rf *.asm *.o *.out  