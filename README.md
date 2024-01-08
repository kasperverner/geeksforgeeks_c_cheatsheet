# [C Cheatsheet](https://www.geeksforgeeks.org/c-cheatsheet/)

This C Cheat Sheet provides an overview of both basic and advanced concepts of the C language. Whether you’re a beginner or an experienced programmer, this cheat sheet will help you revise and quickly go through the core principles of the C language.

In this Cheat Sheet, we will delve into the basics of the C language, exploring its fundamental concepts that lay the groundwork for programming. We will cover topics such as variables, data types, and operators, providing you with a solid understanding of the building blocks of C programming.

## Basic Syntax

Consider the below Hello World program:

```c
#include <stdio.h>

int main()
{
  printf("Hello World!");
  return 0;
}
```

### Output

```c
Hello World!
```

Here,

- **\# include <stdio.h>:** The header file inclusion to use printf() function.
- **int main():** The main() function is the entry point of any C program.
- **printf(“Hello World”):** Function to print hello world.
- **return 0:** Value returned by the main() function.

## Variables

A variable is the name given to the memory location that stores some data.

### Syntax of Variable

```c
  data_type variable_name;
  data_type variable_name = initial_value;
```

A variable can be of the following types:

1. Local Variable
2. Global Variable
3. Static Variable
4. Extern Variable
5. Auto Variable
6. Register Variable

```c
  Note: There are a few rules which we have to follow while naming a variable.
```

### Data Types

The data type is the type of data that a given variable can store. Different data types have different sizes. There are 3 types of data types in C:

1. Basic Data Types
2. Derived Data Types
3. User Defined Data Types

### 1. Basic Data Types

Basic data types are built-in in the C programming language and are independent of any other data type. There are x types of basic data types in C:

1. char: Used to represent characters.
2. int: Used to represent integral numbers.
3. float: Used to represent decimal numbers up to 6-7 precision digits.
4. double: Used to represent decimal numbers up to 15 precision digits.
5. void: Used to represent the valueless entity.

#### Example of Basic Data Types

```c
  char c = 'a';
  int integer = 24;
  float f = 24.32;
  double d = 24.3435;
  void v;
```

The size of these basic data types can be modified using *data type modifiers* which are:

1. short
2. long
3. signed
4. unsigned

#### Example of Data Type Modifiers

```c
  unsigned int var1;
  long double var2;
  long int var3;
```

### 2. Derived Data Types

Derived data types are derived from the basic data types. There are 2 derived data types in C:

1. Array: Used to represent a collection of similar data types.
2. Pointer: Used to represent the address of a variable.

### 3. User-Defined Data Types

The user-defined data types are the data types that are defined by the programmers in their code.  There are 3 user-defined data types in C:

1. Structure
2. Union
3. Enumeration

## Identifiers

Identifiers is the name given to the variables, functions, structure, etc. Identifiers should follow the following set of rules:

1. A variable name must only contain alphabets, digits, and underscore.
2. A variable name must start with an alphabet or an underscore only. It cannot start with a digit.
3. No whitespace is allowed within the variable name.
4. A variable name must not be any reserved word or keyword.

## Keywords

Keywords are the reserved words that have predefined meanings in the C compiler. They cannot be used as identifiers.

### Example of Keywords

```c
  auto,
  float,
  int,
  return,
  switch
```

## Basic Input and Output

The basic input and output in C are done using two <stdio.h> functions namely scanf() and print() respectively.

### Basic Output – print()

The printf() function is used to print the output on the standard output device which is generally the display screen.

#### Syntax of printf()

```c
  printf("formatted-string", ...{arguments-list});
```

where,

- **formatted-string:** String to be printed. It may contain format specifiers, escape sequences, etc.
- **arguments-list:** It is the list of data to be printed.

#### Basic Input – scanf()

The scanf() function is used to take input from the standard input device such as the keyboard.

#### Syntax of scanf()

  ```c
    scanf("formatted-string", {address-argument-list});
  ```

where,

- **formatted-string:** String that describes the format of the input.
- **address-of-arguments-list:** It is the address list of the variables where we want to store the input.

