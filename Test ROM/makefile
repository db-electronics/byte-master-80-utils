CC = wla-z80
CFLAGS = -i -o
LD = wlalink
LDFLAGS = -i -d -s

SFILES = test.z80
IFILES = 
OFILES = bm80bios.o

# Read TARGET_DIR from target_dir.txt file, make sure it's the only line in that file
TARGET_DIR_FILE := target_dir.txt
TARGET_DIR := $(file < $(TARGET_DIR_FILE))

all: $(OFILES) makefile
	$(LD) $(LDFLAGS) linkfile bm80bios.bin
	copy bm80bios.bin $(TARGET_DIR)

bm80bios.o: test.z80
	$(CC) $(CFLAGS) bm80bios.o test.z80

$(OFILES): $(HFILES)

clean:
	rm -f $(OFILES) core *~ linked.rom linked.sym
