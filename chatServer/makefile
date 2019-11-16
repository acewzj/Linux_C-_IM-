CXX = g++

SRC_DIR = ./
TARGET = main
OBJ = dbmysql.o user.o userlist.o thread.o server.o
CFLAGS = -g -c -lpthread -lmysqlclient 
$(TARGET):$(OBJ)
	$(CXX) -o $(TARGET) $(OBJ) main.cpp -lpthread -lmysqlclient
	rm -rf $(OBJ)

dbmysql.o:
	$(CXX) -g -c -L/usr/lib/mysql-workbench  $(SRC_DIR)dbmysql.cpp 	

user.o:
	$(CXX) -g -c $(SRC_DIR)user.cpp 

server.o:
	$(CXX) -g -c $(SRC_DIR)server.cpp 

userlist.o:
	$(CXX) -g -c $(SRC_DIR)userlist.cpp 	

thread.o:
	$(CXX) -g -c $(SRC_DIR)thread.cpp 

clean:
	rm -rf $(OBJ) $(TARGET)