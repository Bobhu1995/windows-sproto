
LUADIR = ..\lua5.4\src
DLLDIR = ..\lua5.4

mingw: lsocket.dll
# gcc -o lsocket.dll -Wall -O2  -I/usr/local/include lsocket.c win_compat.c -shared  -lws2_32 -L/usr/local/bin -llua53
lsocket.dll : lsocket.c win_compat.c
	gcc -o lsocket.dll -Wall -O2  lsocket.c win_compat.c -shared -lws2_32 -I$(LUADIR) -L$(DLLDIR) -llua54

clean:
	del *.o *.dll