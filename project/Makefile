#
#  To sa opcje dla kompilacji
#
CXXFLAGS=-g -Iinc -Wall -pedantic -std=c++11

TRGDIR=/tmp/dron-podwodny

./dron-podwodny: obj obj/main.o\
						obj/lacze_do_gnuplota.o obj/wektor3D.o obj/scena.o obj/woda.o\
						obj/dno.o obj/powierzchnia.o obj/prostopadloscian.o obj/dron.o\
						obj/menu.o obj/macierz3D.o obj/graniastoslup.o obj/wirnik.o\
						obj/przeszkoda.o obj/sciana.o obj/pret.o obj/blok.o

	g++ -Wall -pedantic -std=c++11 -o ./dron-podwodny obj/main.o\
                        obj/lacze_do_gnuplota.o obj/wektor3D.o obj/scena.o obj/woda.o\
						obj/dno.o obj/powierzchnia.o obj/prostopadloscian.o obj/dron.o\
						obj/menu.o obj/macierz3D.o obj/graniastoslup.o obj/wirnik.o\
						obj/przeszkoda.o obj/sciana.o obj/pret.o obj/blok.o


obj:
	mkdir -p obj

obj/lacze_do_gnuplota.o: inc/lacze_do_gnuplota.hh src/lacze_do_gnuplota.cpp
	g++ -c ${CXXFLAGS} -o obj/lacze_do_gnuplota.o src/lacze_do_gnuplota.cpp

obj/main.o: src/main.cpp 
	g++ -c ${CXXFLAGS} -o obj/main.o src/main.cpp

obj/menu.o: src/menu.cpp inc/menu.hh inc/lacze_do_gnuplota.hh inc/scena.hh inc/dron.hh
	g++ -c ${CXXFLAGS} -o obj/menu.o src/menu.cpp

obj/scena.o: src/scena.cpp inc/scena.hh inc/woda.hh inc/dno.hh
	g++ -c ${CXXFLAGS} -o obj/scena.o src/scena.cpp

obj/woda.o: src/woda.cpp inc/woda.hh
	g++ -c ${CXXFLAGS} -o obj/woda.o src/woda.cpp
	
obj/dno.o: src/dno.cpp inc/dno.hh 
	g++ -c ${CXXFLAGS} -o obj/dno.o src/dno.cpp

obj/dron.o: src/dron.cpp inc/dron.hh inc/prostopadloscian.hh
	g++ -c ${CXXFLAGS} -o obj/dron.o src/dron.cpp

obj/wirnik.o: src/wirnik.cpp inc/wirnik.hh
	g++ -c ${CXXFLAGS} -o obj/wirnik.o src/wirnik.cpp	

obj/graniastoslup.o: src/graniastoslup.cpp inc/graniastoslup.hh
	g++ -c ${CXXFLAGS} -o obj/graniastoslup.o src/graniastoslup.cpp

obj/prostopadloscian.o: src/prostopadloscian.cpp inc/prostopadloscian.hh
	g++ -c ${CXXFLAGS} -o obj/prostopadloscian.o src/prostopadloscian.cpp

obj/sciana.o: src/sciana.cpp inc/sciana.hh
	g++ -c ${CXXFLAGS} -o obj/sciana.o src/sciana.cpp

obj/pret.o: src/pret.cpp inc/pret.hh
	g++ -c ${CXXFLAGS} -o obj/pret.o src/pret.cpp

obj/blok.o: src/blok.cpp inc/blok.hh
	g++ -c ${CXXFLAGS} -o obj/blok.o src/blok.cpp

obj/przeszkoda.o: src/przeszkoda.cpp inc/przeszkoda.hh
	g++ -c ${CXXFLAGS} -o obj/przeszkoda.o src/przeszkoda.cpp

obj/powierzchnia.o: src/powierzchnia.cpp inc/powierzchnia.hh inc/wektor3D.hh inc/consts.h
	g++ -c ${CXXFLAGS} -o obj/powierzchnia.o src/powierzchnia.cpp

obj/wektor3D.o: src/wektor3D.cpp inc/wektor3D.hh inc/wektor.hh
	g++ -c ${CXXFLAGS} -o obj/wektor3D.o src/wektor3D.cpp

obj/macierz3D.o: src/macierz3D.cpp inc/macierz3D.hh inc/macierz.hh inc/wektor3D.hh
	g++ -c ${CXXFLAGS} -o obj/macierz3D.o src/macierz3D.cpp

clean:
	rm -f obj/*.o ./dron-podwodny
