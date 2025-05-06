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

ArrayList: used to represent a dynamic list.
- While Java arrays are fixed in size (the size cannot be modified), an ArrayList allows flexibility by being able to both add and remove elements
```java
// import the ArrayList package
import java.util.ArrayList;

// create an ArrayList called students
ArrayList<String> students = new ArrayList<String>();
```
Index: refers to an element’s position within an array.
- The index of an array starts from 0 and goes up to one less than the total length of the array
```java
int[] marks = {50, 55, 60, 70, 80};

System.out.println(marks[0]);
// Output: 50

System.out.println(marks[4]);
// Output: 80
```
Arrays: used to store a list of elements of the same datatype.
- Arrays are fixed in size and their elements are ordered
```java
// Create an array of 5 int elements
int[] marks = {10, 20, 30, 40, 50};
```
Array creation: an array can be created in the following ways:
- Using the {} notation, by adding each element all at once
- Using the new keyword, and assigning each position of the array individually
```java
int[] age = {20, 21, 30};

int[] marks = new int[3];
marks[0] = 50; 
marks[1] = 70;
marks[2] = 93;
```

Changing an element value: select the element via its index and use the assignment operator to set a new value
```java
int[] nums = {1, 2, 0, 4};
// Change value at index 2
nums[2] = 3;
```
Modifying ArrayLists: 
- To add elements to an ArrayList, you use the add() method. The element that you want to add goes inside of the ().
- To remove elements from an ArrayList, you use the remove() method. Inside the () you can specify the index of the element that you want to remove. Alternatively, you can specify directly the element that you want to remove.
```java
import java.util.ArrayList;

public class Students {
  public static void main(String[] args) {
    
     // create an ArrayList called studentList, which initially holds []
		ArrayList<String> studentList = new ArrayList<String>();
    
    // add students to the ArrayList
    studentList.add("John");
    studentList.add("Lily");
    studentList.add("Samantha");
    studentList.add("Tony");
    
    // remove John from the ArrayList, then Lily
    studentList.remove(0);
    studentList.remove("Lily");
    
    // studentList now holds [Samantha, Tony]
    
    System.out.println(studentList);
  }
}
```

## Week 3:


