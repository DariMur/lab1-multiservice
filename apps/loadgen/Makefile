CC ?= gcc
CFLAGS ?= -Wall -Wextra -O2

INCLUDE_DIR = ../../include
COMMON_LIB = ../../build/lib/libcommon.a

.PHONY: all clean

all: loadgen

loadgen: main.c stats.c $(COMMON_LIB)
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) main.c stats.c $(COMMON_LIB) -o loadgen

clean:
	rm -f loadgen