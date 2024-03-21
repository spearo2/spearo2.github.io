---
layout: post
category: writings
---

# Soundness vs. Completeness

## Intro

The complexity of modern programs is at the highest. No, it has been exponentially increasing. <br>
Bill Gates said in 2007 that he spends more than 3 times of cost in testing than actual software development processes.<br>
According to the report from [Meddev](https://maddevs.io/customer-university/software-maintenance-costs/#software-maintenance-vs-development-cost.), almost 90% of cost of the company goes to maintenance. <br>
It is obvious because the complexity makes it not easy to understand the behavior of a program. <br>
Many software companies are trying to solve this problem by program analysis. <br><br>
These indice don't look that intuitive.<br>
Now, let's think about Windows kernel. <br>
It is a huge program with millions of lines of code. <br>
One line edited in that massive lines of source code can possibly cause a bug. <br>
Now, if that change is BIC (bug inducing commit), how can we find it? <br>
What is making this difficult is that this change could affect thousands of lines of code. <br><br>
I think that pretty much explain why program analysis is important. <br>
When we talk about the program analysis, it can be divided into two categories: <br>
1. Dynamic Analysis<br>
2. Static Analysis<br>

## Completeness (dynamic analysis)

Completeness is one of corectness indexes for program analysis. <br>
Let's define a complete program. <br>
A complete method is a method that can prove anything that's right. <br>
On the other hand, a complete method cannot prove that a program does not have defects. <br>

For example, testing as one of the dynamic analysis methods is a complete method. <br>
If a program passes all the tests, then we can say that that program satisfies the test conditions. <br>
However, even if a program passes all test cases given, it is not necessarily bugless. <br>

## Soundness (static analysis)

Soundness is another one
A sound method is a method that cannot prove anything that's wrong. <br>
Meaning that it can only prove things that are right. <br>
Which also means that if it says that a program has a bug, it can only be either false positive or true postive. <br>
Most of the static analysis methods are sound, meaning that it can generate false alarms, yet it literally detects everything without a miss. <br>

The following figure would explain more intuitively. <br>
<img src="{{site.url}}/assets/images/theory/soundnessvsdynamic.png" width="200" height="200" alt="soundness">

## Soundness vs. Completeness
Nowadays, most of huge software companies divide up their limited resources to both static and dynamic analysis to find faults in a software. <br>
This is because the both are uniquely different and strong in their own ways. <br>
For example, static analysis has more scalability and obviously consumes incredibily small amount of resources compared to dynamic analysis. <br>
On the other hand, dynamic analysis is more accurate and more intuitive, making it more trustable. <br>
There are also cons for both. Static analysis cannot react to off-the-convention source code sturucture. <br>
On the other hand, dynamic analysis has many undcidable NPs regarding the test cases. <br>
Mathmatically, 

If Σ is a set of hypotheses, Φ is a set of conclusions, Σ ⊨ Φ means Φ is true given Σ, and Σ ⊢ Φ means Σ can prove Φ. <br>
Σ is sound if, <br>
Σ ⊢ Φ --> Σ ⊨ Φ

Σ is complete if, <br>
Σ ⊨ Φ --> Σ ⊢ Φ
<br>

## Summary
Bugless software does not exist, maybe there are, but it is not possible to find them all according to the Halting Problem. <br>
If there is an analysis method that is both sound and complete, then it would be the best. <br>
There are other indexes such as automaticness, termination, and exactness for the reasoning method of the analysis methods <br>

This is one of the most important problem in the software engineering field. <br>
Like, this is literally Turing Award winning problem. <br>