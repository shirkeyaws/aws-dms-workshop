# Makefile
# 
# Converts Markdown to other formats (HTML, PDF, DOCX, RTF, ODT, EPUB) using Pandoc
# <http://johnmacfarlane.net/pandoc/>
#
# Run "make" (or "make all") to convert to all other formats
#
# Run "make clean" to delete converted files

# Convert all files in this directory that have a .md suffix
SOURCE_DOCS := index.md

EXPORTED_DOCS=\
 $(SOURCE_DOCS:.md=.pdf)

RM=/bin/rm -f

PANDOC=/usr/bin/env pandoc

PANDOC_OPTIONS=--smart --standalone  --latex-engine=xelatex --filter pandoc-include

PANDOC_PDF_OPTIONS=--template ../shared/default.latex

# Pattern-matching Rules
%.pdf : %.md
	$(PANDOC) $(PANDOC_OPTIONS) $(PANDOC_PDF_OPTIONS) -o $@ $<

# Targets and dependencies

.PHONY: all clean

all : clean $(EXPORTED_DOCS)
	- mv $(EXPORTED_DOCS) ../../bucket/runbook_nosql_mongodb_dynamodb.pdf
	- pushd ../../bucket/ && make all && popd

clean:
	- $(RM) $(EXPORTED_DOCS)
