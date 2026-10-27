CC ?= gcc
CFLAGS ?= -Wall -Wextra -O2

INCLUDE_DIR = ../../include
COMMON_LIB = ../../build/lib/libcommon.a

.PHONY: all clean

all: balancer

balancer: main.c router.c $(COMMON_LIB)
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) main.c router.c $(COMMON_LIB) -o balancer

clean:
	rm -f balancer