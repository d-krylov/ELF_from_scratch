AS      = as
LD      = ld
CC      = gcc

OBJCOPY = objcopy 
CHMOD   = chmod
RM      = rm

all: printf_with_libdl.out

# Result
printf_with_libdl.out: printf_with_libdl.o
	$(OBJCOPY)  -O binary printf_with_libdl.o printf_with_libdl.out
	$(CHMOD)    +x printf_with_libdl.out

# Object file
printf_with_libdl.o: printf_with_libdl.asm
	$(AS) -a --32 -o printf_with_libdl.o printf_with_libdl.asm

# Preprocessing
printf_with_libdl.asm: 
	$(CC) -E printf_with_libdl.S -o printf_with_libdl.asm

clean:
	$(RM) -rf *.asm *.o *.out  