### Weekly Digest 4: Questions and Answers

<br/>


#### Stephanie asks:

> We learned how to represent the assignment problem, would it be solved
> using the simplex method? Are there different ways to approach the integer
> programs given that the matrix would be big.

Yes, my goal for the next lecture is to explain why the assignment problem
can be solved using the simplex method. That is, why the simplex method applied
to this type of a problem always gives solutions consisting of integers.

The simplex method can be used to efficiently solve linear programs with thousands
of variables, so a program of this size is not an issue.


#### Chase asks:

> In the example we did in class, why did we use integer programming?
> Is it just because the nature of having a job is binary, expressed by having a 0 or 1?
> Is that the only reason we did integer programming?

As you wrote, the decision if a person should be hired for some position
is binary, yes or no, so it is natural to set it up as an interger program with
0 and 1 values. There are also other ways of approaching the assignment problem, so
integer programming is not the only possible formalism here.


#### Yuzhang asks:

> What are the differences between L1 regression and Lasso Regression, and between L2 regression
> and Ridge Regression? Are these distinct techniques, or simply different names for the same method?

These are all different methods. Lets say that we have points $$(x_i, y_i)$$, and we want to
find a function of the form $$f(x) = ax + b$$ that best fits these points. The difference is
how we define what "best fits" means:

- **L1 regression.** We want $$a, b$$ such that $$\sum_i |ax_i + b - y_i|$$ is the smallest possible.

- **L2 regression.** We want $$a, b$$ such that $$\sum_i (ax_i + b - y_i)^2$$ is the smallest possible.

- **Lasso regression.** We want $$a, b$$ such that $$\sum_i (ax_i + b - y_i)^2 + \lambda\cdot(|a| + |b|)$$
  is the smallest possible. Here $$\lambda$$ is a parameter that we choose. Different
  choices of $$\lambda$$ will give different values of $$a$$ and $$b$$. For example, if we set
  $$\lambda = 0$$ then this becomes an L2 regression.

- **Ridge regression.** We want $$a, b$$ such that $$\sum_i (ax_i + b - y_i)^2 + \lambda\cdot(a^2 + b^2)$$
  is the smallest possible. Here, again, $$\lambda$$ is a parameter whose value we choose.



#### Giacomo asks:

> 1. As far as I can recall, all of the linear programming problems that we have encountered have had integer max/min
> solutions that correspond to integer inputs. Was this done for computational simplicity since we did these problems
> by hand? If so, then is it right to conclude that these cases are rare, i.e. it is more common for solutions and
> their corresponding inputs to these linear programming problems to not be integers?
>
> 2. Also, I would like to check my understanding of the purpose of integer programming. Integer programming is employed
> when we want our max/min value to be an integer value that also corresponds to integer inputs. Is this correct?

1. Yes, the linear programming examples I used in class (and in homework) were selected to have integer solutions in
   order to make manual computations easier. This does not happen in general. Even if all coefficients of a linear
   program are integers, the solution will in almost all cases involve fractions.

2. The only difference between linear programming and integer programming is that in integer programming we are looking
   for a maximal/minimal solution where all variables are integers. The value of the objective function at this optimal
   point does not have to be an integer though. Integers are the arguments of this function, its values can be any numbers.


#### Nick L.:

> Will there be specific instances in which L1 regression or L2 regression are more efficient than the other?

Which regression is more appropriate will depent on what one wants to accomplish. For a given collection of numbers,
the mean value of these numbers is a special example of L2 regression, while the median value is a special example of
L1 regression. Mean and median are both useful, but they provide different information about the data. The same is
true about L1 and L2 regression in general.


#### Huixin asks:

> What are the intentions for building up the (bipartite) graph $$G =(V, E)$$ and the edge incidence matrix
> of a graph $$G =(V, E)$$?

We used it to represent the assignment problem in a convenient form. In particular, using the incidence matrix
associated with the bipartite graph we can write a matrix that describes constraints of the assignment problem.


#### Carter asks:

> In what scenarios would it be better to use L1 regression as opposed to L2 regression? Is there a general identity
> governing when $$L_i$$ regression is better than $$L_j$$?

