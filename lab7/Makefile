CC=gcc
FLAGS=-std=c99 -pedantic -Wall -lm -g
BIN=race-game
SOURCE=lab07.c
INPUT_PATH=input
OUTPUT_PATH=output

build:
	$(CC) $(SOURCE) $(FLAGS) -o $(BIN)

run:build
	./$(BIN) < $(INPUT_PATH)/arq1.in > $(OUTPUT_PATH)/arq1.out
	./$(BIN) < $(INPUT_PATH)/arq2.in > $(OUTPUT_PATH)/arq2.out
	./$(BIN) < $(INPUT_PATH)/arq3.in > $(OUTPUT_PATH)/arq3.out
	./$(BIN) < $(INPUT_PATH)/arq4.in > $(OUTPUT_PATH)/arq4.out
	./$(BIN) < $(INPUT_PATH)/arq5.in > $(OUTPUT_PATH)/arq5.out

test:build
	./$(BIN) < $(INPUT_PATH)/arq1.in > $(OUTPUT_PATH)/arq1.out
	diff -s $(OUTPUT_PATH)/arq1.out $(OUTPUT_PATH)/arq1.res
	./$(BIN) < $(INPUT_PATH)/arq2.in > $(OUTPUT_PATH)/arq2.out
	diff -s $(OUTPUT_PATH)/arq2.out $(OUTPUT_PATH)/arq2.res
	./$(BIN) < $(INPUT_PATH)/arq3.in > $(OUTPUT_PATH)/arq3.out
	diff -s $(OUTPUT_PATH)/arq3.out $(OUTPUT_PATH)/arq3.res
	./$(BIN) < $(INPUT_PATH)/arq4.in > $(OUTPUT_PATH)/arq4.out
	diff -s $(OUTPUT_PATH)/arq4.out $(OUTPUT_PATH)/arq4.res
	./$(BIN) < $(INPUT_PATH)/arq5.in > $(OUTPUT_PATH)/arq5.out
	diff -s $(OUTPUT_PATH)/arq5.out $(OUTPUT_PATH)/arq5.res

valgrind:build
	valgrind --tool=memcheck --leak-check=yes --show-reachable=yes ./$(BIN) < $(INPUT_PATH)/arq1.in > $(OUTPUT_PATH)/arq1.out
	valgrind --tool=memcheck --leak-check=yes --show-reachable=yes ./$(BIN) < $(INPUT_PATH)/arq2.in > $(OUTPUT_PATH)/arq2.out
	valgrind --tool=memcheck --leak-check=yes --show-reachable=yes ./$(BIN) < $(INPUT_PATH)/arq3.in > $(OUTPUT_PATH)/arq3.out
	valgrind --tool=memcheck --leak-check=yes --show-reachable=yes ./$(BIN) < $(INPUT_PATH)/arq4.in > $(OUTPUT_PATH)/arq4.out
	valgrind --tool=memcheck --leak-check=yes --show-reachable=yes ./$(BIN) < $(INPUT_PATH)/arq5.in > $(OUTPUT_PATH)/arq5.out
