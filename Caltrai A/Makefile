# Default to debugging flags. Set to -O3 if you want optimisations
# (either change it here, or type 'make CFLAGS=-O3' in the shell).
CFLAGS?=-g -Wall -Wno-unused-value

all: caltrain reaction

caltrain: caltrain-runner.c caltrain.c pintos_thread.h
	$(CC) $(CFLAGS) -o caltrain caltrain-runner.c -lpthread 

reaction: reaction-runner.c reaction.c pintos_thread.h
	$(CC) $(CFLAGS) -o reaction reaction-runner.c -lpthread 

run: caltrain reaction
	./caltrain
	./caltrain
	./caltrain

clean:
	$(RM) caltrain reaction
	$(RM) -r *.dSYM
