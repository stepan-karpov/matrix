### Matrix

there is a matrix.h file in this directory which can be used
as a simple framework for matrix calculations

---

### Usage

matrix.h contains some basic functions 
which can be done with this object.
To use it you can include it in your C++ code with usual #include

Some operations you can use:

  ###### Addition, subtraction (with relevant sizes)
  
  ###### Multiplication by scalar

  ###### Multiplation by matrix (O(n^3)) with relevant sizes

  ###### Rank of a matrix

  ###### Trace of a matrix

Also these is a special "BigInteger" and "Rational" types, where long arithmetics was implemented.
You can also find "Residue" type, which is a the deduction ring by template modulo.

---

### Description

To use it you can include it in your C++ code with usual #include

---

### Example

Example of matrix addition
```
#include <iostream>
#include "matrix.h"

int main() {
  Matrix<5, 5, BigInteger> a;
  Matrix<5, 5, BigInteger> b;


  for (int i = 0; i < 5; ++i) {
    for (int j = 0; j < 5; ++j) {
      a[i][j] = i + j;
      b[i][j] = i + j;
    }
  }

  Matrix<5, 5, BigInteger> c = a + b;

  for (int i = 0; i < 5; ++i) {
    for (int j = 0; j < 5; ++j) {
      std::cout << c[i][j] << " ";
    }
    std::cout << "\n";
  }


  return 0;
}
```

