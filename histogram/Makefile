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

histo_locks : histo_locks.o $(UNITFILES)
	$(CC) $(CFLAGS) -o histo_locks histo_locks.o $(UNITFILES) $(LIB)

histo_locks.o : histo_locks.c
	$(CC) $(CFLAGS) -c histo_locks.c $(INCLUDE)


histo_atomic : histo_atomic.o $(UNITFILES)
	$(CC) $(CFLAGS) -o histo_atomic histo_atomic.o $(UNITFILES) $(LIB)

histo_ver2.o : histo_atomic.c
	$(CC) $(CFLAGS) -c histo_atomic.c $(INCLUDE)

histo_creative: histo_creative.o $(UNITFILES)
	$(CC) $(CFLAGS) -o histo_creative histo_creative.o $(UNITFILES) $(LIB)

histo_creative.o : histo_creative.c
	$(CC) $(CFLAGS) -c histo_creative.c $(INCLUDE)