### Example of Input and Output

```c
  // C program to illustrate the basic input and output using
  // printf() and scanf()
  #include <stdio.h>

  int main()
  {
      int roll_num;
      char name[50];

      // taking input using scanf
      scanf("Enter Roll No.: %d", &roll_num);
      scanf("Enter Name: %s", name);

      // printing output using printf
      printf("Name is %s and Roll Number is %d", name,
            roll_num);

      return 0;
  }
```

### Default Output

```c
  Name is ? and Roll Number is 0
```

### Input

```c
  Enter Roll No: 20
  Enter Name: GeeksforGeeks
```

### Output

```c
  Name is GeeksforGeeks and Roll Number is 20.
```

## Format Specifiers

Format specifiers are used to describe the format of input and output in formatted string. It is different for different data types. It always starts with %

The following is the list of some commonly used format specifiers in C:

| Format Specifier | Description |
| --- | --- |
| %c | Used to print a character |
| %d | Used to print an integer |
| %f | Used to print a float value |
| %lf | Used to print a double value |
| %p | Used to print a pointer |
| %s | Used to print a string |
| %u | Used to print an unsigned integer |
| %% | Used to print a % char |

## Escape Sequences

Escape sequences are the characters that are used to represent those characters that cannot by represented normally. They start with **( \ ) backslash** and can be used inside string literals.

The below table list some commonly used escape sequences:

| Escape Sequence | Name | Description |
| --- | --- | --- |
| \b | Backspace | Moves the cursor to the previous tab |
| \n | Newline | Moves the cursor to the next line |
| \r | Carriage Return | Moves the cursor to the beginning of the line |
| \t | Horizontal Tab | Moves the cursor to the next tab |
| \v | Vertical Tab | Moves the cursor to the next tab |
| \\\\ | Backslash | Prints a backslash |
| \\' | Single Quote | Prints a single quote |
| \\" | Double Quote | Prints a double quote |
| \\? | Question Mark | Prints a question mark |
| \0 | Null Character | Prints a null character |

## Operators

Operators are the symbols that are used to perform some kind of operation. Operators can be classified based on the type of operation they perform.

There are the following types of operators in C:

| Operator Type | Description | Example |
| --- | --- | --- |
| Arithmetic Operators | Used to perform arithmetic operations such as addition, subtraction, multiplication, etc. | +, -, *, /, % |
| Relational Operators | Used to compare two values | ==, !=, >, <, >=, <= |
| Bitwise Operators | Used to perform bitwise operations | &, \|, ^, ~, <<, >> |
| Logical Operators | Used to perform logical operations such as AND, OR, NOT, etc. | &&, \|\|, ! |
| Conditional Operators | Used to insert conditional code | ?, : |
| Assignment Operators | Used to assign a value to a variable | =, +=, -=, *=, /=, %=, <<=, >>=, &=, ^=, \|= |
| Misc Operators | Used to perform miscellaneous operations | sizeof(), &, \*, ?, :, ., ->, etc. |

## Control Statements

Conditional statements are used to execute some block of code based on whether the given condition is true. There are the following conditional statements in C:

### 1. If Statement

if statement contains a block of code that will be executed if and only if the given condition is true.

#### Syntax of if statement

```c
  if (condition)
  {
      // code to be executed if condition is true
  }
```

### 2. If-else Statement

The if-else statement contains the else block in addition to the if block which will be executed if the given condition is false.

#### Syntax of if-else statement

```c
  if (condition)
  {
      // code to be executed if condition is true
  }
  else
  {
      // code to be executed if condition is false
  }
```

### 3. if-else-if Ladder

The if-else-if ladder is used when we have to test multiple conditions and for each of these conditions, we have a separate block of code.

#### Syntax of if-else-if ladder

```c
  if (condition1)
  {
      // code to be executed if condition1 is true
  }
  else if (condition2)
  {
      // code to be executed if condition2 is true
  }
  ...
  else
  {
      // code to be executed if all the conditions are false
  }
```

