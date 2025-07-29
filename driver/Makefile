CFLAGS += -m32 -Wall -fno-stack-protector -fno-builtin -Wno-error=address-of-packed-member -Wno-address
OBJ = tty.o ramdisk.o pci.o hd.o pata.o ahci.o tty_ld.o console.o 8139.o eth.o

all: $(OBJ) 
	
	
%.o: %.c
	$(CC) $(CFLAGS) -o $@ -c $<
		
clean:
	rm -f $(OBJ)

include Makefile.dep

dep:
	gcc -M -iquote../include *.c   > Makefile.dep
	
