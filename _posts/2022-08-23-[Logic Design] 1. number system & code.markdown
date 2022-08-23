---
layout: post
category: theory
---

# Number Systems & Codes

## Number Systems

### Type 1. Postive-value system

Ex) binary, decimal, octal, etc.

There exist the most significant digit (MSD) and the least significant digit (LSD).
Number closer to the MSD is always bigger than the one closer to the LSD.

Ex) MSD : .<span style="text-decoration:underline">1</span>82A  <span style="text-decoration:underline">3</span>BC.E42F (in hexadecimal).
    LSD : .182<span style="text-decoration:underline">A</span>  BC.E42<span style="text-decoration:underline">F</span> (in hexadecimal).

#### Type 1-1. decimal number system

Most frequently used number system. Represented with 0~9 numbers.
Each digit represents powers of 10. ex) 1234 = 1 x 10^3 + 2 x 10^2 + 3 x 10^1 + 4 x 10^0

#### Type 1-2. binaray number system

Each digit represents powers of 2 and only represented with 0 or 1.

Ex) 111<sub>2</sub> = 1 x 2<sup>2</sup> + 1 x 2<sup>1</sup> + 1 x 2<sup>0</sup>

Converting a binaray number to a decimal number is simple.
In above example,
Ex) 111<sub>2</sub> = 1 x 2<sup>2</sup> + 1 x 2<sup>1</sup> + 1 x 2<sup>0</sup> = 7<sub>10</sub>
    1.111<sub>2</sub> = 1 x 2<sup>0</sup> + 1 x 2<sup>-1</sup> + 1 x 2<sup>-2</sup> + 1 x 2<sup>-3</sup> = 1.875<sub>10</sub>

However, converting vice versa could be tricky.

Ex       2 | 13             x2 | 0.125
            -----               -------
        2 |  6  ...1       x2 | 0.25 ...0
            -----               -------
        2 |  3  ...0       x2 | 0.5  ...0
            -----               -------
            1  ...1            0    ...1

    13<sub>10</sub> = 101<sub>2</sub>     0.125<sub>10</sub> = 0.01<sub>2</sub>


#### Type 1-3. octal number system

Each digit is represented with number 0~7 and it represents the power of 8.

Since 2<sup>3</sup> = 8, an octal-to-binary conversion can be easily done by converting 3 binary digits into one octal digit.

Ex) 327<sub>8</sub> = 11 010 111<sub>2</sub>

Converting decimals(0<x<1) is same but left to right.

Ex) 0.125<sub>8</sub> = 0.001 010 011<sub>2</sub>


#### Type 1-4. hexadecimal number system

Each digit is represented with number 0~9, A, B, C, D, E, F and it represents the power of 16.

Hexadecimal numbers are useful because it is easy to convert from binary, decimal, and octal number systems.

Ex) 2AF<sub>16</sub> = 2 x 16<sup>2</sup> + 10 x 16<sup>1</sup> + 15 x 16<sup>0</sup> = 687<sub>10</sub>

    16 | 423            
        -----          
    16 |  26  ...7      
        -----         
            1   ...10      

    423<sub>10</sub> = 1A7<sub>16</sub>

    1011 1010 0111<sub>2</sub> = BA7<sub>16</sub>                   

### Type 2. Fixed-point number

This type of number system considers how to represent positive and negative numbers.


#### Type 2-1. sign-magnitude system

- Most popular style using + and - signs to represent both positive and negative numbers.
- It could possibly cause serious problems in computer systems due to the coexistence of +0 and -0.

#### Type 2-2. 1's complement representation

We take 1's complement by using bitwise operators NOT.

For example, we know that +6<sub>10</sub> = 0000 0110<sub>2</sub>.
From here, this representation take -6<sub>10</sub> = 1111 1001(this is not equivalent to a binary representation).

In 1's complement representation, the MSD is 0 for positive integers and 1 for negative integers.
(It depends on the systaem, but here we use 8-bit notation to see if a digit is positive or negative)

However, arithmatic expressions could be unstable due to the same reason in the type 2-1.

#### Type 2-3. 2's complement representation

Simply, it is it is 1 + '1's complement representation'

So, 
6<sub>10</sub> = 0000 0110<sub>2</sub>
-6<sub>10</sub> = 1111 1001<sub>1's complement</sub>
-6<sub>10</sub> = 1111 1010<sub>2's complement</sub>

* 2's complement representation can be converted to opposite sign by
1) subtract 1 and take 1's complement representation of it.
2) take 1's complement representation then add 1 to it.

Both ways are equivalent(<a href="https://www.cs.cornell.edu/~tomf/notes/cps104/twoscomp.html">proven by mathmatical induction</a>).

Obviously, there is a limit for each representation
For example, 7-bit representation can only express -128 to 127.


#### Type 2-4. floating-point representation

This particular representation is often used.
Each representation is divided into 3 parts. Significand, base, and exponent.

For example,
<img src="{{site.url}}/assets/images/theory/ld1.png" width="auto" height="auto" alt="ld1">
-Source:Wikipedia-

For binary representation, there are <span style="text-decoration:underline">1) single-precision floating-point representation</span> and <span style="text-decoration:underline">double-precision floating-point representation.</span>

It uses a following formula.

(-1)<sup>S</sup> (1+F) 2<sup>E-127</sup>

1)single-precision floating-point representation

significand (S) is 1 bit, exponent is 8 bits, and fraction is 23 bits.

2)double-precision floating-point representation

significand (S) is 1 bit, exponent is 8 bits, and fraction is 55 bits.

For example, if it is a single precision floating-point representation and each parts are as follows,

<img src="{{site.url}}/assets/images/theory/ld2.png" width="auto" height="auto" alt="ld2">




## Codes

In communications and information processing, code is a system of rules to convert information

I would like to justify it as a system of rules with embedded meanings.

In logic design, codes are represented with

1) bit (0 or 1)
2) nibble (1 nibble = 4 bits)
3) byte (1 byte = 8 bits)

There are various types of codes in extension of above 3.

### Type 2. Straght Binary Coding

Simple binary coding with the most basic rule of binary number system.

327<sub>8</sub> = 11010111<sub>2</sub>

### Type 2. Binary Coded Decimal(BCD or 8421 code)

4 bits code system.

Ex) 327<sub>137</sub> = 0001 0011 0111<sub>2</sub>

This coding method is advantageous because it has no rounding error.

Ex) Straight Binary Coding: 0.6 = 0.10011001100....
    BCD: 0.6 = 0000. 0110

However, This method does not use binary representation within one 4-bit elements above 10(as the name implies).
Ex) 1010, 1011, 1100, 1101.... are not used.

Also, Expressions are usually long, therefore requires more computation.


### Type 3. Grey Code

### Type 4. Parity bit

### Type 5. ASCII, American Standard Code for Information Interchange

<img src="{{site.url}}/assets/images/theory/ld3.png" width="auto" height="auto" alt="ld3">