### 4. Switch Case Statement

The switch case statement is an alternative to the if-else-if ladder that can execute different blocks of statements based on the value of the single variable named switch variable.

#### Syntax of switch case statement

```c
  switch (switch_variable)
  {
      case value1:
          // code to be executed if switch_variable = value1
          break;
      case value2:
          // code to be executed if switch_variable = value2
          break;
      ...
      default:
          // code to be executed if all the values are not matched
  }
```

### 5. Conditional Operator

The conditional operator is a kind of single-line if-else statement that tests the condition and executes the true and false statements.

#### Syntax of conditional operator

```c
  (condition) ? (true_statement) : (false_statement);
```

#### Example of Conditional Operator

```c
  // C program to illustrate conditional statements
  #include <stdio.h>

  int main()
  {
  // conditional operator will assign 10 if 5 < 25,
  // otherwise it will assign 20
  int i = 5 < 25 ? 10 : 20;

  if (i == 10)
    printf("i is 10");
  else if (i == 15)
    printf("i is 15");
  else if (i == 20)
    printf("i is 20");
  else
    printf("i is not present");
  }
```

### Output

```c
  i is 10
```

## Loops

Loops are the control statements that are used to repeat some block of code till the specified condition is false. There are 3 loops in C:

### 1. For loop

The for loop is an entry-controlled loop that consists initialization, condition, and updating as a part of itself.

#### Syntax of for loop

```c
  for (initialization; condition; updation)
  {
      // code to be executed
  }
```

### 2. While loop

The while loop is also an entry-controlled loop but only the condition is the part of is syntax.

#### Syntax of while loop

```c
  while (condition)
  {
      // code to be executed
  }
```

### 3. Do-While loop

The do-while loop is an exit-controlled loop in which the condition is checked after the body of the loop.

#### Syntax of do-while loop

```c
  do
  {
      // code to be executed
  } while (condition);
```

## Jump Statements

Jump statements are used to override the normal control flow of the program. There are 3 jump statements in C:

### 1. Break Statement

It is used to terminate the loop and bring the program control to the statements after the loop.

#### Syntax of break statement

```c
  break;
```

It is also used in the switch statement.

### 2. Continue Statement

The continue statement skips the current iteration and moves to the next iteration when encountered in the loop.

#### Syntax of continue statement

```c
  continue;
```

### 3. Goto Statement

The goto statement is used to move the program control to the predefined label.

#### Syntax of goto statement

```c
  goto label;
  ...
  ...
  label: statement;
```

## Example of Loops and Jump Statements

```c
  // C program to illustrate loops
  #include <stdio.h>

  // Driver code
  int main()
  {
    int i = 0;

    // for loop with continue
    for (i = 1; i <= 10; i++) {
      if (i == 5 || i == 7) {
      continue;
      }
      printf("%d ", i);
    }
    printf("\n");

    // while loop with break
    i = 1;
    while (i <= 10) {
      if (i == 7) {
      break;
      }
      printf("%d ", i++);
    }
    printf("\n");

    // do_while loop
    i = 1;
    do {
      printf("%d ", i++);
    } while (i <= 10);
    printf("\n");

    // goto statement
    i = 1;
    any_label:
    printf("%d ", i++);
    if (i <= 10) {
      goto any_label;
    }

    return 0;
  }
```

### Output

```c
  1 2 3 4 6 8 9 10
  1 2 3 4 5 6
  1 2 3 4 5 6 7 8 9 10
  1 2 3 4 5 6 7 8 9 10
```

## Arrays

An array is a fixed-size homogeneous collection of items stored at a contiguous memory location. It can contain elements from type int, char, float, structure, etc. to even other arrays.

### Syntax of Array

- Array provides **random access** using the element index.
- Array **size cannot change**.
- Array can have **multiple dimensions** in which it can grow.

```c
  data_type arr_name [size1];   // 1D array
  data_type arr_name [size1][size2];   // 2D array
  data_type arr_name [size1][size2][size3];    // 3D array
```

### Example of Arrays

