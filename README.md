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
    // I'm a comment, and the computer is going to ignore me :'(

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

