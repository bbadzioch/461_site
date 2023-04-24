### Weekly Digest 11: Questions and Answers


<br/>

#### Chase asks:

> When we are working with the 3rd principal axis,
> is it orthogonal to **both** the 1st principal axis and the 2nd?

Yes. Principal axes are given by orthogonal eigenvectors of the covariance
matrix, so each axis is orthogonal to all other axes.


#### Giacomo asks:

> The motivation for finding the first principal component is clear.
> However, it is not clear to me why we care about subsequent principal components.
> What kind of information can we obtain from these subsequent components?

The second principal component is by definition the first principal component
of the difference matrix between the original data matrix and the projection matrix.
The projection matrix encodes all information that can be obtained using the first
principal component and the first principal axis. This means that the second principal
component summarizes the information that is not captured by the first component.
In the same way, the third principal component provides a summary of the information
which is not captured by the first two principal components etc.


#### Stephanie asks:

> Why are we interested in finding any principal component/axis after the first one?
> What do those mean graphically?

Please see my response to Giacomo's question above. I will talk more about the
geometric interpretation of further principal components and principal axes in class.


#### Yuzhang asks:

> I am wondering what is the difference between the 1st principal axis ($$_u_1$$) and the 1st
> principal component ($$Y_1$$)?

The first principal axis of a data matrix $$A$$ specifies how colummns of $$A$$ need to be combined
to get the largest variance. The first principal component is the linear combination of columns
of $$A$$ obtained in this way: $$Y_1 = Au_1$$.


#### Nick F. asks:

> For a demeaned matrix, are there only as many principal components as there are eigenvalues?

For a data matrix $$A$$ the number of principal components is equal to the number of columns
of $$A$$. This number is the same as the number of linearly independent eigenvectors of the
covariance matrix $$C_A$$. This is not always the same as the number of eigenvalues, since
an eigenvalue can correspond to several linearly independent eigenvactors.



#### Alan asks:

> Are there only up to the number of points amount of total principal components or can
> it potentially go further than that? Like in the example in lecture 28 there are 6 points
> so I would expect there to be just 6 principle components.

For a data matrix $$A$$ the number of principal components is equal to the number of columns
of $$A$$ i.e. the number of features of the data. In the example you mentioned there are only
two principal components since the matrix has two columns. Using the first $$k$$ principal
components we can approximate the data, and the approximation gets better as $$k$$ increases.
Using all principal components we can recover the original data exactly.


#### Alice asks:

> Is it PCA that is used in machine learning?

Yes.


#### Nick L. asks:

> 1. Can you explain the ith principal component on page 119?
>
> 2. Does this mean that the 2nd principal axis of $$D$$ is the 3rd principal axis of $$A$$?


1. I plan to talk more about it in class.
2. Yes, this is correct.


#### Pavan asks:

> I know there's computation concerned with finding the 1st principal component and
> so on for demeaned matrices. But what's the real purpose behind demeaning data?
> How does it help with data analysis?

From the point of view od statistics, demeaning splits data into two pieces that are
easier to deal with separately. One is the mean of the data and the second is the demeaned
data. Demeaned data is more convenient for analysis since its center (i.e. its mean) is
at the origin of the coordinate system. Also, no information is lost in the process since
if we want to recover the orginal data from demeaned one we can simply add the mean.


#### Keith asks:

> 1. Let $$A$$ be an $$n\times n$$ data matrix and $$C$$ be its corresponding covariance matrix.
> If I understand correctly, since $$C$$ is symmetric, it is diagonalizable, and therefore
> has $$n$$ linearly independent eigenvectors, but not necessarily $$n$$ distinct eigenvalues.
> $$A$$ itself need not have $$n$$ linearly independent eigenvectors.
>
> 2. When it comes to principal component analysis, if the number of normalized eigenvectors of
> $$C$$ is greater than the number of distinct eigenvalues of $$A$$ (and $$C$$), then there will
> be $$n$$ principal components of $$A$$, but some of these principal components will have the
> same variance, since they correspond to the same eigenvalue. Is all of this correct?


1. The matrix $$A$$ is rarely square. In the example we used in class, with exam scores, the matrix
would be square only if the number of exams was equal the number of students taking them. For
this reason $$A$$ typically does not have eigenvalues and eigenvectors. On the other hand,
every matrix has a singular value decomposition, and for a data matrix $$A$$ this decomposition
is closely related to to PCA.

The covariance matrix $$C$$ is symmetric, so it is orthogonally diagonalizable. Moreover $$C$$ is
positive semidefinite, i.e. all its eigenvalues are non-negative.

1. This is correct. An additional complication is that if an eigenvalue of $$C$$ has more than one
linearly independent eigenvector, then these eigenvectors need not be orthogonal to each other. However,
in such case we can use the Gram-Schmidt process to orthogonalize them.


#### Carter asks:

> Would there be an advantage to changing basis on the data set so that we had basis vectors
> corresponding to the line with the first principal aXis and the second basis being the second
> principal aXis etc.

This is precisely what PCA does. The principal axes form a new, better basis for the data and the principal
components are coordinates of the data taken with respect to this new basis.


#### Huixin asks:

> 1. Do we obtain further principal axes and principal components of $A$ in order to obtain the minimum
> possible of $$\sum \|{S_i}^T - \text{proj}_{u_i} {S_i}^T\|^2$$? And thus the maximum possible
> $$\text{Var}(Y_i)$$ can be computed out?
>
> 2. In general, we should pursue keeping the variance as small as possible in real life. Why do we want to get
> the largest possible of $$\text{Var}(y_i)$$?

1. Yes, this is the goal.

2. I am not sure why you wrote that we should keep the variance small. In some applications this may be the case.
However, in the context of PCA variance gives a measure of the amount of information that a principal component
contains, so bigger variance is better.


#### Yingkun asks:

> We know that Difference matrix $$D = A - P$$. $$A$$ is Demeaned data matrix and $$P$$ is projection matrix.
> I am a little bit hard to visualize the structure of this matrix. Could you give me a more
> detailed explanation of D?

I will talk more about it in class.

#### Anthony asks:

> Why do we want to focus on projections of demeaned data matrix?

The goal (at least for the first principal component) is to replace multidimensional data
with one dimensional in a way that changes the data matrix as little as possible.
This is accomplished by projecting the data onto the first principal axis.
