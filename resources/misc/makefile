SRC := $(filter-out header.md, $(wildcard *.md))
BINS := $(patsubst %.md,%.pdf,$(SRC))
OUT_DIR := out/

all: $(BINS)

out_dir:
	mkdir -p $(OUT_DIR)

clean:
	rm -rf $(OUT_DIR)

.INTERMEDIATE: $(notdir $(BINS))
.DELETE_ON_ERROR:

%.pdf: %.md out_dir
	pandoc -s header.md $< -o $(OUT_DIR)$@
