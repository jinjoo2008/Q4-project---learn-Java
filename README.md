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
learned:

while loop: repeatedly runs code as long as the given condition remains true
```java
int count = 0;
while (count < 5) {
    System.out.println("Count is: " + count);
    count++;
}
```

for loop: repeats code over a range of values by initializing a variable, checking a condition, and updating the variable each iteration
```java
public class LoopExample {
    public static void main(String[] args) {
        for (int i = 0; i < 5; i++) {
            System.out.println("Iteration " + i);
        }
    }
}
/*
Iteration 0
Iteration 1
Iteration 2
Iteration 3
Iteration 4
*/
```

for-each statement: allows you to directly loop through each item in an array or ArrayList and perform some action with each item
When creating a for-each statement, you must include the for keyword and two expressions inside of parentheses, separated by a colon. 
These include:
1. The handle for an element we’re currently iterating over.
2. The source array or ArrayList we’re iterating over.
```java
// array of numbers
int[] numbers = {1, 2, 3, 4, 5};

// for-each loop that prints each number in numbers
// int num is the handle while numbers is the source array
for (int num : numbers) {  
	System.out.println(num);
}
```

Strings:
- .length() --> returns the total number of characters – the length – of a String.
```java
String str = "Codecademy";  

System.out.println(str.length());
// prints 10
```

- .indexOf() --> returns the first occurence of a character or a substring in a String. The character/substring that you want to find the index of goes inside of the () (If indexOf() cannot find the character or substring, it will return -1)
```java
String str = "Hello World!";

System.out.println(str.indexOf("l"));
// prints 2

System.out.println(str.indexOf("Wor"));
// prints 6

System.out.println(str.indexOf("z"));
// prints -1
```

- .concat() --> append one String to the end of another String. This method returns a String representing the text of the combined strings
```java
String s1 = "Hello";
String s2 = " World!";

String s3 = s1.concat(s2);
// concatenates strings s1 and s2

System.out.println(s3);
// prints "Hello World!"
```

- .equals() --> ests for equality between two Strings (equals() compares the contents of each String. If all of the characters between the two match, the method returns true. If any of the characters do not match, it returns false. Additionally, if you want to compare two strings without considering upper/lower cases, you can use .equalsIgnoreCase())
```java
String s1 = "Hello";
String s2 = "World";

System.out.println(s1.equals("Hello"));
// prints true

System.out.println(s2.equals("Hello"));
// prints false 

System.out.println(s2.equalsIgnoreCase("world"));
// prints true 
```

- .charAt() --> returns the character of a String at a specified index. The index value is passed inside of the (), and should lie between 0 and length()-1
```java
String str = "This is a string";

System.out.println(str.charAt(0));
// prints 'T'

System.out.println(str.charAt(15));
// prints 'g'
```

- .toUpperCase() --> returns the string value converted to uppercase
- .toLowerCase() --> returns the string value converted to lowercase
```java
String str = "Hello World!";

String uppercase = str.toUpperCase();
// uppercase = "HELLO WORLD!"

String lowercase = str.toLowerCase();
// lowercase = "hello world!"
```

the "static" keyword: 
```java
public class ATM{
  // Static variables
  public static int totalMoney = 0;
  public static int numATMs = 0;

  // A static method
  public static void averageMoney(){
    System.out.println(totalMoney / numATMs);
  }
```

Static methods and variables: associated with the class as a whole, not objects of the class. Both are used by using the name of the class followed by the . operator
```java
public class ATM{
  // Static variables
  public static int totalMoney = 0;
  public static int numATMs = 0;

  // A static method
  public static void averageMoney(){
    System.out.println(totalMoney / numATMs);
  }

  public static void main(String[] args){

    //Accessing a static variable
    System.out.println("Total number of ATMs: " + ATM.numATMs); 

    // Calling a static method
    ATM.averageMoney();
  }

}
```

