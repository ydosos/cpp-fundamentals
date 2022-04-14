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
![image](https://user-images.githubusercontent.com/98479568/163413847-306be1f5-1d02-4ce3-b38d-63dec5ea2249.png)

Prefix operators increment the value of the variable, then return the reference to the variable.
Postfix operators create a copy of the variable and increments the value of the variable. Then it returns a copy from BEFORE the increment.

## Control Flow
----

### Rational Operators

![image](https://user-images.githubusercontent.com/98479568/163414526-78d188e6-d383-4d42-8523-b32b09925ff8.png)

### Logic Operators

![image](https://user-images.githubusercontent.com/98479568/163414710-10ab0c90-8b97-4a3d-8099-67b29383aac1.png) 

### If-Else Statements

```cpp
if(boolean expression)
{
     //statements to execute if the boolean expression is true
}
else if (boolean expression #2)
{
     //statements to execute if the 'else if' boolean expression  #2 is true
}

else
{
     //statements to execute if the boolean expressions 
    //'if' and 'else if'  are false
}
```
### Switch Statements

```cpp
switch(expression)
{
     case constant-expression : statements;
                               break; (this is optional);
     case constant-expression : statements;
                               break; (this is optional);
     ...

     default : //optional
        statements;
}

```

### For Loops

```cpp
for ( declaration : range ) statement;

for (initialization; condition; increase) statement;

```

To create infinite loop: 

```cpp
for( ; ;)
{
     statements
}
```

### While Loops

```cpp
while(condition)
{
     statements;
}

```

To create infinite loop: 

```cpp
while(1)
{
     std::cout<<"This while loop will run forever\n";
}

```

#### Break and Continue 
Break statement will end the loop and begin executing the first statement that comes after the end of the loop.

The continue statement: The continue statement will force the next iteration to be executed.