```c
  // C Program to demonstrate the use of array
  #include <stdio.h>

  int main()
  {
    // array declaration and initialization
    int arr[5] = { 10, 20, 30, 40, 50 };

    // modifying element at index 2
    arr[2] = 100;

    // traversing array using for loop
    printf("Elements in Array: ");
    for (int i = 0; i < 5; i++) {
      printf("%d ", arr[i]);
    }

    return 0;
  }
```

### Output

```c
  Elements in Array: 10 20 100 40 50
```

## Strings

Strings are the sequence of characters terminated by a ‘\0’ NULL character. It is stored as the array of characters in C.

### Syntax of String

```c
  char string_name [] = "any_text";
```

### Example of Strings

```c
  // C program to illustrate strings

  #include <stdio.h>
  #include <string.h>

  int main()
  {
    // declare and initialize string
    char str[] = "Geeks";

    // print string
    printf("%s\n", str);

    int length = 0;
    length = strlen(str);

    // displaying the length of string
    printf("Length of string str is %d", length);

    return 0;
  }
```

### Output

```c
  Geeks
  Length of string str is 5
```

### C string functions

C language provides some useful functions for string manipulation in <string.h> header file. Some of them are as follows:

| Function | Description |
| --- | --- |
| strlen() | Returns the length of the string |
| strcmp() | Compares two strings |
| strcpy() | Copies the string from source to destination |
| strcat() | Concatenates the string from source to destination |
| strchr() | Find the given character in the string |
| strstr() | Returns the pointer to the first occurrence of the substring in the string |

## Pointers

Pointers are the variables that store the address of another variable. They can point to any data type in C.

### Syntax of Pointer

```c
  data_type * ptr_name;
```

```c
  Note: The addressof (&) operator is used to get the address of a variable.
```

We can dereference (access the value pointed by the pointer) using the same * operator.

### Example of Pointer

```c
  // C program to illustrate pointers
  #include <stdio.h>

  int main()
  {
    int var = 10;

    // declare pointer variable
    int *ptr;

    // note that data type of ptr and var must be same
    ptr = &var;

    // assign the address of a variable to a pointer
    printf("Value at ptr = %p \n", ptr);
    printf("Value at var = %d \n", var);
    printf("Value at *ptr = %d \n", *ptr);

    return 0;
  }
```

### Output

```c
  Value at ptr = 0x7ffd8c9b4a2c
  Value at var = 10
  Value at *ptr = 10
```

There are different types of pointers based on different classification parameters. Some of them are:

1. Double Pointers
2. Function Pointers
3. Structure Pointers
4. NULL Pointers
5. Dangling Pointers
6. Wild Pointers

## Functions

Functions are the block of statements enclosed within { } braces that perform some specific task. They provide code reusability and modularity to the program.

### Function Syntax is divided into three parts

#### 1. Function Prototype

It tells the compiler about the existence of the function.

```c
  return_type function_name ( parameter_list... );
```

where,

1. **Return Type:** It is the type of optional value returned by the function. Only one value can be returned.
2. **Parameters:** It is the data passed to the function by the caller.

#### 2. Function Definition

It contains the actual statements to be executed when the function is called.

```c
  return_type function_name ( parameter_list... )
  {
      // code to be executed
  }
```

#### 3. Function Call

Calls the function by providing arguments. A function call must always be after either function definition or function prototype.

```c
  function_name ( argument_list... );
```

### Example of Functions

```c
  // C program to show function
  // call and definition
  #include <stdio.h>

  // Function that takes two parameters
  // a and b as inputs and returns
  // their sum
  int sum(int a, int b) { return a + b; }

  // Driver code
  int main()
  {
    // Calling sum function and
    // storing its value in add variable
    int add = sum(10, 30);

    printf("Sum is: %d", add);
    return 0;
  }
```

### Output

```c
  Sum is: 40
```

### Types of Functions

A function can be of 4 types based on return value and parameters:

1. Function with no return value and no parameters.
2. Function with no return value and parameters.
3. Function with return value and no parameters.
4. Function with return value and parameters.

