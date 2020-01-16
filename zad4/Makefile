all: myProgram

myProgram: main.o employee.o address.o
	g++ main.o employee.o address.o -o myProgram

main.o: main.cpp address.h employee.h
	g++ -c main.cpp

employee.o: employee.cpp address.h
	g++ -c employee.cpp

address.o: address.cpp
	g++ -c address.cpp

.PHONY: clean

clean:
	rm -rf *.o myProgram
