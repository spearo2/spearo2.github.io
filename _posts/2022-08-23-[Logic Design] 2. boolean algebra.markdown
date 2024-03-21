<!-- ---
layout: post
category: theory
--- -->

# Boolean Algebra

Boolean as we know refers to a variable which is either true or false (1 or 0).
Let's check few basic terms.

- Binary Logic: Logic composed of <span style="text-decoration:underline">binary</span> variables and <span style="text-decoration:underline">logical operations</span>.

Boolean Variable ~ Binary Variable.

Logical operations are expressions consisting of famouse bitwise operatiors NOT, AND and OR (!, && and ||).
Also, there are NOR, NAND, XOR, and XNOR.

`These Operations are expressed by`
1. boolean expressions
2. truth tables
3. logic gate.

Let's look at how each operations can be expressed.

## OR Operation

-Y = A + B
-Y = A or B

-Gate Symbol
<img src="{{site.url}}/assets/images/theory/ld_or.png" width="auto" height="auto" alt="or">

-Truth Table

<img src="{{site.url}}/assets/images/theory/ld_ortt.png" width="auto" height="auto" alt="and_tt">

## AND Operation

-Y = A x B = AB
-Y = A AND B

-Gate Symbol
<img src="{{site.url}}/assets/images/theory/ld_and.png" width="auto" height="auto" alt="and">

-Truth Table

<img src="{{site.url}}/assets/images/theory/ld_andtt.png" width="auto" height="auto" alt="and_tt">

## NOT Operation

-Y = A'
-X = Complement of A

-Gate Symbol
<img src="{{site.url}}/assets/images/theory/ld_not.png" width="auto" height="auto" alt="not">

-Truth Table

<img src="{{site.url}}/assets/images/theory/ld_nottt.png" width="auto" height="auto" alt="not_tt">

* Note that OR is + and AND is x. This refers to the order of performance.

NOT --> AND(x) --> OR(+)

Ex) Y = A'B + C = 1 (When A=B=C=1)

## Question
Convert the given circuit to an equation
<img src="{{site.url}}/assets/images/theory/ld_circuit1.png" width="auto" height="auto" alt="circuit1">

Ans)
X = (A+B)(B+C)+C

## NOR Operation

-Y = (A+B)'
-Y = A NOR B

- Gate Symbol & Truth Table
<img src="{{site.url}}/assets/images/theory/ld_nor.png" width="auto" height="auto" alt="nor">

## NAND Operation

-Y = (AB)'
-Y = A NAND B

-Gate Symbol & Truth Table
<img src="{{site.url}}/assets/images/theory/ld_nand.png" width="auto" height="auto" alt="nand">


* From here, It gets less intuitive. So I added Ven diagram.

## XOR Operation

* This Operation only takes two inputs due to its characteristics.

-Y = 'AB + B'A

-Ven diagram
<img src="{{site.url}}/assets/images/theory/ld_xor_vd.png" width="auto" height="auto" alt="xor_vd">

-Gate Symbol & Truth Table
<img src="{{site.url}}/assets/images/theory/ld_xor.png" width="auto" height="auto" alt="xor">


## XNOR Operation

-Y = AB + A'B'

-Ven diagram
<img src="{{site.url}}/assets/images/theory/ld_xnor_vd.png" width="auto" height="auto" alt="xnor_vd">

-Gate Symbol & Truth Table
<img src="{{site.url}}/assets/images/theory/ld_xnor.png" width="auto" height="auto" alt="xnor">

Finally, two things to keep in mind.

## Number of Possible Funtions IF ...

inputs are 2 --> 2<sup>4</sup>
inputs are 3 --> 2<sup>8</sup>
inputs are 4 --> 2<sup>16</sup>

Because 2 boolean variable can make four combinations.

## Duality Principle

For any boolean expression consisting of AND and OR operators, swapping 0 and 1 as well as swapping + and x does not change the output.