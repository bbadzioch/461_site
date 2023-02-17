### Weekly Digest 3: Questions and Answers

<br/>


#### Chase asks:

> Imagine a computer program that calculates an answer to a simplex linear system.
> Does degeneracy cause the program to calculate super slow? I imagine it would,
> considering it would have to take into account all of the previous extreme nodes
> it's been to already.

Degenerate basic feasible solutions can slow down the simplex method, but usually
not very significantly. It is not necessary to keep a record of all solutions that
have been visited in previous steps. It is possible to use some fairly simple rules
(called anti-cycling rules) to decide how to perform each pivot step. These rules
assures that even when we need to go through several degenerate solutions in a row,
we will not get back to a solution we have seen already.


#### Giacomo asks:

> Would it be possible to see a comparison of the simplex method and some other method
> of solving these types of problems? I wonder in what circumstances the other methods
> would be more efficient and in what circumstances the simplex method is superior.

There are two sides to this. One is theoretical: theoretically, how many computations
we need to do with the simplex method and with other methods to get the solution.
It is known that in the worst possible cases, the simplex method will be much slower
than the interior method or the ellipsoid method (for any number $$n > 1$$ one can design
a linear programs where the siplex method will be $$n$$ at least times slower).
A more interesting, but harder question is how this comarison looks on the average.
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

Yes, the simplex method is finished when all coefficients of free variables in the
objective function are negative. At that point it is not possible to change the
values of free variables anymore to increse the objective function, which means that
we reached the maximum.
