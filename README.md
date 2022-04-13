# C++ Cheatsheet



## Program Structure
---- 
```cpp
  #include <iostream>

  int main() 
  {
    std::cout << "Hello world";
    return 0;
  }
```
Any line that has a hash sign at the start is a preprocessor directive. Include means add the declarations of the given library. In this case we are adding the declarations of the iostream library. The brackets means we try to insert a file from the directory where all the standard libraries are stored.

```cpp
   #include "main.hpp"
```
The double qoutes means we try to insert a file from the current directory, and if it is not there then look in the directory where all the standard libraries are stored.

To avoid writing std:: (or every other library) , before the start of the main function, put in the command "using namespace std;"
```cpp
   using namespace std;
   int main()
   {
   }
```
This tells the compiler to assume we are using the library.
