### Weekly Digest 9: Questions and Answers


<br/>

#### Stephanie asks:

> Why is it important to find the algebraic connectivity of a graph,
> and is there reason that its the second smallest eigenvalue and not
> the smallest?

The algebraic connectivity of a graph provides an estimate how many edges
would need to be removed to split the graph into two parts of given sizes.
This privides information how tight is the structure of the graph.

The smallest value of the Laplacian is always equal to 0, so it does not
provide any information about the graph (but the corresponding eigenvectors do).

#### Yuzhang asks:

> Does the matrix of quadratic form have to be symmetric?
> If not, if the matrix of quadratic form can be in the matrix in the
> form such that $$n\times m$$, here $$n\neq m$$.

In order to define a quadratic form a matrix must be square.
Any (not necessarity symmetric) square matrix gives a quadratic form,
but we can always replace such matrix by a symmetric matric that will
define the same quadratic form. For this reason given a quadratic form
we can always assume the matrix representing it is symmetric.


#### Chase asks:

> What is the significance of all of our classfications of quadratic forms?
> Why do we have so many classificiations for them (positive definite, positive semi-definite,....,
> negative semi definite, indefinite).

This is just terminology that comes useful in many settings. Quadratic forms
of these various types behave quite differently, so it is handy to have
names that specify what kind of a form one is dealing with.


#### Nick F. asks:

> Can we use the spectral partition algorithm to calculate the maximum $$E(S, \bar{S})$$ value
> instead of the minimum value?

It is possible to use similar computations to estimate this maximum value, but
in applications it is of lesser interest.


#### Giacomo asks:

> 1. What are some real-world applications of the constrained maximum problem?
>
> 2. Also, on page 92 of mth_461_notes_22, why did we hone in on a proof for an if and only
> if condition form of the positive semidefinite quadratic forms? Are similar conditions
> for the other types of quadratic forms too difficult, or did we only focus on positive
> semidefinite because this will be the most useful form for our purposes?


1. We have already used a variant of the constrained maximum problem to develop the
spectral partitioning algorithm. We will use it again for the next topic in this course,
which will be the Principal Component Analysis (PCA) - a very useful teachique used to
analyze sets of data.

2. Than particular condition works for positive semindefinite forms, but there is a similar
contition that characterizes positive definite forms. These conditions come handy in
many applications. For example, we have used it already to show that the Laplacian of
a graph is positive demidefinite, which played a role in the spectral partioning of
a graph. The material on PCA will use this condition too.


#### Yingkun asks:

> The steps for quadratic from classification of ordinary matrices are cumbersome.
> We know before that for any matrix $$A$$, we can create a matrix $$A_S$$ so that their
> quadratic from is equal. And $$A_S$$ is a symmetric matrix. The judgment method for
> the symmetric matrix is relatively simple. Can we convert the ordinary matrix
> into $$A_S$$ every time and use the classification judgment method of symmetric matrix
> to judge the classification of this ordinary matrix A?

Yes, this is the point. When dealing with a quadratic form we can always represent
it by a symmetric matrix and then classification of the form depends only on
eigenvalues of this symmetric matrix.



#### Nick L. asks:

> Can you restate what the classification of the quadratic forms is used for?

Quadratic forms of different types behave quite differently, and it is useful to
have names for them. For example, the spectral partitioning algorithms of a graph
makes use of the fact that the quadratic form represented by the Laplacian of the
graph is positive semidefinite. In the next topic of this course which is the
Principal Component Analysis we will again make use of the fact that a certain
quadratic form we will encounter is positive semidefinite.


#### Alan asks:

> In what sort of applications is the quadratic form used to solve/make problems easier to solve?

We have already used the quadratic for defined by the Laplacian of a graph to
obtain the spectral partitioning algorithm for graphs. We will use quadratic forms
again for the next topic of this course which is the Principal Component Analysis.
This is a very useful technique for analyzing sets of data.


#### Pavan asks:

> The second smallest eigenvalue of the Laplacian of a graph G is the algebraic
> connectivity of $$G$$. Does the smallest eigenvalue in the Laplacian have any
> significance? Also, is it possible to find the Laplacian for directed graphs?

The smallest eigenvalues of the Laplacian is always 0, so it does not carry any
information about the graph. There is no good analog of the Laplacian for directed graphs.

#### Alice asks:

> Is the opposite to a constrained maximum problem just a unconstrained maximum problem?

An unconstrained maximum problem is a different problem that the constrained one,
and is not very interesting. Multiplying a vector by scalars we can always make
values of a quadratic form larger, and so an unconstrained maximum does does exist.


#### Keith asks:

> Do there exist methods for determining how a network is likely to split into more than
> two groups that are similar to the partitioning problem? If we were interested in predicting
> how a network might split in three, we could solve the partitioning problem twice, but that
> might yield a partition different from one obtained by looking for a three-way split more directly.

There are many methods for partitioning graphs. Spectral partitioning is often adapted to
split a graph $$G$$ into $$k$$ pieces by computing the Laplacian of the graph and then
pretending that $$k$$ smallest eigenvalues of the Laplacian are 0, which means that
$$G$$ has $$k$$ connected components. Then one uses the eigenvectors corresponding to these
smallest eigenvalues to determine which vertices are in the same connected component.


#### Huixin asks:

> What does the $$k$$ stand for in $$k-(N-k)$$ in note #21?

In the graph partitioning problems we want to separate a set of vertices of a graph
of a given size from the rest of the graph by removing the smallest possible number of
edges. $$k$$ is the number of vertices we want to separate.


#### Anthony asks:

> What are the benefits of using the quadratic form and are there any applications that we
> can use for graphs?

We have already used the quadratic for defined by the Laplacian of a graph to
obtain the spectral partitioning algorithm for graphs. We will use quadratic forms
again for the next topic of this course which is the Principal Component Analysis.
This is a very useful technique for analyzing sets of data.



#### Jonah asks:

> Is there a connection between quadratic forms and normal subgroups? In Group Theory,
> a subgroup $$H$$ of $$G$$ is normal if it is invariant under conjugation. In other words,
> $$ghg^{-1}$$ is in $$H$$, for all $$h \in H$$ and all $$g \in G$$. This is slightly different
> from quadratic forms, since a quadratic form $$q_A$$ maps from $$\mathbb{R}^n$$ to $$\mathbb{R}$$
> and so $$q_A(v)$$ is not an element of the original set. Suppose $$A$$ is an element of group $$G$$
> of $$n\times n$$ matrices. Are there special quadratic forms which map from $$\mathbb{R}^n$$ to
> $$\mathbb{R}^n$$, such that $$q_A(v)$$ is an element of the original matrix group? In this case,
> we would be able to ask if any of the subgroups are normal.

It you take the set of all ortogonal $$n\times n$$ matrices with matrix multiplication, then this
is a group. Given two such matrices $$A$$ and $$B$$ their conjugation is given by $$ABA^{-1}$$ = $$ABA^{T}$$
(since for an orthogonal matrix we have $$A^{-1} = A^T$$). The right hand side resembles the
definition of a quadratic form and it can be used to determine which subgroups of the group
of orthogonal matrices are normal.