I will not get into the details of this, but there are some statistical assumptions on the distribution of
data which, if they are satisfied, justify why one type of regression is more appropriate than the other.
L2 is related to a normal distribution, L1 to a Laplace distribution. However, regression is often applied
when we don't know what statistical model the data adheres to, and then the choice is a matter of what
seems to work better in a specific case.


#### Alan asks:

> When introducing absolute values to the constraints, is it still considered a linear programming problem?
> (i.e. the least squares minimizing problem).

In the case of L1 regression, the minimization problem can be rewritten without
absolute values, and it becomes a linear program. This may not be possible in other
problems that involve absolute values.

Least squares (i.e. L2) regression requires finding a minimum of a function that
involves squares of numbers. This cannot be converted into a linear program.
However, as you may remember from MTH 309, least square problems can be reduced
to solving a system of linear equations.


#### Alice asks:

> What are the advantages of integer programming?

It is not so much a matter of advantages but applications: many problems (e.g.
the assignment problem) can be solved by solving some integer program.



#### Zoe asks:

> How do integer programs link to areas of number theory like diophantine equations?

Number theory methods can be used to help solve some integer programming problems.
Constrains of integer programs are given by linear Diophantine equations. I am not sure
if there are other connections.


#### Keith asks:

> 1. When using the simplex method to solve a maximization problem, is it possible for a variable
> just removed from a basis to have a nonnegative entry in the objective row of a simplex tableau?
>
> 2. Using simplex method: suppose I want to remove a variable s1 from a basis, adding a variable $$s2$$
> in its place, and that the corresponding columns of the coefficient matrix are $$s_1=[0 1 0]^T$$ and
> $$s_2=[u 0 v]^T$$. How can the swap be accomplished?

> 3. What are the advantages to approaching regression as a linear programming problem, rather than
> some other kind of problem? For example, as far as I know, $$A^T(A)\vec{x}=A^T \vec{b}$$ will always
> work to find a best-fit line, and it seems this formula might be preferable to solving a linear
> programming problem in many cases.

1. No, it is not possible. The interesting question is why.

2. It cannot be done. The variable that exits the basis must provide the tightest bound on the value
   of the free variable, but in this case $$s_1$$ does not bound the value of $$s_2$$ at all.

3. The formula you mentioned finds the best-fit line in the least squares sense, i.e. L2 regression.
   Linear programming can be used for L1 regression. The difference is how one measures the deviation
   of data points from the line. As I mentioned in class, it is like a difference between mean and median:
   each carries different information.


#### Yingkun asks:

> 1. I think there is a problem with the picture in the example in course note 10. For the feasible region,
> the maximum value of $$x_1$$ should be 3 instead of 6. Because $$x1+x1$$ is less than or equal to 6 in the restriction.
> Therefore, x1 should be less than or equal to 3, but the range of the feasible region in the figure is x1=6.
> So, the graph should shrink.
>
> At the same time, in the Augment Metrix of Example in course note 11 (annotated notes version), there are some
> problems that the matrix values cannot be matched. I think it is possible to rewrite an Augment Metrix.

1. This is a typo, the constraint should be $$x_1 + x_2 \leq 6$$. Thank you for bringing it up, I fixed it.

2. Good point as well, and I fixed it too.


#### Nick F. asks:

> For the augmented matrix where we combined the edge incidence matrix with the slack variable matrix,
> why was the final column entirely 1s?

This is the columns of constants. In an assignment problem all constraints are equal to 1 (when we write
the linear program in the equality form). Thus the column of constants in the augmented matrix representing
the constraints consists of 1s.

#### Jonah asks:

> Since there are infinitely many approximate solutions we can obtain using L1 regression,
> can we always expect to find a good approximate solution of an integer programming problem
> using multiple attempts at L1 regression?

L1 regression can be computed using linear programming. I am not sure though how one could use
L1 regression to solve an integer programming problem. On the other hand, interger programming
problems are usually solved using multiple attempts with linear programs.


#### Anthony asks:

> Is it appropriate to say that a bipartite graph is a graph that has no two edges that connect
> to the same pair of vertices?

No, not every graph with this property is bipartite. Bipartite means that vertices of the graph
can be divided into two groups and all edges are connecting one group with the other (i.e. there
are no edges between vertices that belong to the same group). For example, a graph of the shape of
a triangle (with three vertices and three adges) is not bipartite.


