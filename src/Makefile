CXXFLAGS= -O3 -fomit-frame-pointer -ffast-math -std=c++17
override CXXFLAGS+= -Wall -fsigned-char -fno-exceptions -fno-rtti

all: tessfont

tessfont: tessfont.o
	g++ $(CXXFLAGS) -o tessfont tessfont.o `freetype-config --libs` -lz

tessfont.o: tessfont.c
	g++ $(CXXFLAGS) -c -o $@ $< `freetype-config --cflags`

clean:
		rm tessfont tessfont.o



