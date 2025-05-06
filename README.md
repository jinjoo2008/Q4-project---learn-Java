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
learned:
- else statement: executes a block of code when the condition inside the if statement is false (Always last)
```java
boolean condition1 = false;

if (condition1){
    System.out.println("condition1 is true");
}
else{
    System.out.println("condition1 is not true");
}
// Prints: condition1 is not true
```
- else-if statement: can be chained together to check multiple conditions. Once a condition is true, a code block will be executed and the conditional statement will be exited (can be multiple)
```java
int testScore = 76;
char grade;

if (testScore >= 90) {
  grade = 'A';
} else if (testScore >= 80) {
  grade = 'B';
} else if (testScore >= 70) {
  grade = 'C';
} else if (testScore >= 60) {
  grade = 'D';
} else {
  grade = 'F';
}

System.out.println("Grade: " + grade); // Prints: C
```
- if statement: executes a block of code when a specified boolean expression is evaluated as true
```java
if (true) {
	System.out.println("This code executes");
}
// Prints: This code executes

if (false) {
	System.out.println("This code does not execute");
}
// There is no output for the above statement
```
- nested conditional statement: a conditional statement nested inside of another conditional statement. The outer conditional statement is evaluated first; if the condition is true, then the nested conditional statement will be evaluated
```java
boolean studied = true;
boolean wellRested = true;

if (wellRested) {
  System.out.println("Best of luck today!");  
  if (studied) {
    System.out.println("You are prepared for your exam!");
  } else {
    System.out.println("Study before your exam!");
  }
}

// Prints: Best of luck today!
// Prints: You are prepared for your exam!
```
Operators:
- ! NOT
```java
boolean a = true;
System.out.println(!a); // Prints: false

System.out.println(!false) // Prints: true
```
- && AND
```java
System.out.println(true && true); // Prints: true
System.out.println(true && false); // Prints: false
System.out.println(false && true); // Prints: false
System.out.println(false && false); // Prints: false
```
- || OR
```java
System.out.println(true || true); // Prints: true
System.out.println(true || false); // Prints: true
System.out.println(false || true); // Prints: true
System.out.println(false || false); // Prints: false
```

Conditional Operators (Order of Operations) --> If an expression contains multiple conditional operators, the order of evaluation is as follows: Expressions in parentheses -> NOT -> AND -> OR
```java
boolean foo = true && (!false || true); // true
/* 
(!false || true) is evaluated first because it is contained within parentheses. 

Then !false is evaluated as true because it uses the NOT operator. 

Next, (true || true) is evaluation as true. 

Finally, true && true is evaluated as true meaning foo is true. */
```
