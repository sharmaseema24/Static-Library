CC=gcc
SRC=$(wildcard *.c)
OBJ=$(SRC:.c=.o)
EXEC=libStatic.a
INC_DIR=../include
OUT_DIR=../OUT
CFLAGS=-I$(INC_DIR)


all:  dir $(OUT_DIR)/$(OBJ) $(OUT_DIR)/$(EXEC)

$(OUT_DIR)/$(OBJ): $(SRC) $(INC_DIR)/*.h
	$(CC) -c -o $@ $< $(CFLAGS)

$(OUT_DIR)/$(EXEC): $(OUT_DIR)/$(OBJ)
	ar rc $@ $^ && ranlib $@ 

dir:
	@mkdir -p $(OUT_DIR)

clean:
	rm -rf $(OUT_DIR)/*.o

run: $(OUT_DIR)/$(EXEC)
	./$(OUT_DIR)/$(EXEC)
