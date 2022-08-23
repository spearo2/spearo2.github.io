---
layout: post
category: theory
---

# Number System & Codes

## Number System

### Type 1. Postive-value system

    Ex) binary, decimal, octal, etc.

There exist the most significant digit (MSD) and the least significant digit (LSD).
Number closer to the MSD is always bigger than the one closer to the LSD.

Ex) MSD : .<span style="text-decoration:underline">1</span>82A  <span style="text-decoration:underline">3</span>BC.E42F (in hexadecimal).
    LSD : .182<span style="text-decoration:underline">A</span>  BC.E42<span style="text-decoration:underline">F</span> (in hexadecimal).

    #### Example 1. decimal number system

    Most frequently used number system. Represented with 0~9 numbers.
    Each digit represents powers of 10. ex) 1234 = 1 x 10^3 + 2 x 10^2 + 3 x 10^1 + 4 x 10^0

    #### Example 2. binaray number system

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


    #### Example 3. octal number system

    Each digit is represented with number 0~7 and it represents the power of 8.

    Since 2<sup>3</sup> = 8, an octal-to-binary conversion can be easily done by converting 3 binary digits into one octal digit.

    Ex) 327<sub>8</sub> = 11 010 111<sub>2</sub>

    Converting decimals(0<x<1) is same but left to right.

    Ex) 0.125<sub>8</sub> = 0.001 010 011<sub>2</sub>


    #### Example 4. hexadecimal number system

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

