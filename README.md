# C++ Tutorial


## Basics
----
### Program Structure 
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

### Constants
In C++ we can define a variable as a constant. Meaning, its value does not change for the life of the program.
```cpp
const int weightGoal = 100;
```
### Enumerated Constants
This means the programmer can create a new variable type and then assign a finite number of values to it. 
```cpp
enum type_name {
  value1,
  value2,
  value3,
  .
  .
};
```
### File IO 

```cpp
 - Include the <fstream> library 
 - Create a stream (input, output, both)
      - ofstream myfile; (for writing to a file)
      - ifstream myfile; (for reading a file)
      - fstream myfile; (for reading and writing a file)
 - Open the file  myfile.open(“filename”);
 - Write or read the file
 - Close the file myfile.close();
```
### Header Files
The header file (.hpp) contain informatiom about how to do tasks while the main program (.cpp) tells what to do. Everything that is not directly related to to doing the task should be in the header file. Don't forget to include the header file in the main program.

```cpp
#include "main_header.hpp"
```

### User Input
The function std::cin will not retrieve strings that have a space in them. It will see the space as the end of the input. We will obviously need a method to enter strings. C++ has the function getline().

```cpp
#include<iostream>
#include<string>

using namespace std;
int main()
{
  int number;
  cin >> number;
  string name; 
  cout<<"Tell me your nickname?: ";
  getline(std::cin, name);
  cout<<"Hello "<<name<<"\n";
  return 0;
 }
```
## Arithmetic Operations
----
