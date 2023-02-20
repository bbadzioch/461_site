### Weekly Digest 3: Questions and Answers

<br/>


#### Chase asks:

> Imagine a computer program that calculates an answer to a simplex linear system.
> Does degeneracy cause the program to calculate super slow? I imagine it would,
> considering it would have to take into account all of the previous extreme nodes
> it's been to already.

Degenerate pivot steps can slow down the simplex method, but usually
not very significantly. It is not necessary to keep a record of all solutions that
have been visited in previous steps. It is possible to use some fairly simple rules
(called anti-cycling rules) to decide how to perform each pivot step. These rules
assure that even when we need to go through several degenerate solutions in a row,
we will not get back to a solution we have seen already.


#### Giacomo asks:

> Would it be possible to see a comparison of the simplex method and some other method
> of solving these types of problems? I wonder in what circumstances the other methods
> would be more efficient and in what circumstances the simplex method is superior.

There are two sides to this. One is theoretical: theoretically, how many computations
we need to make with the simplex method and with other methods to get a solution.
It is known that in the worst possible cases, the simplex method will be a lot slower
than the interior point method or the ellipsoid method.
A more interesting but harder question is how this comarison looks on the average.
We take, say, all possible linear programming problems with $$n$$ variables, compare
the number of computations for different methods for each of these problems, and
take the average of these comparison. This is a subject of active research, but the general
conclusion is that the simplex method is in this setting comparable to the other methods.

The second possible comparison is practical: if we enter some problem into a linear
programming software, how fast can we get a solution. Here, in practice, the speed
is more dependent on the implementation details of the software than on the algorithm
used. Some software packages using the simplex method can be a lot faster than other
packages using the same method.


#### Yuzhang asks:

> Is the simplex method only used for finding the maximum and minimum?
> What will be the other application for the simplex method?

Simplex method is a method for solving linear programming problems. It is also used in
interger programming - a topic that we will deal with next.


#### Nick L. asks:

> Will questions using the simplex method always be over when all free variables
> are negative?

Yes, as long as the linear program has a maximum (i.e. is bounded), the simplex method
is finished when all coefficients of free variables in the objective function are negative.
At that point it is not possible to change the values of free variables anymore to increase
the objective function, which means that we reached the maximum.


#### Zoe asks:

> When using the simplex method, can there be a case where $$z$$ decreases between steps
> (like a local maximum) before finding the true maximum or is $$z$$ always increasing or
> staying the same?

In linear programming problems there are no local maxima, only a global maximum (as long
as a maximum exists i.e. the problem is bounded). The value of $$z$$ increases at every step
of the simplex method or, in the worst case, it stays the same at degenerate pivot steps.


#### Alice asks:

> For the simplex method, is the method the same if the feasible solution does not include
> the coordinates $$(0,0)$$? How do we know if no feasible solutions exists?

The simplex method works the same regardless which basic feasible solution we start from.
I will explain in class how to check if any feasible solution exists and how to find one
so we can start the simplex method.


#### Alan asks:

> What would you consider to be the most difficult topic in this course to understand?

I don't intend to make anything particularly difficult. But then, this is also a matter of
personal opinion.


#### Nick F. asks:

> If you come to a degenerate pivot step, should you try to continue on past it or try
> to go ahead in a different path to find the ideal solution?

Whenever there is an option to avoid a degenerate step i.e. if there is a non-degenerate
step we can choose instead, then we choose the non-degenerate step. However,
in some cases there is no choice - all possible pivot steps are degenerate - and then
we need to go through them before the objective function starts increasing again.

#### Huixin asks:

> Is it possible that have more than 2 variables of the objective function after the pivot step?
> If yes, do we still keep one of the variables increasing whose coefficient is positive and
> the others zero?

If you mean more than two variables with positive coeffcients, then yes, there can be a lot of
such variables. This does not change the pivot step: we choose one such variable and try to increase it.

#### Huixin asks:

> Is it possible to use simplex methods to find optimal solutions in financial models?

Sure, as long as these models lead to linear programs.


#### Yingkun asks:

> 1. The judgment of unboundedness depends on free variables coefficients. Is there any other way to judge
> unboundedness?
>
> 2. The last question of assignment1 is the code, how to upload it to gradescope?


1. Not in the simplex method.
2. It is explained in the statement of that homework question: create a screenshot or a printout
   of your computations and add it to the rest of the homework.



#### Anthony asks:

> Is it possible for a system to be both unbound and degenerate?

When we talk about degeneracy we refer to pivot steps in the simplex method that do not increase
the value of the objective function. It is possible that the simplex method will go through
degenerate steps before it discovers that the linear program is unbounded.


#### Jonah asks:

> 1. In class, we usually find the extreme points of a feasible region by drawing the graph of the constraints
> and then observing where the lines intersect. Using the simplex method, we can identify extreme points by
> starting with an initial extreme point (e.g. the origin) and then swapping one of the basic variables and
> free variables in the corresponding tableaux. Are there faster ways of finding extreme points other than
> drawing the graph or besides the simplex method?

> We could alternatively start with two constraints $$a_1 x_1 + b_1 x_2 + s_1 = c_1$$ and $$a_2x_1 + b_2x_2 + s_2 = c_2$$,
> and assuming the two lines are not parallel, we could set the two lines equal to each other and solve for
> the intersection point. Although perhaps this is simply what the simplex method accomplishes and I just don't realize it.
> Also, this method is potentially very inefficient, since if there are n constraints, then I think there are $$n(n-1)/2$$
> points of intersection that would need to be checked. I think the simplex method suffers from the same problem
> for sufficiently large n.

1. The graphing method works only for problems that have only 2 free variables, since in such cases the feasible
   region is 2 dimensional and we can draw it. In practice, linear programs have many more variables so this method
   is not an option. Computing all best feasible solutions i.e. all extreme points of the feasible region is not
   an option as well, since usually there are too many of them. The simplex method is usually quite efficient.
   There are other methods (the interior point method or the ellipsoid method) that for some linear programs will be
   faster, but on average their performance is comparable to the simplex method.

2. At each pivot step the simplex method does compute one such intersection point. However, it only computes
   intersections that increase the value of the objective function. Because of this, the simplex method
   usually skips a great majority of such intersection points and arrives to the final solutions quickly.