# Dart

## Introduction

Dart is a client-optimized language for developing fast apps on any platform. Its goal is to offer the most productive programming language for multi-platform development, paired with a flexible execution runtime platform for app frameworks.

Dart is fairly a new programming language, as compared to others (**First appeared:** *October 10, 2011*), and that makes it more fun to learn!

## Environment


## *Hello World!*

Let's start writing our first Dart Program!

```dart
void main() {
    print("Hello World!");
}
```

- `print()` is a function used to print lines onto output (*console*).

## Variables

While working with programming languages, it's essential that you "*store*" the values of few things, so that you could reuse those values at some other place. That is where variables come in! 

```dart
void main() {
    // I'm a single-line comment, and the computer is going to ignore me :'(
    /* I'm a multi-line comment,
    and the computer is going to ignore me too :'(
    */

    int numberOfStones = 6;
    String name = "Thanos";

    print("${name} tries to find the ${numberOfStones} infinity stones");
    // Thanos tries to find the 6 infinity stones

    name = "Mickey Mouse";
    print("${name} tries to find the ${numberOfStones} infinity stones");
    // Mickey Mouse tries to find the 6 infinity stones
}
```

The various types of data types available with Dart are:
- Number:
    - `int`
    - `double`
    - `num`
- Strings (`string`)
- Boolean (`bool`)
- Lists (`List`)
- Maps (`Map`)

```dart
void main() {
    int age = 11;
    double street = 9.45;
    bool isWizard = true;
    String name = "Harry Potter";

    print(name);
    // Harry Potter
}
```

## Strings

String data type represents a sequence of characters. They can be represented using either single, double or triple quotes. Strings with triple quotes are used to represent multi-line strings. They are zero-indexed!

```dart
String thisIsAString = 'value';

String thisAlso = "value";

String andThisToo = """value""";

String andAlsoThis = '''value''';
```

- Strings are immutable. So they can't be changed, but only reassigned its new value.

```dart
String name = "Eren Jeager";
name[0] = "A";
// Not Valid

name = "Naruto";
// Valid
```

- The length of a string could be found using `string.length`.

```dart
String adjective = "Beautiful";

print(adjective.length);
// 9

print(adjective[2]);
// a
```

### String Functions

It is common to use "*functions*" to modify a string.

- `.toUpperCase()`: Converts all characters in a string to upper case.

```dart
String food = "joey doesn't share food";
print(food.toUpperCase());
// JOEY DOESN'T SHARE FOOD
```

`.toLowerCase()` works similarly, except that it converts the string to lower case.

- `.indexOf()` finds the index of a given string within a string.

```dart
String company = "Microsoft";

print(company.indexOf("i"));
// 1

print(company.indexOf("soft"));
// 5
```

- `.contains()` checks if a string is present within in a string.

```dart
String a = "This is a string";
print(a.contains("is"));
// true
```

### String Concatenation

Strings could be concatenated in Dart using `+` operator.

```dart
String a = "Bro";
String b = "ther";

print(a + b);
// Brother
```

## Math

It's common to use *libraries*, for the use of specific functions. For math related functions, the library `math`.

```dart
import "dart:math";

void main() {
    print(max(10, 2));
}
```

## Input

The library associated with inputs is `io`.

```dart
import "dart:io";

void main() {
    print("How high can you jump?: ");
    String height = stdin.readLineSync();
}
```

### Number inputs

While taking number inputs, the inputs are taken as `Strings` and not as `number`. Hence, it is required to parse the `String` into `number`.

```dart
String num = stdin.readLineSync();

print(int.parse(num));
// Parse as Integer

print(double)
// Parse as Double
```

## Lists

A list is simply an ordered group of objects.

```dart
List<String> names = ["Harry", "Ron", "Harmoine"];
print(names);
// [Harry, Ron, Harmoine]

print(names[1]);
// Ron
```

### Adding Elements to list

To add elements to a list, you could use the `.add()` function.

```dart
List<String> names = ["Harry", "Ron", "Harmoine"];
names.add("Malfoy");

print(names);
// [Harry, Ron, Harmoine, Malfoy]
```

