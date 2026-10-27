CC ?= gcc
CFLAGS ?= -Wall -Wextra -O2

INCLUDE_DIR = ../include
LIB_DIR = ../build/lib
TARGET = $(LIB_DIR)/libcommon.a

.PHONY: all clean

all: $(TARGET)

$(TARGET): net.c http.c utils.c
	mkdir -p $(LIB_DIR)
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c net.c http.c utils.c
	ar rcs $(TARGET) net.o http.o utils.o

clean:
	rm -f net.o http.o utils.o $(TARGET)