Static methods: cannot access or change the values of instance variables
```java
class ATM{
// Static variables
  public static int totalMoney = 0;
  public static int numATMs = 0; 

  public int money = 1;

  // A static method
  public static void averageMoney(){
    // Can not use this.money here because a static method can't access instance variables
  }

}
```

Non-static and static method: can access or change the values of static variables
```java
class ATM{
// Static variables 
  public static int totalMoney = 0; 
  public static int numATMs = 0; 
  public int money = 1;

 // A static method interacting with a static variable 
  public static void staticMethod(){ 
    totalMoney += 1;
   } 

  // A non-static method interactingwith a static variable 
  public void nonStaticMethod(){
    totalMoney += 1; 
  } 
}
```

Static Methods and the "this." Keyword: Static methods do not have a this reference and are therefore unable to use the class’s instance variables or call non-static methods
```java
public class DemoClass{

  public int demoVariable = 5;

  public void demoNonStaticMethod(){
    
  }
  public static void demoStaticMethod(){
    // Can't use "this.demoVariable" or "this.demoNonStaticMethod()"
  }
}
```

keywords "public" and "private": define the access of classes, instance variables, constructors, and methods
- private restricts access to only the class that declared the structure, while public allows for access from any class

Encapsulation: a technique used to keep implementation details hidden from other classes. Its aim is to create small bundles of logic

private keyword: encapsulates instance variables, prevents other classes from directly accessing these variables
```java
public class CheckingAccount{
  // Three private instance variables
  private String name;
  private int balance;
  private String id;
}
```

accessor methods: returns the value of a private variable. This gives other classes access to that value stored in that variable. without having direct access to the variable itself (Accessor methods take no parameters and have a return type that matches the type of the variable they are accessing)
```java
public class CheckingAccount{
  private int balance;
  
  //An accessor method
  public int getBalance(){
    return this.balance;
  }
}
```

mutator methods: resets the value of a private variable. This gives other classes the ability to modify the value stored in that variable without having direct access to the variable itself (Mutator methods take one parameter whose type matches the type of the variable it is modifying. Mutator methods usually don’t return anything)
```java
public class CheckingAccount{
  private int balance;
  
  //A mutator method
  public void setBalance(int newBalance){
    this.balance = newBalance;
  }
}
```

local variables: can only be used within the scope that they were defined in. This scope is often defined by a set of curly brackets. Variables can’t be used outside of those brackets
```java
public void exampleMethod(int exampleVariable){
  // exampleVariable can only be used inside these curly brackets.
}
```

the this keyword with variables: can be used to designate the difference between instance variables and local variables. Variables with this. reference an instance variable.
```java
public class Dog{
  public String name;

  public void speak(String name){
    // Prints the instance variable named name
    System.out.println(this.name);

    // Prints the local variable named name
    System.out.println(name);
  }
}
```

the this keyword with methods: can be used to call methods when writing classes
```java
public class ExampleClass{
  public void exampleMethodOne(){
    System.out.println("Hello");
  }

  public void exampleMethodTwo(){
    //Calling a method using this.
    this.exampleMethodOne();
    System.out.println("There");
  }
}
```

Static methods: methods that can be called within a program without creating an object of the class
```java
// static method
public static int getTotal(int a, int b) {
  return a + b;
}

public static void main(String[] args) {
  int x = 3;
  int y = 2;
  System.out.println(getTotal(x,y)); // Prints: 5
}
```

Calling a Static method: can be called by appending the dot operator to a class name followed by the name of the method
```java
int largerNumber = Math.max(3, 10); // Call static method
System.out.println(largerNumber); // Prints: 10

```

Math class (which is part of the java.lang package) contains a variety of static methods that can be used to perform numerical calculations
```java
System.out.println(Math.abs(-7.0)); // Prints: 7

System.out.println(Math.pow(5, 3)); // Prints: 125.0

System.out.println(Math.sqrt(52)); // Prints: 7.211102550927978
```






