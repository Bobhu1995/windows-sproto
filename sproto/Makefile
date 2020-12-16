.PHONY : all win clean

all : linux
win : sproto.dll

LUADIR = ..\lua5.4\src
DLLDIR = ..\lua5.4

# For Linux
linux:
	make sproto.so "DLLFLAGS = -shared -fPIC"
# For Mac OS
macosx:
	make sproto.so "DLLFLAGS = -bundle -undefined dynamic_lookup"

sproto.so : sproto.c lsproto.c
	env gcc -O2 -Wall $(DLLFLAGS) -o $@ $^

sproto.dll : sproto.c lsproto.c
	gcc -O2 -Wall --shared -fPIC -o $@ $^  -I$(LUADIR) -L$(DLLDIR) -llua54

clean :
	del sproto.dll
