CC = wla-z80
CFLAGS = -i -o
LD = wlalink
LDFLAGS = -i -d -s

SFILES = test.z80
IFILES = 
OFILES = bm80bios.o
TARGET_DIR = C:\Git\VisualStudio\byte-master-80-emulator\bm80-emulator

all: $(OFILES) makefile
	$(LD) $(LDFLAGS) linkfile bm80bios.bin
	copy bm80bios.bin $(TARGET_DIR)

bm80bios.o: test.z80
	$(CC) $(CFLAGS) bm80bios.o test.z80

$(OFILES): $(HFILES)

clean:
	rm -f $(OFILES) core *~ linked.rom linked.sym
