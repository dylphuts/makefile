# Dylan Hutson
# File: Makefile
# Last Modified: 9/12/2024
# To handle compilation for multiple files with only the make command

# The compiler
CC=g++

# Compile with all errors and warnings 
CFLAGS= -g -Wall -Wextra

# The exicutable to be made and ran
TARGET= employee

all:$(TARGET)

$(TARGET): main.o Employee.o Officer.o Supervisor.o
	$(CC) $(CFLAGS) -o $(TARGET) main.o Employee.o Officer.o Supervisor.o

main.o: main.cpp Employee.h Officer.h Supervisor.h 
	$(CC) $(CFLAGS) -c main.cpp

Employee.o: Employee.cpp Employee.h
	$(CC) $(CFLAGS) -c Employee.cpp

Officer.o: Officer.cpp Officer.h
	$(CC) $(CFLAGS) -c Officer.cpp

Supervisor.o: Supervisor.cpp Supervisor.h
	$(CC) $(CFLAGS) -c Supervisor.cpp

clean:
	$(RM) $(TARGET) *.o *~
