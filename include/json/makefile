PROJECT = jsoncpp.a
OBJECTS = jsoncpp.o

LIBS =

# Extensions to clean
CLEANEXTS = o a

INCLUDES =
# define the C compiler to use
CC = clang++

# define any compile-time flags
CFLAGS= -std=c++14 -ggdb -Wall -pedantic

LFLAGS=

all: $(PROJECT)

.cpp.o:
	$(CC) -c $(CFLAGS) $(INCLUDES) $< $(LFLAGS) $(LIBS)

$(PROJECT): $(OBJECTS)
	ar ru $@ $^

.PHONY: clean install
clean:
	for file in $(CLEANEXTS); do rm -f *.$$file; done

install:
	cp *.a ../../lib/
	cp *.h ../../include
