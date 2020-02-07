CXX ?= g++

CXXFLAGS += -c -Wall $(shell pkg-config --cflags opencv)
LDFLAGS += $(shell pkg-config --libs opencv)
OBJS = matchmethod_orb_akaze_brisk.o
TARGET = matchmethod_orb_akaze_brisk

all: $(TARGET)

$(TARGET): $(OBJS); $(CXX) $< -o $@ $(LDFLAGS)
%.o: %.cpp; $(CXX) $< -o $@ $(CXXFLAGS)

clean:
	rm -f *.o
	rm -f $(TARGET)







