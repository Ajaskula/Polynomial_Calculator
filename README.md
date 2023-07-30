# Introduction
A monomial of variable x is an expression of the form ax^n, where a is the coefficient and n is the degree of the monomial. The value of n, known as the degree of the monomial, is a non-negative integer. A monomial with a coefficient equal to 0 is called the zero monomial.

A polynomial of variable x is the sum of monomials of variable x. A polynomial with all zero monomials is called the zero polynomial.

The degree of a non-zero polynomial is the highest degree of its non-zero monomials. We consider the degree of the zero polynomial to be -1.

The operations of addition and multiplication are defined for polynomials.

# Project Description
Implement a calculator that calculates the sum and product of polynomials with integer coefficients.

The calculator has memory, referred to as the accumulator, which stores one polynomial. The initial value of the accumulator is the zero polynomial.

The calculator executes commands to calculate the sum and product of the current value in the accumulator and the polynomial, which is the argument of the command. The result is written to the output and stored in the accumulator.

# Input Data Format
The input data of the program is a sequence of lines with commands, terminated by a line starting with the period ... Each command occupies one line.

A line for calculating the sum starts with the + character, and a line for calculating the product starts with the * character. The subsequent characters until the end of the line are the representation of the argument of the command.

The syntax for representing a polynomial is described by the following extended Backus-Naur Form (BNF) notation, with the starting symbol <wielomian>:
```
<wielomian> ::= "0" | [ "-" ] <jednomian> { <operacja> <jednomian> }
<operacja> ::= "+" | "-"
<jednomian> ::= "1" | <dużo> | [ <dużo> ] "x" [ "^" <dużo> ]
<dużo> ::= "1" <cyfra> { <cyfra> } | <cyfra od 2 do 9> { <cyfra> }
<cyfra> ::= "0" | "1" | <cyfra od 2 do 9>
<cyfra od 2 do 9> ::= "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"
```
Curly braces {} represent zero or more repetitions, square brackets [] indicate optional parts, and the vertical bar | denotes alternatives. Auxiliary symbols are enclosed in angle brackets, and terminal symbols are enclosed in double quotes. The character between double quotes represents the corresponding symbol in the notation.

Additionally, monomials in the polynomial are ordered in descending order of their degrees.

There may be any number of spaces in the command line. However, a non-empty sequence of spaces does not occur at the beginning of the line or directly between two digits.

# Output Format
For each executed command, the program writes one line to the output with its result. The syntax for representing a polynomial in the output is the same as in the input. There is one space before and after the symbol + or - in the productions of the auxiliary symbol <operacja>. Apart from that, there are no other spaces in the output.

# Compilation
```
gcc @opcje -DPOLA=4 -DWIERSZE=10 -DKOLUMNY=7 -DWYBOR=234 Polynomial_Calculator.c -o Polynomial_Calculator
```

# Examples
Example input data files with sample commands are provided as .in files, and the expected output for each example is provided as .out files.

For the input data in the file przyklad1.in, the correct output is in przyklad1.out.
For the input data in the file przyklad2.in, the correct output is in przyklad2.out.
For the input data in the file przyklad3.in, the correct output is in przyklad3.out.
