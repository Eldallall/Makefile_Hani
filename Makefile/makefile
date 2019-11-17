 vpath %.c ./Src
 vpath %.o ./Dependencies/
 vpath %.h ./Inc/
 
SOURCES = ./Src/
HEADERS = ./Inc
OBJECTS = ./Dependencies/
SOURCES_Files = DIO.c LCD.c main.c
OBJ_Files = DIO.o LCD.o main.o code.o
Link_Target = app.exe
CLEAN_TARGET = $(Link_Target) $(OBJECTS)*.o
cc = gcc_S

all : $(OBJ_Files)

clean : 
	rm $(CLEAN_TARGET)
	echo clean file done !
	
%.o : %.c
	$(cc) -c -I$(HEADERS) $< -o $(OBJECTS)$@
	echo generating object file done !

#Compiling
compile : 
	make_S $(OBJ_Files)
	
#Linking The Project
Link:
	make_S $(Link_Target)

$(Link_Target) : $(OBJ_Files)
		$(cc) $(OBJECTS)*.o -o $@
	echo linking file done !