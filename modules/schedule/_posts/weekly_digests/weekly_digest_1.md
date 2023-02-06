### Weekly Digest 1: Questions and Answers

<br/>

#### Yuzhan asks:

> 1. I am wondering if there is any website for learning the Numpy package.
> 2. From my understanding, once the number of basic variables = the number of rows,
>   then this matrix is in a basic form. I am not sure if my understanding of a matrix
>   in a basic form is correct.

1. I would recommend the website for [*Python Data Science Handbook*](https://jakevdp.github.io/PythonDataScienceHandbook/index.html) by Jake VanderPlas.
2. No, being in basic form means that matrix is row reduced (except it is more general).
We will get back to it soon, so it should get clearer.


#### Stephanie asks:

> Are we going to learn how to solve the linear programs other than graphically?
> Are you going to demonstrate things in class using python? ( I have very little experience in python
> so i am curious and nervous)

I will explain how to solve linear programming problems using the simplex method, which is one of the
main methods used in practice.

Yes, I will show how to do various linear algebra computations using Python. I don't assume though
that everyone in this class has programming experience. It not difficult to perform some computations
without writing fully-featured Python programs.

What is does it mean for a matrix to be in basic form? This was a little unclear to me.
Is the following correct?
If an mxn matrix has m leading ones when in reduced echelon form then the matrix is in basic form.


#### Giacomo asks:

> What is does it mean for a matrix to be in basic form? This was a little unclear to me.
> Is the following correct? If an mxn matrix has m leading ones when in reduced echelon form
> then the matrix is in basic form.

No, this is not quite true. In order to be in the basic form the matrix already needs
to be essentially row reduced. I will get back to it in class.

#### Alan asks:

> Is convexity relevant in terms of linear programming? Just checking since it is linear programming
> so it seems everything will end up being convex.

We will not explicitly study it, but convexity is a crucial reason why linear programming
problems are solvable. In general, non-convex optimization problems are much more difficult
than convex ones.


#### Zoe asks:

> How would you find the exact optimal values in the examples given, is it using techniques from multivariable
> and vector calc? What do you do when you have a lot of decision variables and how quickly does it escalate
> in complexity?

I will explain how these problems can be solved. There is no need for calculus, and they can be solved efficiently
even for millions of decision variables and constraints. Of course, computers are used to do the calculations
at this scale.


#### Nicholas asks:

> I understand the theory and calculation of the growth of linear functions, but I'm not sure if I exactly understand
> its application.

In linear programming problems the objective is to find a maximum or a minimum of a linear function within
the feasible region. Understanding the behavior of linear functions is needed to see where this maximum or
minimum can occur and if it needs to exist at all. This should become clearer in this course very soon.


#### Alice asks:

> What can we do to prepare for the lectures before hand?

Reviewing the previous ones should be helpful.


#### Huixin asks:

> Do we need to bring a laptop to every class?

No.


#### Pavan asks:

> I am aware there's no textbook for this course. Could you suggest some textbook
> or any other source to learn more about the contents mentioned in this course?
> I feel that would also give me more insight and maybe even ideas for job applications.

There is no single book that I know of that would cover all material I intend to
introduce in this course. There are good books for various pieces of this material.
For example, for linear and integer programming (i.e. our first topics) "Understanding
and using linear programming" by Matousek and Gartner is very nice.


#### Carter asks:

> Will canonical forms show up in this class? Im not sure if they can be applied but
> seem interesting.

Various canonical forms of matrices have many applications. I do not plan to talk about
canonical forms in general, but they will show up in some instances. For example,
diagonalization of a matrix (if it exists) gives a canonical form, and we will use
diagonalizations several times.


#### Anthony asks:

> Will a copy of the homework be posted on Gradescope for instant access? For homework that
> involves coding, will we have to write a report on the code or just send in the code cells?

We will use Gradescope for homework submissions and grading. As for coding assignments,
there will be no full-features reports, but sometime I may ask you to provide some explanations
to go with computations.


#### Jonah asks:

When we were formulating linear programming problems, the decision variables (e.g. a_11, a_12, ... a_23)
were arranged like the entries of a matrix. Will we use matrices to solve linear programming programs?

Yes.