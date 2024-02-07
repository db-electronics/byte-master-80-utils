CC = wla-z80
CFLAGS = -i -o
LD = wlalink
LDFLAGS = -i -d -s

SFILES = test.z80
IFILES = 
OFILES = test.o

all: $(OFILES) makefile
	$(LD) $(LDFLAGS) linkfile test.bin

test.o: test.z80
	$(CC) $(CFLAGS) test.o test.z80

$(OFILES): $(HFILES)

clean:
	rm -f $(OFILES) core *~ linked.rom linked.sym
