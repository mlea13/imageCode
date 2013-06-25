CC=g++

# compile flags
CFLAGS=-g -Wall

# OpenCV Related
OCVFLAGS=`pkg-config --cflags opencv`
OCVLIBS=`pkg-config --libs opencv`

OBJECTS=FastMatchTemplate.o main.o

PROGRAM=FastMatchTemplate

program: $(OBJECTS)
	$(CC) $(OBJECTS) -o $(PROGRAM) $(OCVLIBS)
  
FastMatchTemplate.o: FastMatchTemplate.cpp FastMatchTemplate.h
	$(CC) -c $(CFLAGS) $(OCVFLAGS) FastMatchTemplate.cpp

main.o: main.cpp
	$(CC) -c $(CFLAGS) $(OCVFLAGS) main.cpp

clean:
	rm -f *o
	rm -f $(PROGRAM)
	rm -f *~
