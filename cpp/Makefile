CFLAGS = -Wall -Wextra -Werror -g \
         -std=c++11 -O3 -L. -I.. \
         $(shell root-config --cflags)

LIBS = $(shell root-config --libs)

EXE = bblocks

$(EXE) : $(EXE).cc bayesian_blocks.cc
	$(CXX) $(CFLAGS) -o $@ $^ $(LIBS)

clean :
	rm -f bblocker

install : $(EXE)
	mkdir -p $(PREFIX)/bin
	cp $(EXE) $(PREFIX)/bin

.PHONY : install clean
