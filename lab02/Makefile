LAB_BUILD_DIR=$(BUILD_DIR)/lab02
INCLUDE_DIR=./include
BINARY=$(LAB_BUILD_DIR)/lab02

CFLAGS=-c -std=c99 -Wall -Wextra -pedantic-errors -I$(INCLUDE_DIR)

ifeq ($(BUILD_TYPE), release)
	CFLAGS:=$(CFLAGS) -O2
endif

ifeq ($(BUILD_TYPE), debug)
	CFLAGS:=$(CFLAGS) -ggdb3 -O1
endif

SOURCES=src/main.c src/vector.c src/file.c \
		src/error.c
OBJECTS=$(patsubst src/%.c, $(LAB_BUILD_DIR)/%.o,$(SOURCES))

$(BINARY): dir $(OBJECTS)
	$(CC) $(OBJECTS) -o $(BINARY)

$(OBJECTS): $(LAB_BUILD_DIR)/%.o: src/%.c
	$(CC) $(CFLAGS) $< -o $@

dir:
	@mkdir -p "$(LAB_BUILD_DIR)"

clean:
	@rm -f $(OBJECTS) $(BINARY)
	@make BUILD_DIR=$(BUILD_DIR) --directory=report clean

test: $(BINARY)
	@bash ./run_tests.sh $(BINARY)

report:
	@make BUILD_DIR=$(BUILD_DIR) --directory=report

.PHONY: clean test report
