INCLUDE_DIRS = 
LIB_DIRS = 
CC=gcc

CDEFS=
CFLAGS= -O0 -g $(INCLUDE_DIRS) $(CDEFS)
LIBS= -lrt

HFILES= capture.h  
CFILES= seqgenex0.c capture.c

SRCS= ${HFILES} ${CFILES}
OBJS= ${CFILES:.c=.o}

all:	seqgenex0 

clean:
	-rm -f *.o *.d *.ppm *.pgm
	-rm -f seqgenex0 seqgen seqgen2 clock_times

seqgenex0: ${OBJS}
	$(CC) $(LDFLAGS) $(CFLAGS) -o $@  *.o -lpthread -lrt  ${HFILES}

depend:

.c.o:
	$(CC) $(CFLAGS) -c $<
