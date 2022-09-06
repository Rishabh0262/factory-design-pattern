This file have two branches

oldMethod - the method which complies the regular Header file & Classes and Objects using techniques to make a project work on OOPs.

factoryDesignPattern - It complies the implementaion of Factory Design for creating a project.


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
            
            
            




# Scenario
    if apart from "car" & "bike" if we want to create more classes like "bus", "auto", "scooty", etc.

    we'll have to #include those classes as well as lines in ... *1`**if else*** condition too.





****** ***factoryDesignPattern*** ******  

(We will just be using the Vehicle_factory class as the base class to handle all the fuctionality. Which will  be loosely coupled)  

[Library should be responsible to decide which obj type to create based on input  
Client should just call library's factory and pass type without worrying about actual implementation of creation of object.]

    1. Created vehicle_factory.hpp & included car.hpp and bike.hpp 

    2. Created vehicle_factory.cpp and implemented getvehicle()

    3. Compiled the .cpp files
            g++ -c vehicle_factory.cpp car.cpp bike.cpp vehicle.cpp  

    4. Created the #archived file 
            ar ru vehicle_library.a .\vehicle_factory.o .\car.o .\bike.o  

    5. Compile the smartClient file
            <!-- g++ -o smartClient .\smart_client.cpp .\vehicle_library.a -->
            g++ -o smartClient smart_client.cpp vehicle_library.a  



# We run the client's app  

    i.e. : ./smartClient 


