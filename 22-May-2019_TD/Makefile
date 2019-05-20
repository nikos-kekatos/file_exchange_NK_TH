CCP = clang++
CFLAGS = -I. -I/usr/local/include/eigen3 -I/Users/thaodang/GIT/pagai/build/deepcontrol/include
OBJS = file1.o file2.o


all : bc executable

bc :
	$(CCP) -emit-llvm $(CFLAGS) -g -c neuralnet.cpp -o neuralnet.bc

executable : neuralnet.o
	$(CCP) -o neuralnet neuralnet.o

neuralnet.o : 
	$(CCP) -g -c $(CFLAGS) neuralnet.cpp
 
clean :make 
	rm neuralnet.o executable core
