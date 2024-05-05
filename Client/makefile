compile: ../open62541/open62541.o obj/myClient.o bin/myClient
	gcc ../open62541/open62541.o obj/myClient.o -o bin/myClient

../open62541/open62541.o: ../open62541/open62541.c
	gcc -c -std=c99 ../open62541/open62541.c -o ../open62541/obj/open62541.o

obj/myClient.o: src/myClient.c
	gcc -c src/myClient.c -I ../open62541 -o obj/myClient.o

clean:
	rm *.o myClient

run: compile
	./bin/myClient
