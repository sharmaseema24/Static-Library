CC=gcc
EXEC=Test_StaticLib
SRC=main.c
INC_DIR=../include
LIB=../OUT
LDFLAGS=-L$(LIB) -lStatic  #"lib" is automatically prefixed & ".a" is automatically suffixed with this name i.e.Static"
			   
CFLAGS=-I$(INC_DIR)

$(EXEC):$(SRC) $(INC_DIR)/*.h
	$(CC) -o $@ $^  $(CFLAGS) $(LDFLAGS)

