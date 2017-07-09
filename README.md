# libfast_knn
C++ library of k-nearest neighbors algorithm (k-NN), faster because uses Armadillo lib

Example:

Look the file src/main.cpp

```
cooler@Nepal:~/codes/libfast_knn$ make
g++ -Wall -O3 -larmadillo -fstack-protector-all -D_FORTIFY_SOURCE=2 -c src/*.cpp -c lib/*.h -c lib/*.cpp
g++ -o bin/knn_test *.o -Wl,-z,relro,-z,now 
rm *.o

cooler@Nepal:~/codes/libfast_knn$ bin/knn_test 
Test Manhattan:
1:    5.0000   3.0000   1.6000   0.2000
	Result: 1
2:    1.0000   2.0000   1.6000   2.2000
	Result: 1
3:    6.0000   4.0000   4.6000   3.2000
	Result: 3
4:    0.9000   1.0000   2.6000   2.2000
	Result: 1
5:    9.0000   7.0000   4.6000   4.2000
	Result: 3

Test Euclidean:
1:    5.0000   3.0000   1.6000   0.2000
	Result: 1
2:    1.0000   2.0000   1.6000   2.2000
	Result: 2
3:    6.0000   4.0000   4.6000   3.2000
	Result: 3
4:    0.9000   1.0000   2.6000   2.2000
	Result: 2
5:    9.0000   7.0000   4.6000   4.2000
	Result: 3
```