There is another classification of function in which there are 2 types of functions:

1. Library Functions
2. User-Defined Functions

### Dynamic Memory Management

Dynamic memory management allows the programmer to allocate the memory at the program’s runtime. The C language provides four <stdlib.h> functions for dynamic memory management which are malloc(), calloc(), realloc() and free().

#### 1. malloc()

The **malloc() function** allocates the block of a specific size in the memory. It returns the void pointer to the memory block. If the allocation is failed, it returns the null pointer.

#### Syntax of malloc()

```c
  malloc (size_t size);
```

#### 2. calloc()

The **calloc() function** allocates the number of blocks of the specified size in the memory. It returns the void pointer to the memory block. If the allocation is failed, it returns the null pointer.

#### Syntax of calloc()

```c
  calloc (size_t num, size_t size);
```

#### 3. realloc()

The **realloc() function** is used to change the size of the already allocated memory. It also returns the void pointer to the allocated memory.

#### Syntax of realloc()

```c
  realloc (void* ptr, size_t size);
```

#### 4. free()

The **free() function** is used to deallocate the already allocated memory.

#### Syntax of free()

```c
  free (ptr);
```

### Example of Dynamic Memory Allocation

```c
  // C program to illustrate the dynamic memory allocation
  #include <stdio.h>
  #include <stdlib.h>

  int main()
  {
    // using malloc to allocate the int array of size 10
    int* ptr = (int*)malloc(sizeof(int) * 10);

    // allocating same array using calloc
    int* ptr2 = (int*)calloc(10, sizeof(int));

    printf("malloc Array Size: %d\n", 10);
    printf("calloc Array Size: %d\n", 10);

    // reallocating the size of first array
    ptr = realloc(ptr, sizeof(int) * 5);
    printf("malloc Array Size after using realloc: %d", 5);

    // freeing all memory
    free(ptr);

    return 0;
  }
```

### Output

```c
  malloc Array Size: 10
  calloc Array Size: 10
  malloc Array Size after using realloc: 5
```

## Structures

A structure is a user-defined data type that can contain items of different types as its members. In C, struct keyword is used to declare structures and we can use **( . ) dot operator** to access structure members.

### Structure Template

To use structure, we first have to define its template.

```c
  struct structure_name
  {
      data_type member1;
      data_type member2;
      ...
      data_type memberN;
  };
```

### Structure Variable Syntax

```c
  ...{
    ...structure template...
  }var1, var2..., varN;
```

or

```c
  strcut str_name var1, var2,...varN;
```

### Example of Structure

```c
  // C program to illustrate the use of structures
  #include <stdio.h>

  // declaring structure with name str1
  struct str1 {
    int i;
    char c;
    float f;
    char s[30];
  };

  // declaring structure with name str2
  struct str2 {
    int ii;
    char cc;
    float ff;
  } var; // variable declaration with structure template

  // Driver code
  int main()
  {
    // variable declaration after structure template
    // initialization with initializer list and designated
    // initializer list
    struct str1 var1 = { 1, 'A', 1.00, "GeeksforGeeks" },
        var2;
    struct str2 var3 = { .ff = 5.00, .ii = 5, .cc = 'a' };

    // copying structure using assignment operator
    var2 = var1;

    printf("Struct 1:\n\ti = %d, c = %c, f = %f, s = %s\n",
      var1.i, var1.c, var1.f, var1.s);
    printf("Struct 2:\n\ti = %d, c = %c, f = %f, s = %s\n",
      var2.i, var2.c, var2.f, var2.s);
    printf("Struct 3\n\ti = %d, c = %c, f = %f\n", var3.ii,
      var3.cc, var3.ff);

    return 0;
  }
```

### Output

```c
  Struct 1:
    i = 1, c = A, f = 1.000000, s = GeeksforGeeks
  Struct 2:
    i = 1, c = A, f = 1.000000, s = GeeksforGeeks
  Struct 3
    i = 5, c = a, f = 5.000000
```

## Union

A union is also a user-defined data type that can contain elements of different types. However, unlike structure, a union stores its members in a shared memory location rather than having separate memory for each member.

