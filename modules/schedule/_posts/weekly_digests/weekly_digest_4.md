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
  is the smallest possible. Here $$\lambda$$ is a parameter that we set to some value. Different
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
   program are integers the solution will in almost all cases involve fractions.

2. The only difference between linear programming and integer programming is that in integer programming we are looking
   for an maximal/minimal solution where all variables are integers. The value of the objective function at this optimal
   point does not have to be an integer though. Integers are the arguments of this function, its values can be any numbers.
