#Archivo makefile simple

PROYECTO = muestreo
DESTDIR = /usr/local/bin
CFLAGS = -Wall
LDFLAGS = -lm
CC=gcc
OBJETOS:= $(patsubst %.c, %.o, $(wildcard *.c)) 

all: $(PROYECTO)

%.o: %.c
	$(CC) -c $< $(CFLAGS)

$(PROYECTO):  $(OBJETOS)
	$(CC) $^ -o $@ $(LDFLAGS)

.PHONY: clean

install: all
	if [ ! -d $(DESTDIR) ]; then \
     		sudo mkdir $(DESTDIR); \
		fi; \
		sudo cp $(PROYECTO) $(DESTDIR)

uninstall: 
	sudo rm $(DESTDIR)\$(PROYECTO)


clean: 
	rm -f *.o $(PROYECTO)

