
#### Introduction
A String in Java is a collection of characters. 
e.g **"jerry"** contains the character **'j', 'e', 'r', 'r', and 'y'** 
in a sequence.

When we look closely, we can see that each values within
**"jerry"** is a character wrapped with single quote ' '. By default String is immutable which means 
once created it cannot be changed. We would discuss the immutability of the String later on this page.

#### Creating a String

There are several ways a String can be created in Java
  - using the String constructor that accepts arrays of characters, declaring it with a new keyword from java.lang library. 
  - Or using the string literal. See below for the two methods
  - Using String buffer
  - Using String Builder


```java
 char[] ch = {'j', 'e', 'r', 'r', 'y'}; 

String name = new String(ch);
 ```
This yielded same result as the one below

```java
String name = "jerry";
```

#### Immutability of String
The ability of a value being changed after creation is what is referred to as immutability.
As mentioned above. Once a String is created in Java and an attempt to change the value
of the String will result to the compiler creating new instance of the String. e.g

```java
1   String changeMe = "henry";
2   changeMe = "jerry";
```
From the code above, line 1 creates a String, 
attempt to change it on line **2** will create a new String in memory with the new value assigned

In other words, if two Strings are created with different variable names but the same values,
The JVM (Java Virtual Machine) checks the pool in heap memory and finds an existing value, then it will not create a new String
instance but it will point the first variable to the previously variable created. and returns the value.
e.g

```java
1   String myName = "jerry";
2   String yourName = "jerry";
```
Line 2 was not created in heap but returned from the value of line 1.





