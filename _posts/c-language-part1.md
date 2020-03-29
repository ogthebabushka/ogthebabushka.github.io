---
layout: post
title: C Language Part 1
---

The C programming language is a computer programming language that was developed to do system programming for the operating system UNIX and is an imperative programming language. C was developed in the early 1970s. It is a procedural language, which means that people can write their programs as a series of step-by-step instructions.

## How C works?

C is a compiled language. A compiler is a special tool that compiles the program and converts it into the object file which is machine readable. After the compilation process, the linker will combine different object files and creates a single executable file to run the program.

Writing a source code(file.c) => Preprocessing a source code(file.c) => Compiling a source code(file.obj or file.o) => Linking object files(file.exe)

Nowadays, various compilers are available online, and you can use any of those compilers. Also you can use C soure code in C++ project because C++ is extended version of C language.

## Signed magnitude representation(SMR)

Signed magnitude representation is a simple method to represent signed binary numbers. The most significant bit(MSB)is used as the sign bit. If the sign bit is 0, this means the number is positive in value. If the sign bit is 1, then the number is negative in value. The remaining bits in the number are used to represent the magnitude of the binary number in the usual unsigned binary number format way.

00001 = 1, 10001 = -1

## Two`s complement

Two`s complement is a mathematical operation on binary numbers. It is used in computing as a method of signed number representation. Two`s complement is calculated by inverting the digits(One`s complement) and adding one.

Two`s complement = One`s complement + 1

001 => 110(One`s complement) + 1 = 111

## Binary operators

& - Binary AND Operator copies a bit to the result if it exists in both operands.
00011 & 10010 = 00010

| - Binary OR Operator copeis a bit if it exists in either operand.
00011 | 10010 = 10011

^ - Binary XOR Operator copies the bit if it is set in one operand but not both
00011 ^ 10010 = 10001

~ - Binary One`s Complement Operator is unary and has the effect of 'flipping' bits.
~(00011) = 11100

<< - Binary Left Shif Operator. The left operands value is moved left by the number of bits specified by the right operand.
00011 << 2 = 01100

>> - Binary Right Shift Operator. The left operands value is moved right by the number of bits specified by the right operand.
10010 >> 2 = 00100

## Recursive function

A function that calls itself is known as a recursive function. And, this technique is known as recursion.

```objc
#include<stdio.h>

int factorial(int n) {
  if(n == 1) return 1;
  else return n * factorial(n - 1);
}

int main(void) {
  factorial(100);
}
```

## Pointers

Pointers are special variable that stores/points the address of another variable. A pointer in C is used to allocate memory dynamiccaly. The pointer variable might be belonging to any of the data type such as int, float, char, double. Always C pointer is initialized to null and the value of null pointer is 0.

Pointer syntax: 
data_type *var_name; => int *p;

In C pointers and arrays are almost same.

```objc
int numbers[] = {1, 2, 3, 4, 5};
int *pointer = numbers;
printf("%d\n", pointer[1]);
```
