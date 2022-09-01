---
layout: post
category: theory
---

# The title says Linear Algebra but let's talk about a fundamental question about machine learning.

Below Ven Diagram must be familar to CS folks.
<img src="{{site.url}}/assets/images/theory/AI1.png" width="auto" height="auto" alt="AI1">

So the deep learning is basically machine learning.
And we know that machine learning is a technique making `model`

## What the heck is model anyways?

This is where the math kicks in.

let's say there is an equation
`x + 2y = 3`

What does this equation really mean?
It is not a simple question.

### Math is a subject of abstractions.
<img src="{{site.url}}/assets/images/theory/AI2.png" width="auto" height="auto" alt="AI2">
One of the easiest way to express the equation is using 2-D vector space.
From here we can see that the co-efficients determine the direction of the equation.

let's draw an another linear equation on the same plane.
`2x + y = 10`
<img src="{{site.url}}/assets/images/theory/AI3.png" width="auto" height="auto" alt="AI3">

The point where two lines meet, we call this a solution.

`x + 2y = 3`
`2x + y = 10`

When there are equations like this we call this a system.
So, this will be a linear system

The solutions can be expressed as a solution set as `(10/3, -1/6)`

This system then can be expressed as a matrix
--     --
|1 2  3 |
|2 1  10|
--     --

Now each column is a vector which represents the movement of the variable, and each row represents an equation.

Machine learning is a process of making model.
And this system that creates a solution set is a model.

Let's say we know T: average temperature today, M: average moisture rate today. and binary variable R: 1 if it rains tomorrow, 0 if it doesn't.

Then we can make an equation: `aT + bR = R`
This is for today.
What if we have a record for while year?

Then we will get a system that has 365 rows which means vector size of 365.

Now the machine learning is a process of finding that system or model.

Usually, typical machine learning is for linear models, and deep learning for non-linear models.