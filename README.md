This file have two branches

oldMethod - the method which complies the regular Header file & Classes and Objects using techniques to make a project work on OOPs.

FactoryDesignPattern - It complies the implementaion of Factory Design for creating a project.


*********** oldMethod ***********
    1.  Created vehicle.hpp (as Base class) & vehicle.cpp.
    2.  Created car.hpp & bike.hpp (as 2 children) along with car.cpp & bike.cpp.
    3.  Compiled & Created the #object file
            $ g++ -c .\vehicle.cpp .\car.cpp .\bike.cpp

                where vehicle.o , car.o & bike.o were created

    4.  Archived these object files in "vehicle_library.a"
            $ ar ru vehicle_library.a car.o bike.o

    5.  Lastly created a client.cpp file which we will compile it and use the vehicle library to create the vehicle
            $ g++ -o client client.cpp .\vehicle_library.a

