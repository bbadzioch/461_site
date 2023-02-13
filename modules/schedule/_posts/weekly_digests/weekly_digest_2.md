### Weekly Digest 2: Questions and Answers

<br/>


#### Stephanie asks:

> Are there similar things to linear programs but instead wants to maximize
> functions which are not linear? Like what if we had multiple constraints
> that were all nonlinear. Would it follow the same format of solving linear
> programs or something completely different.

There are many types of optimization problems with objective functions and constraints
given by non-linear functions. For example, in quadratic programming contraints are
still linear, but the objective function is a second degree polynomial of several
variables. For different types of problems there are different methods of solving them,
usually more complicated and slower than for linear programming.


#### Chase asks:

> You noted that "The extreme points in the feasible region correspond to all
> possible basic feasible solutions", when we were specifically referencing simplex form.
> Do the extreme points of a feasible region correspond to all basic feasible solutions
> of a matrix NOT in basic form? I have a gut feeling that the answer is no.

A matrix in the basic form is convenient for reading off a basic feasible solution,
but modifying any matrix to this form using elementary row operations does not
change the feasible region, the extreme points or what are the basic feasible solutions.
Starting with any matrix, a basic feasible solution can be computed by first selecting
a maximal collection of columns of the matrix that are linearly independent. The variables
corresponding to these columns become basic variables and the other variables are free.
Then we set the free variables to 0, and compute values of the basic variables.
The complication is that if a matrix is not in the basic form, then computing the values
of basic variables requires some work. This work amounts to reducing the matrix to the
basic form.


#### Giacomo asks:

> If a linear programming problem produces an unbounded feasible region, is it
> still possible for the simplex method to find the maximum if it exists?

Yes, the simplex method always finds the maximum if it exists. If the maximum
does not exist it will detect it too. Thus, it will always solve a linear
programming problem.


#### Huixin asks:

> 1) I am still not clear about the slack values for when do we need them? Is it used to make
>    an inequality form become an equality form? Are slack values always larger than zero no matter
>    the sign of the inequality form?
>
> 2) How do we find a feasible solution by setting all the basic variables equal to zero? Because we
>    got a new equality form with two free variables and an unknown z (example in note 5, page 18),
>    but didn't get the exact values of the two variables yet.

1) Slack variables are used to convert inequality constraints to equalities. We usually want
   all linear programming variables to be greater or equal to 0, so slack variables are added in a way
   that this condition is satisfied. After a linear programming problem is solved, it may happen that
   some slack variables for the optimal solution will be 0.

2) By the definition of a basic feasible solution, this is a solution where all free variables are
   equal to 0. The notes on page 18 show how one can modify the objective function so that it depends
   on free variables only. This is not directly related to basic feasible solutions.


#### Yuzhang asks:

> Are all of the equations applied to the `scipy.optimize.linprog` package getting the minimum
> points?

Yes, this function always looks for the minimum of the objective function. But of course any
maximization problem can be converted into a minimization one by multiplying the objective function
by -1.


#### Nicholas asks:

> Is it possible for multiple columns in a basic matrix to have the same identity matrix columns?
> i.e. column one is $$[1, 0, 0]$$ and column five is also $$[1, 0, 0]$$.

Yes, and this creates a complication in the simplex method that may slow it down
in some cases (but the simplex method will still find the optimal solution). I will talk about it later.


#### Carter asks:

> Are we expected to be able to compute the simplex method by hand?

Yes, and I will explain how to do it. While virtually all practical linear programming problems
are too large to be solved manually, being able to solve small problems by hand should give a better
insight how the simplex method works.


#### Keith asks:

> 1. When we have an unrestricted real variable x in a linear program, and we want to write the program
>    in some standard form, I'm still a little unclear how decomposing x into x+ and x- helps to solve
>    the problem.

> 2. In week 1, I asked whether the matrices we will be working with would also represent linear transformations.
>   I believe that you answered not often. Still, it seems to me that some features of matrices used to solve
>   systems of linear equations and of those representing linear transformations are somehow bound up together;
>   infeasibility seems somehow connected to null space, for example. I haven't studied linear algebra in several
>   semesters, so I may well be off the mark.

1. This is a trick that lets us represent an unrestricted variable as a difference of two non-negative
   variables. This accomplishes the goal of having a linear program where all variables are non-negative.
   This condition is essential for the simplex method to work.

2. I may have misspoken, we will quite frequently consider matrices as representing linear
   transformations. This perspective is perhaps less visible in linear programming, but it will be more useful
   later. I am not sure how to relate the null space of a matrix to infeasibility, but maybe I am overlooking
   something. We can talk about it.


#### Alice asks:

> What is an example of an objective function in a unbounded feasible region that has a maximum?

For a very simple example, assume that there are two objective variables $$x_1$$ and $$x_2$$,
there is only one constraint $$x_2 \leq 1$$ and the objective function is $$z = x_2$$. The
feasible region is unbounded since $$x_1$$ can be arbitrarily large, but the objective function
has the maximum $$z = 1$$.


#### Zoe asks:

> Are there more efficient algorithms than the simplex method?

Theoretically, the interior point method can be more efficient than the simplex method
in same cases of linear programs. Practically there is not much difference though, since
linear programs in which the simplex method would be significantly slower are rarely
encountered.


#### Jonah asks:

> During class, we went over a constraint which was represented as an equality. This equality was then
> converted into two inequalities. Does having two inequalities instead of one equality increase the amount
> of labor needed to solve a linear programming problem? Are there cases where it is beneficial to minimize
> the total number of constraints? Are there other cases where it is beneficial to have all constraints
> represented as inequalities instead of including both inequalities and equalities?

Introducing more constraints or more variables may indeed increase the number of computations
needed to solve a linear programming problem. It is helpful though to set up a problem in some uniform
form - either with all constraints given by equalities or given by inequalities. Otherwise the process
of finding a solution would be more complicated since we would need to consider various cases,
depending on the type of constraints.


#### Alan asks:

> In class you were talking about how with an increase number of constraints and variables that the time to
> find the optimal solution would increase exponentially. Obviously the simplex method works great to reduce
> the runtime, but is there a sort of "divide and conquer" method that would be ultimately log*linear
> that exists too?

The most efficient algorithms solve linear programming problems in polynomial time (more or less
$$O(n^{2.5})$$) in the number of variables. The simplex method in the worst cases requires exponential
time, but in practice it almost always finds the solution in polynomial time too.


#### Nicholas asks:

> I got stuck on the first homework problem. It seemed simple at first, but I quickly got confused by when to
> produce and when to store. I may be overcomplicating it, but at one point I had recursively defined the number
> of widgets for one month by the previous month.

This should not be very complicated. I can have at look at what you came up it after class or
during office hours.


#### Pavan asks:

> Why exactly are slack variables needed to solve problems? In real life applications, what's
> their significance?

Slack variables are used to bring a linear program to the equality form.
They are just a technical tool for replacing inequality constraints by equalities.


#### Anthony asks:

> For basic feasible solutions, are we always to consider the minimum solutions to our free variables?
> Is it possible if you can elaborate on the geometric interpretation of the feasible solutions?
> I cant necessarily grasp my hand around it without considering coordinate planes which is an issue,
> especially for equations with greater than 3 variables.

Basic feasible solutions by definition are obtained by setting free viariables to 0. Since
we assume that all variables are non-negative, this is indeed the minimum possible value of
these variables.

Geometrically, feasible solutions correspond to all points of the feasible region. Basic feasible
solutions correspond to the extreme points (i.e. corners) of the feasible region. The maximum and
minimum of the objective function will always occur in one of these corner points.