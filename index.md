# Background Substraction using Local SVD Binary Pattern
El presente proyecto es una implementación en c++ del algoritmo LSBP

# Getting Started
Requirements:
- Sistema Operativo: Ubuntu
- Install CUDA
- Opencv 3.2.0 o superior
- Compilador gcc, g++

To run the code:
- Clone o download the source code.
- Open a terminal in the repository folder.
- Compile with the command:
-using threads
g++ local_svd.cpp -fopenmp -o main -std=c++11 -lpthread -lstdc++fs  -DWITH_CUDA=ON -larmadillo `pkg-config --cflags --libs opencv`
- using cuda
nvcc local_svd.cu -o main2 -std=c++11 -lpthread  -larmadillo `pkg-config --cflags --libs opencv`

Using threads
or write "make"
- Run with the command:
./main

Using cuda
or write "make exec"
- Run with the command:
./main2

# 1. Framework[1]
![Alt text](https://github.com/Dijaq/BackgroundSubstraction/blob/master/datos/Framework.PNG?raw=true "Title")

# 2. Pseudocodigo[1]
![Alt text](https://github.com/Dijaq/BackgroundSubstraction/blob/master/datos/Pseucodigo.PNG?raw=true "Title")

# 3. Results
## 3.1 Time comparation
![Alt text](https://github.com/Dijaq/BackgroundSubstraction/blob/master/datos/Table.PNG?raw=true "Title")

## 3.2 CDnet 2012
![Alt text](https://github.com/Dijaq/BackgroundSubstraction/blob/master/datos/CDnet2012.PNG?raw=true "Title")

## 3.3 Own video
![Alt text](https://github.com/Dijaq/BackgroundSubstraction/blob/master/datos/OwnVideo.PNG?raw=true "Title")
