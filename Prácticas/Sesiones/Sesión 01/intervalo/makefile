# Makefile para prácticas de MP
# ESTE MAKEFILE CREA UNA LIBRERÍA
# Autor: Miguel Ángel Fernández Gutiérrez

# Uso del makefile:
# 	make nombre_ejecutable nombre_main
#		nombre_ejecutable: nombre del binario que quiere generarse
#		nombre_main: nombre del archivo .cpp donde se encuentra el main
#				(sin el .cpp)
# Genera automáticamente la estructura de ficheros especificada

EXECUTABLE=$1
OBJECT_MODULES=`ls ./obj -I $2.o`

$(EXECUTABLE): $(OBJECT_MODULES)
	g++ obj/$2.o -l$(EXECUTABLE) -o bin/$1 -Llib
#g++ $^ -o $@

lib$(EXECUTABLE).a: $(OBJECT_MODULES)
	ar rvs lib/lib$(EXECUTABLE).a $(OBJECT_MODULES)

.o: .cpp
	$(CC) -Wall -c $< -o $@ -Iinclude

#g++ -c src/$ARCH.cpp -o obj/$ARCH.o -Iinclude

#g++ obj/*.o -o bin/$1

#ar rvs lib/lib$1.a obj/*.o

#g++ obj/$2.o -l$1 -o bin/$1 -Llib
