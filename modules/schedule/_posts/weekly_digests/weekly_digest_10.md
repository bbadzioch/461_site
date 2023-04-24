### Weekly Digest 10: Questions and Answers


<br/>

#### Stephanie asks:

> Is the variance and covariance similar to standard deviation?
> Why do we use one and not the other?

Standard deviation is just the square root of variance. It provides
essentially the same information about the distribution of data as
variance. In some cases it is more convenient to use variance,
while in other settings standard deviation is a more natural choice.

#### Carter asks:

> How is the $$\frac{1}{2N^2}$$ constant of the intuitive form of variance
> derived and is there a geometric interpretation as to why it is that value?

The definition of variance is $$\text{Var}(X) = \frac{1}{N}\sum_i (x_i - m_X)^2$$
which means that we are taking the average of squares of differences between data
values and the mean data value. Here $$\frac{1}{N}$$ is used since we
are computing an average of $$N$$ values. We can equivalently compute variance
using the formula $$\text{Var}(X) = \frac{1}{2N^2}\sum_{ij} (x_i - x_j)^2$$. The
constant $$\frac{1}{2N^2}$$ is needed so that both of these formulas are the same.
I am not sure if this constant can be given a more intuitive interpretation -
it is just what comes out from computations.


#### Chase asks:

> One of our covariance definitions is as follows: $$Cov(X,Y) = \frac{1}{2N^2}\sum_{ij}(xi - xj)(yi - yj)$$.
> The number $$(x_i - x_j)(y_i - y_j)$$ can be negative or positive, depending on the $$x$$ and $$y$$ values
> These positive and negative values can possibly cancel out each other, in the summation. This would make the
> $$Cov(X,Y)$$ smaller. This definition of covariance allows for vectors with extreme positives and extreme negatives
> to present themselves as low covariance. In terms of data analysis, this seems extremely strange. Especially considering
> that our definition for variance accounts for this, because variance is always $$\geq 0$$.
>
> Is my understanding of covariance correct? Is it possible for vectors with extreme positives and extreme
> negatives to present themselves as low covariance?

Yes, this understranding is correct. Variance and covariance are simple measures that help us get some
insight into the distribution of data. They are not perfect though and sometimes they can be misleading.
The issue with covariance that you described applies to variance as well. If we have data
where almost all values $$x_i$$ are exactly the same with the exeception of one value which much bigger
or much smaller than the rest, then the variance of the data will be large, even though almost data
is concentrated in a single point. In data analysis people deal with such situations using various methods,
for example by removing outliers before analyzing the data.


#### Yuzhang asks:

> I am curious what is the closet vector. And what's the application for orthogonal projections?

I guess you mean the "closest vector"? When I was talking about the orthogonal projection of a vector $$v$$
onto a vector $$u$$, I mentioned that the projection $$\text{proj}_u v$$ is the vector which is the closest
to $$v$$ among all vectors that go in the same direction as $$u$$.

Orthogonal projections are used in many applications. We will use them to get a geometric
interpretation of the first principal axis and the first principal component of a data matrix.


#### Yingkun asks:

> I found that $$\|u_1\|= 1$$ is an important condition. In Quadratic froms, if $$A$$ is a symmetric matrix,
> $$u_1$$ is an eigenvector and corresponds to the largest eigenvalue, then $$\|u_1\|= 1$$. And, in
> the first principal component, $$\|u_1\|= 1$$, Then the variance of the vector of $$Au_1=Y_1$$ formed by
> it is the largest possible. In addition, there is the same requirement for $$\|u_1\|= 1$$ in orthogonal
> projections. Why $$\|u_1\|= 1$$ must be equal to 1  to construct these properties? Is there anything special
> about $$\|u_1\|= 1$$?

It is not true that the eigenvector corresponding to the the largest eigenvalue (or any other eigenvalue) of
a matrix must satisfy $$\|u_1\|= 1$$. If $$u_1$$ is an eigenvector then so is $$cu_1$$ for any scalar $$c$$,
so eigenvectors can have any length. It is true though that for any eigenvalue we can find an eigenvector
satisfying $$\|u_1\|= 1$$ and sometimes it is useful to use such a vector.

Similarly, for orthogonal projections it is not needed that $$\|u_1\|= 1$$, but some formulas are a bit simpler
when a vector satisfies this property.

For the first principal component the assumption $$\|u_1\|= 1$$ is more important since we are ultimately looking
for a maximum of a quadratic form, and such maximum does not exist unless we restrict the length of vectors.
We could use $$\|u_1\|= 5$$ or $$\|u_1\|= 123$$ instead, but $$\|u_1\|= 1$$ is more natural and it simplifies some
formulas.


#### Nick F. asks:

> Does $$\| v − \text{proj}_u v\| = \|v − cu\|$$ in the case that $$u = v$$?

If $$u = v$$ then $$\text{proj}_u v = v $$, so the left hand side is 0.
The value of the right hand side is $$|1 - c|\cdot \| v \|$$ which can
be any positive number, depending on what $$c$$ is.


#### Nick L. asks:

