#### String is a collection of characters. There are two types of strings commonly used in C++ programming language: 

#### 1. Strings that are objects of string class (The Standard C++ Library string class)
#### 2. C-strings (C-style Strings)
![](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20191113124516/StringInC.png)

C-strings
In C programming, the collection of characters is stored in the form of arrays.C-strings are arrays of type char terminated with null character, that is, \0 (ASCII value of null character is 0).

To define a C-string
char str[] = "C++"; - str is a string and it holds 4 characters. Although, "C++" has 3 character, the null character \0 is added to the end of the string automatically.

Alternative ways of defining a string
char str[4] = "C++";,   char str[] = {'C','+','+','\0'};,    char str[4] = {'C','+','+','\0'};

char str[100] = "C++";- Like arrays, it is not necessary to use all the space allocated for the string.


