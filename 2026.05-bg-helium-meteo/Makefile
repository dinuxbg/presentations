# Build rules for the presentations.

TARGETS_DOCS=$(wildcard *.latex)

# What to build.
TARGETS=$(patsubst %.latex,%.pdf,$(TARGETS_DOCS))

# --------------------------------------------------------------------------
# Do not modify below this line.

OUT=out

all: $(TARGETS)

$(OUT):
	mkdir $(OUT)

%.pdf: %.latex | Makefile $(OUT)
	lualatex --shell-escape -output-directory=$(OUT) $^
	lualatex --shell-escape -output-directory=$(OUT) $^
	mv $(OUT)/$@ $@

clean:
	rm -fr $(OUT)
	rm -fr $(TARGETS)
