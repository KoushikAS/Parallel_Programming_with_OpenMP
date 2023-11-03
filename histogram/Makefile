#----- Modify CC and CFLAGS as appropriate in your environment
CC = gcc
CFLAGS = -O3 -fopenmp

LIB = -lm -lc

UNITFILES = 

#------------ EXECUTABLE FILES ---------------

histo : histo.o $(UNITFILES)
	$(CC) $(CFLAGS) -o histo histo.o $(UNITFILES) $(LIB)

clean:
	rm -f histo *.o

histo.o : histo.c
	$(CC) $(CFLAGS) -c histo.c $(INCLUDE) 

histo_ver1 : histo_ver1.o $(UNITFILES)
	$(CC) $(CFLAGS) -o histo_ver1 histo_ver1.o $(UNITFILES) $(LIB)

histo_ver1.o : histo_ver1.c
	$(CC) $(CFLAGS) -c histo_ver1.c $(INCLUDE)
