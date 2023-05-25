

I have surveyed, researched, experimented machine learning, but I have not found anyone explaining the most basic idea what it is.

Almost everyone knows what machine learning does but it is difficult to study or even simply google what it exactly is.

Today, I would like to discuss the most fundemental idea behind it.

## The title says Linear Algebra but let's talk about a fundamental question about machine learning.

Below Ven Diagram must be familar to CS folks.
<img src="{{site.url}}/assets/images/theory/AI1.png" width="auto" height="auto" alt="AI1">

So as we can see, the deep learning is basically machine learning.
And we know that machine learning is all about making `model`

## What the heck is model anyways?

This is where the math kicks in.

let's say there is an equation
`x + 2y = 3`

What does this equation really mean?
It is not a simple question.

### Math is a subject of abstractions.
<img src="{{site.url}}/assets/images/theory/AI2.png" width="200" height="200" alt="AI2">
One of the easiest way to express the equation is using 2-D vector space.
Look at the given plane made out of x and y axis.

From here we can see that the co-efficients of the equation determine the direction of the equation.

let's draw an another linear equation on the same plane.
`2x + y = 10`
<img src="{{site.url}}/assets/images/theory/AI3.png" width="200" height="200" alt="AI3">

The point where two lines meet, we call this <span style="text-decoration:underline">a solution of the equations</span>.

`x + 2y = 3`
`2x + y = 10`

When there are equations sharing same vector space like the given example, we call this <span style="text-decoration:underline">a system</span>.
So, this will be a linear system

The solutions can be expressed as a solution set as `(10/3, -1/6)`

This system then can also be expressed as a matrix using the co-efficients.
---       ---
|1 2  3 |
|2 1  10|
---       ---

Now each rows of the matrix is <span style="text-decoration:underline">a vector</span> which represents the movement of the variable, and each row represents <span style="text-decoration:underline">an equation</span>.

Machine learning is a process of making model.
And this system that creates a solution set is equivalent to models in machine learning.

Let's say we know 

T: average temperature today
M: average moisture rate today. 
binary variable R: 1 if it rains tomorrow, 0 if it doesn't.

Then we can make an equation: `aT + bR = R`
This, however, is data just for today.
What if we have a record for while year?

Then we will get a system that has 365 rows which means vector size of 365.

Now the machine learning is a process of finding that system or model.
More explicitly, finding out the co-efficients of each equation in the system.

Machine Learning is a subject of methodologies to find a way to find approximated co-efficients.
In this way, the system or the model we made out of the system we discussed basically predicts whether it rains tomorrow. And this is done based on the data.

Therefore, it is quite clear what are important factors in machine learning.
1) Choosing a right metric/ variable/ or dataset.
2) Choosing a right method to find the co-efficients.

## Of course, in actuality, ML algorithms are more complicated than this.

Usually, typical machine learning is for linear models, and deep learning for non-linear models.

