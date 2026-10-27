CC ?= gcc
CFLAGS ?= -Wall -Wextra -O2

INCLUDE_DIR = ../../include
COMMON_LIB = ../../build/lib/libcommon.a

.PHONY: all clean

all: backend

backend: main.c handler.c $(COMMON_LIB)
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) main.c handler.c $(COMMON_LIB) -o backend

clean:
	rm -f backend