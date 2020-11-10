all: all.out 
all.out : patient.o airborne.o Airborne_db.o AirborneTest.o AirborneDBTest.o foodborne.o Foodborne_db.o FoodborneTest.o FoodborneDBTest.o waterborne.o Waterborne_db.o WaterborneTest.o WaterborneDBTest.o vectorborne.o vectorborne_db.o VectorborneTest.o VectorborneDBTest.o
	g++ $^ -o $@ -lgtest -lgtest_main -lpthread
AirborneTest.o: AirborneTest.cpp patient.h airborne.h 
	g++ $< -c
AirborneDBTest.o: AirborneDBTest.cpp patient.h airborne.h Airborne_db.h
	g++ $< -c
Airborne_db.o : Airborne_db.cpp Airborne_db.h airborne.h patient.h
	g++ $< -c
airborne.o : airborne.cpp airborne.h patient.h
	g++ $< -c    
FoodborneTest.o: FoodborneTest.cpp patient.h foodborne.h 
	g++ $< -c
FoodborneDBTest.o: FoodborneDBTest.cpp patient.h foodborne.h Foodborne_db.h
	g++ $< -c
Foodborne_db.o : Foodborne_db.cpp Foodborne_db.h foodborne.h patient.h
	g++ $< -c
foodborne.o : foodborne.cpp foodborne.h patient.h
	g++ $< -c    
WaterborneTest.o: WaterborneTest.cpp patient.h waterborne.h 
	g++ $< -c
WaterborneDBTest.o: WaterborneDBTest.cpp patient.h waterborne.h Waterborne_db.h
	g++ $< -c
Waterborne_db.o : Waterborne_db.cpp Waterborne_db.h waterborne.h patient.h
	g++ $< -c
waterborne.o : waterborne.cpp waterborne.h patient.h
	g++ $< -c    
VectorborneTest.o: VectorborneTest.cpp patient.h vectorborne.h 
	g++ $< -c
VectorborneDBTest.o: VectorborneDBTest.cpp patient.h vectorborne.h vectorborne_db.h
	g++ $< -c
vectorborne_db.o : vectorborne_db.cpp vectorborne_db.h vectorborne.h patient.h
	g++ $< -c
vectorborne.o : vectorborne.cpp vectorborne.h patient.h
	g++ $< -c    
patient.o : patient.cpp patient.h
	g++ $< -c


clean:
	rm -rf *.o *.out
