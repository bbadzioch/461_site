### Weekly Digest 5: Questions and Answers

<br/>


#### Stephanie asks:

> Are there other ways to solve the assignment problem?
> And would the simplex method still be reasonable to use
> If the matrix was REALLY BIG?

There are various ways of solving the assignment problem that do not
involve linear programming. In particular, the [Hungarian method](https://en.wikipedia.org/wiki/Hungarian_algorithm)
is one of the more efficient ones. The simplex method is routinely used
with problems involving thousands of variables and constrainsts.


#### Chase asks:

> These past few days have been mesmerizing. There is so many different intricate parts
> coming together when we are tackling this assignment problem.
>
> How many people were involved in making it possible to solve the assignment problem?
> How long did it take for everyone involved to get to a point where they could solve
> the assignment problem?

There were many people researching this and various related problems, and this research
goes on since people are still looking for ways to solve these problems more
efficiently.


#### Nick L. asks:

> Can you use row reduction to make any matrix into a totally unimodular matrix so it works for
> the integer program?

It is not possible to do it in general. A system of equations with a totally unimodular
coefficient matrix has the property that all its basic feasible solutions consist of integers.
Row reduction of a matrix does not change the basic feasible solutions. As a consequence, if
it would be possible to row reduce any matrix to a totally unimodular one then
a system of linear equations represented by any matrix would have basic feasible solutions
given by integers. This is not true for arbitrary systems.


#### Huixin asks:

> Could you please upload the note on the process you wrote in class? Because I am still confused
> about the outcome of note #14.

I posted all notes that I used in class so far. If there is something missing, please
let me know.


#### Alice asks:

> Are there other methods than Konigs Theorem to see if an assignment problem has a solution?

Yes. The most general one is Hall's theorem. Using the setting of job candidates being matched
with positions that we have been using, it says that a match of candidates with positions does
not exist if and only if there is some subset of $$k$$ positions such that fewer than $$k$$
job candidates are qualified for these positions. This is a stronger result than K&ouml;nig's
theorem since K&ouml;nig's theorem gives a sufficient condition for a match while Hall's
theorem gives a condition that is both sufficient and necessary. However, Hall's theorem is
more difficult to apply since we have to check all subsets of the set of available positions.


#### Carter asks:

> Will all applications covered in this course involve formulating the problem as a linear program?

Homework 3 will include a couple problems on writing integer programs.


#### Yingkun asks:

> In proposition 3 of courseware 13, I know that if A is a totally unimodular matrix and B is the column
> expansion matrix of this A matrix (a column, only one non-zero entry equal to 1), then B is totally unimodular.
> I have a Question, if the only one non-zero entry equal to -1 in the extended column in B, is B still totally
> unimodular?

Yes, the argument is the same as in the case of adding a column of the identity matrix:
we can calculate determinants by cofactor expansion along the new column.


#### Giacomo asks:

> What are other use cases of totally unimodular matrices? Also, you used the term "minor"
> when referring to part of a matrix. Could you please explain what a "minor" part of a matrix is?

The main use of totally unimodular matrices is the one I talked about: for systems of equations represented
by such matrices it is easy to obtain solutions consisting of integers.

For a square matrix $$A$$, the $$(i, j)$$-minor of $$A$$ is the determinant of the martix obtained by
removing $$i$$-th row and $$j$$-th column of $$A$$. For example, the cofactor expansion is a formula
that says how to compute the determinant of $$A$$ using minors of $$A$$.


#### Alan asks:

> Are we allowed to use a higher level simplex method on the homework than the one taught in class? The one that
> I learned was from [this textbook](http://www.math.chalmers.se/Math/Grundutb/CTH/tma947/0405/kompendium_sub.pdf)
> The class for this textbook was non-linear optimization.

I am not sure what tools you would like to use, but if you have some specific ideas, let me know..
Homework problems has been selected to be solvable using material covered in class.
Also, we will be moving away from the simplex method to different topics.


#### Keith asks:

> In other math courses, we are taught linearization as a method for solving certain problems. If a nonlinear
> function is locally differentiable near some point, then it might be possible to obtain a linear approximation there.
> Is there an analog for this in linear programming? Nonlinear programming has come up in class and in previous digests,
> but I'm asking whether there's a way to turn nonlinear optimization problems into linear programs, possibly using
> linear approximation. Or is this just what nonlinear programming is?

Some non-linear optimization problems can be converted to linear programs, but this does not work in general.
However, many optimization methods (e.g. gradient descent) rely on local linear approximation of functions.

#### Nick F. asks:

> Regarding Konig's Theorem, I don't understand why a candidate applying for at most k positions would be a constraint.
> Wouldn't having more candidates applying for positions yield a greater chance of having a solution? So we
> limit yourself to at most k?

The situation we want to avoid is a small group of people applying for a lot of positions while the rest applies
for very few. For example, one person applies for all positions, and everyone else applies for only one, the same
position. Since every person can get at most one job, in this case an assignmnet satisfying these preferences
may not exist. The assumptions of K&ouml;nig's theorem eliminate such issues.

#### Pavan asks:

> Apart from bipartite graphs, are there other instances where totally unimodular matrices are applied?

The main use of totally unimodular matrices is the one I talked about: for systems of equations represented
by such matrices it is easy to obtain solutions consisting of integers. Not every totally unimodular matrix
comes from a bipartite graph. This is true though for incidence matrices of graphs: a graph is bipartite
if and only if its incidence matrix is totally unimodular.


#### Jonah asks:

> Last class we examined some bipartite graphs and we considered if the corresponding assignment of candidates
> to jobs was possible. Can these kind of questions be solved by representing the graph as an incidence matrix?

Yes, this is essentially what we used in class.