### Syntax of Union

```c
  union union_name
  {
      data_type member1;
      data_type member2;
      ...
      data_type memberN;
  };
```

Union members can be accessed using **dot operator ( . )** but only one member can store the data at a particular instance in time.

### Example of Union

```c
  // C Program to demonstrate how to use union
  #include <stdio.h>

  // union template or declaration
  union un {
    int member1;
    char member2;
    float member3;
  };

  // driver code
  int main()
  {

    // defining a union variable
    union un var1;

    // initializing the union member
    var1.member1 = 15;

    printf("The value stored in member1 = %d",
      var1.member1);

    return 0;
  }
```

### Output

```c
  The value stored in member1 = 15
```

## Enumerations (enum)

Enumeration, also known as enum is a user-defined data type that is used to assign some name to the integral constant. By default, the enum members are assigned values starting from 0 but we can also assign values manually.

### Syntax of Enum

```c
  enum { name1, name2, name3 = value };
```

### Example of Enum

```c
  // An example program to demonstrate working
  // of enum in C
  #include <stdio.h>

  enum week { Mon, Tue, Wed, Thur, Fri, Sat, Sun };

  int main()
  {
    enum week day;
    day = Wed;
    printf("%d", day);
    return 0;
  }
```

### Output

```c
  2
```

## File Handling

File handling is the process of performing input and output on a file instead of the console. We can store, retrieve, and update data in a file. C supports text and binary files.

### C File Operations

We can perform some set of operations on a file and C language provide some functions for it.

1. Creating a new file – fopen() with attributes as “a” or “a+” or “w” or “w+”
2. Opening an existing file – fopen()
3. Reading from file – fscanf() or fgets()
4. Writing to a file – fprintf() or fputs()
5. Moving to a specific location in a file – fseek(), rewind()
6. Closing a file – fclose()

## Preprocessor Directives

The preprocessor directives are used to provide instructions to the preprocessor that expands the code before compilation. They start with the # symbol.

**The following table lists all the preprocessor directives in C/C++:**

| Preprocessor Directive | Description |
| --- | --- |
| #define | Used to define a macro |
| #undef | Used to undefine a macro |
| #include | Used to include the header file |
| #ifdef | Used to check if macro is defined or not |
| #ifndef | Used to check if macro is not defined |
| #if | Used to check if a condition is true |
| #else | Used with #if to specify the alternative |
| #elif | Used with #if to specify the alternative |
| #endif | Used to end #if directive |
| #pragma | Used to provide additional information to the compiler |

## Common Library Functions

C languages come bundled with some Standard Libraries that contain some useful functions to make it easier to perform some common operations. These are as follows:

### C Math Functions

The <math.h> header file contains functions to perform the arithmetic operations. The following table contains some common maths functions in C:

| Function | Description |
| --- | --- |
| ceil(x) | Returns the smallest integer greater than or equal to the given number |
| floor(x) | Returns the largest integer less than or equal to the given number |
| fabs(x) | Returns the absolute value of the given number |
| sqrt(x) | Returns the square root of the given number |
| cbrt(x) | Returns the cube root of the given number |
| pow(x, y) | Returns the given number x to the power of y |
| exp(x) | Returns the exponential value of the given number |
| fmod(x, y) | Returns the remainder of the given number x divided by y |
| log(x) | Returns the natural logarithm of the given number |
| log10(x) | Returns the base-10 logarithm of the given number |
| cos(x) | Returns the cosine of the given number |
| sin(x) | Returns the sine of the given number |
| tan(x) | Returns the tangent of the given number |

## Conclusion

In summary, this C Cheat Sheet offers a concise yet comprehensive reference for programmers of all levels. Whether you’re a beginner or an experienced coder, this cheat sheet provides a quick and handy overview of the core principles of C. With its organized format, code examples, and key syntaxes, it serves as a valuable resource to refresh your knowledge and navigate through the intricacies of C programming. Keep this cheat sheet close by to accelerate your coding journey and streamline your C programming endeavors.


