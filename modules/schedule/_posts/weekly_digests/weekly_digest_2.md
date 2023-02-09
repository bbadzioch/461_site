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

#### Chase asks:

> If a linear programming problem produces an unbounded feasible region, is it
> still possible for the simplex method to find the maximum if it exists?

Yes, the simplex method always finds the maximum if it exists. It the maximum
does not exist then it will detect it too. Thus, it will always solve a linear
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