### Removing Elements from list

To remove elements from a list, you could use the `.remove()` function.

```dart
List<String> names = ["Harry", "Ron", "Harmoine", "Malfoy"];
names.remove("Malfoy");

print(names);
// [Harry, Ron, Harmoine]
```

## Functions

Functions are the building blocks of readable, maintainable, and reusable code. A function is a set of statements to perform a specific task.

```dart
void myFunc() {
    print("Hello!");
}

void main() {
    myFunc();
    myFunc();

    // Hello!
    // Hello!
}
```

### Parameters

The parameters are essentially the (names of) values that you could pass onto a function.

```dart
void myFunc(String name) {
    print("Hello, ${name}!");
}

void main() {
    myFunc("Elon");
    // Hello, Elon!
}
```

### Return

To *return* a value from a function, we use the `return` statement.

```dart
int square(int num) {
    return num * num;
}

void main() {
    print(square(6));
    // 36
}
```

## If Statement

`If` statements are used to execute a code block, if a given condition evaluates to be `true`.

```dart
if (num1 > num2) {
    print("Number 1 is greater than number 2!");
}
else {
    print("Number 1 is not greater than number 2!");
}
```

### And/Or

To combine conditons, `&&` or `||` operators could be used.

```dart
if ((num1 > num2) && (num1 > num3)) {
    print("Number 1 is greater than number 2 and 3");
}

if ((num1 > num2) || (num1 > num3)) {
    print("Number 1 is greater than number 2 or 3");
}
```

- `!` is used to negate a result
```dart
bool result = 5 > 3;
print(!result);
// false
```

### Else if

```dart
if (num1 > num2) {
    print("Number 1 is greater than number 2!");
}
else if (num1 > num3) {
    print("Number 1 is greater than number 3!");
}
```

## Switch Statement

The switch statement evaluates an expression, matches the expression???s value to a case clause and executes the statements associated with that case.

```dart
String a = stdin.readLineSync();
switch(a){
    case '+':
        print("You entered +");
        break;
    case '-':
        print("You entered -");
        break;
    default:
        print("Invalid!");
}
```

## Loops!

### While Loop

The while loop executes the instructions each time the condition specified evaluates to true.

```dart
i = 0
while (i < 3) {
    print(i);
    i++;
}
```

### For Loop

The for loop executes the code block for a specified number of times.

```dart
for(int i = 0; i < 3; i++){
    print(i);
}

// 0
// 1
// 2
```

The for loop also could be used to iterate through a fixed set of values (*such as a list*).

```dart
String stones = ["space", "mind", "reality", "power", "time", "soul"];
for(String stone in stones) {
    print(stone);
}
// space
// mind
// reality
// power
// time
// soul
```

## Classes

Dart is an object-oriented language. It supports object-oriented programming features like classes, interfaces, etc. 

A class in terms of OOP is a blueprint for creating objects. A class encapsulates data for the object. Dart gives built-in support for this concept called `class`.

```dart
class Car {
    String name;
    int year;
    String type;
}

void main() {
    Car ferrari = Car();
    ferrari.name = "LaFerrari";
    ferrari.year = 2018;
    ferrari.type= "Sport";

    print(ferrari.year);
    // 2018
}
```

### Constructor

*Constructors* are functions used to initialize the object values with data.

```dart
class Car {
    String name;
    int year;
    String type;

    Car(String name, int year, String type){
        this.name = name;
        this.year = year;
        this.type = type;
    }
}

void main() {
    Car ferrari = Car("LaFerrari", 2018, "Sport");

    print(ferrari.name);
    // LaFerrari
}
```

### Class Methods

Classes could also have its own functions, called as `methods`.

```dart
class Car {
    String name;
    int year;
    String type;

    Car(String name, int year, String type){
        this.name = name;
        this.year = year;
        this.type = type;
    }

    bool isFast(){
        return this.name == "LaFerrari";
    }
}

void main() {
    Car ferrari = Car("LaFerrari", 2018, "Sport");

    print(ferrari.isFast());
    // true
}
```