> What is the first principal axis used for?

This is a tool for sumarizing data. Multiplying a data matrix by its first principal
axis vector gives a data vector where each row of the data matrix is replaced by
a single number. Moreover, the vector obtained in this way preserved as much of the total
variance of the original data matrix as possible. As the next topic of the course
we will also look at a geometrical interpretation of the first principal axis.


#### Giacomo asks:

> In class, when discussing variance and covariance, you kept mentioning phrases similar
> to " we want to see how much information we can keep"... or something along those lines.
> I never quite understood what you meant by that. If you can recall what I am talking about,
> could you elaborate on it a bit? Thank you.

We can use the variance of data as some measure of how much information the data holds.
Bigger variance means that differences between different data values are larger, so
it should be easier to distinguish between these values. This general interpretration
in general can be misleading. However, it is useful to compare the total variance of
a data matrix with the variance of the first principal component of the matrix, and
to interpret this as a measure of the amount of information that the first principal
component retrieves.


#### Alice asks:

> To calculate the covariance (page 98), would we just use the proposition equation rather
> than the one in the definition?

Both formulas give the same value. In practice, the formula in the definition is easier
to use since the summation is taken over only one index, while in the proposition it is
taken over two indices. The formula in the proposition gives possibly an easier
interpretation of what covariance is.


#### Pavan asks:

> In 26. Review of Orthogonal projections (page 109) for the Proposition's proof (Line 2),
> shouldn't there be a negative sign before the dot product?

Yes, this is a typo. Luckily since the dot product is 0, it does not change the computation.


#### Alan asks:

> Is it possible to view the answers for the HW 4? I spend a couple of days and a ton of
> time reviewing lecture notes to solve problem 4, but I felt that I could not get to the hint,
> nor could i use the hint to solve the problem.

The idea is that $$\lambda$$ is an eigenvalue of the Laplacian if and only if $$k - \lambda$$
is an eigenvalue of $$A$$ (with the same eigenvectors). Since the smallest eigenvalue of
the Laplacian is $$0$$, thus the largest eigenvalue of $$A$$ is $$k$$. I can explain the details
after class, during the office hours etc.


#### Hixin asks:

> Why is that $$\frac{1}{N}\sum (x_i - m_X)^2 = \frac{1}{2N^2}\sum (x_i - x_j)^2$$ (the $$\text{Var}(X))$$?
> Similarly, Why does $$\frac{1}{N}\sum (x_i - m_X)(y_i - m_Y)$$ equal $$\frac{1}{2N^2}\sum (x_i - x_j)(y_i - m_Y)$$
> (the $$\text{Cov}(X,Y)$$)?

It is quite easy to check that these formulas produce the same values. I left this computation
as an exercise.


#### Keith asks:

> You mentioned in class that finding maximum and minimum values of quadratic forms is important.
> I read that these max/min problems are important in geometry for describing quadric surfaces,
> and for simplifying the classification of extrema. In particular, the second-order term in
> the Taylor expansion of a $$C^{2}$$ or better function $$f$$ is a quadratic form $$x^THx$$, where $$H$$
> is a symmetric Hessian matrix whose orthogonal diagonalization more readily describes the local
> behavior of $$f$$.
>
> My nascent understanding relates this classification of extrema to the classification of quadratic
> forms we were discussing prior to last week. Since $H$ describes all second-order partial derivatives
> at a point, if $$x^THx$$ is positive definite, then all eigenvalues of $$H$$ are positive and $$f$$ increases
> in all directions about that point, which is therefore a minimum. Similarly, if $$x^THx$$ is negative definite,
> then $$f$$ decreases in all directions. Is this correct?
>
> What are some other important reasons for working with quadratic forms, and for identifying their
> max/min values given a set of vectors? Also, can you say something about the sets of vectors? What sorts
> of sets are interesting here, apart from geometry?

With regard to the extreme values of a function: you are right as long as the point $$x$$ is a critical point, i.e.
the first derivative of $$f$$ vanishes. Calculus III textbooks usually include a second derivarive test
to classify extreme points of functions of 2 variables. This test does not mention quadratic forms but it is
derived from the classification the quadratic forms defined by the Hessian.

Quadratic forms are related to many branches of mathematics: they define Clifford algebras that have application
e.g. in differential geoemtry, they are studied in algebraic geometry and number theory, they show up in
algebraic topology etc.


#### Jonah asks:

> What exactly does the covariance of two vectors measure? Are there any particular applications
> of knowing the covariance? In the notes, it mentions that if the covariance of two vectors X and Y
> is positive, then on average the value of vector Y increases as the value of vector X increases.
> Although I'm unsure how this information could be helpful.

Positive or negative covariance indicates that there is some linear relationship between the two data vectors.
For example, if we would discover that there is a positive covariance between data recording heights of
students and their calculus exam scores, then it would be an indication that taller students tend to
do better in calculus.


#### Anthony asks:

> What can we interpret from demeaning a vector?

Demeaning tells us how data values differ from the mean of the data:
after demeaning positive values are the ones that are above the mean,
and negative values are below the mean.

