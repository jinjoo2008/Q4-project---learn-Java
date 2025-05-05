# Q4-project---learn-Java
learning Java!

## Week 1:
learned:
- main() method
- classes
- System.out.println();
- comments (Single-line // and Multi-line/* */)

```java
public satic void main(String [] args) {
   System.out.println("Hello!");
//this is code!
}
```
Primitive Data Types
- you have to name the data types, so try to name them appropriately (second words and on should start with a capital letter, don't use a space to seperate words)
- int: integer number
- double: any number
- char: single character
- string: word(s) (put in " ")
- boolean: true/false
- final keyword: value of a variable cannot be changed if the variable was declared using the final keyword

```java
int age = 28; 

char grade = 'A';

boolean late = true;

byte b = 20;

long num1 = 1234567;

short no = 10;

float k = (float)12.5;

double pi = 3.14;

// Value cannot be changed:
final double PI = 3.14;
```

Math operations (order of operations: PEMDAS)
- \+ addition
- \- subtraction
- \* multiplication
- \/ division
- \% modulo (yields the remainder)

```java
int a = 20;
int b = 10;

int result;

result = a + b;  // 30

result = a - b;  // 10

result = a * b;  // 200

result = a / b;  // 2

result = a % b;  // 0
```

Comparison operations
- \> greater than
- \< less than
- \>= greater than or equal to
- \<= less than or equal to
- \== equal to
- \!= not equal to

- \== can only compare numbers whereas .equals() can compare anything (including strings!)

```java
int a = 5;
int b = 3;

boolean result = a > b;
// result now holds the boolean value true
```

Compound Assignment Operators
- \+=
- \-=
- \*=
- \/=
- \%=

```java
int number = 5;

number += 3; // Value is now 8
number -= 4; // Value is now 4
number *= 6; // Value is now 24
number /= 2; // Value is now 12
number %= 7; // Value is now 5
```

Increment and Decrement Operators
- \++ adds by 1
- \-- subtracts by 1

```java
int numApples = 5;
numApples++; // Value is now 6

int numOranges = 5;
numOranges--; // Value is now 4
```

static typing - catches errors

```java
int i = 10;         // type is int
char ch = 'a';      // type is char

j = 20;             // won't compile, no type is given
char name = "Lil";  // won't compile, wrong data type
```

## Week 2:
