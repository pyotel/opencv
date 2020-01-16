CXX ?= g++

CXXFLAGS += -c -Wall $(shell pkg-config --cflags opencv)
LDFLAGS += $(shell pkg-config --libs opencv)

all: matchmethod

matchmethod: matchmethod_orb_akaze_brisk.o; $(CXX) $< -o $@ $(LDFLAGS)

%.o: %.cpp; $(CXX) $< -o $@ $(CXXFLAGS)

clean: ; rm -f matchmethod_orb_akaze_brisk.o matchmethod
