### Weekly Digest 10: Questions and Answers

<br/>

#### Aurora asks:

> How are quadratic forms used in application? 
> What scenarios or problems do quadratic forms normally come up in?

We already used a quadratic forms defined by the Laplacian of graphs for spectral 
partitioning of the graphs. We will use quadratic forms again for principal 
component analysis, which is a technique very often used in data analysis.


#### Himanshu asks:

> 1. What do you mean when you say something is "semidefinite"?
> 2. How does classfying the quadratic form help us in the real world? Could you give some examples?

1. It does not mean anything by itself. It is terminology used in the context of 
   quadratic forms and a few related notions. For example, positive semidefinite form is a form 
   whose values are are only positive numbers and 0. 
2. Quadratic forms are used in practice (we have used them already for spectral partitioning, 
   and we will use them again for the principal component analysis). Classification of quadratic forms 
   is a part of the theory that comes useful in such cases. For example, spectral partitioning works
   because the Laplacian of any graph has non-negative eigenvalues. This is the same as saying that 
   the quadratic form defined by the Laplacian is positive semidefinite.


#### Xu asks:

> How do we diagonalize a quadratic form, and what significance does this process hold?

Diagonalization amounts to computing eigenvalues and their associated eigenvectors. 
Diaganalization enables us to classify quadratic forms, solve for them optimization 
problems etc. 


#### Samuel asks:

> Out of curiosity, if you were given a matrix in the quadratic form, 
> can you find the original matrix?

If you mean that we are given the symmetrized matrix, and we want to recover
from it the matrix before symmetrization, then it is not possible. Many different 
matrices have the same symmetrization. 

#### Jonathan asks:

> What does the Cheeger constant mean? 

It is a number, assciated to a graph, which provides some measure how hard it is 
to partition a graph. Larger Cheeger constant means that more edges need to be cut
in order to split the graph into pieces. 

#### Grace asks:

> How can we use quadratic form in optimization problems?

This is the next topic I will talk about in class. 


#### Angelo asks:

> A question I have is on page 2 of the lecture note 21. I see $$V_S = [1,1,-1,-1,-1 ]$$ 
> with 1, 2, 3, 4, 5 on the right of it. Do we have multiple -1 values because those are 
> the nodes in the other circle? Nodes 3, 4, and 5 are in the other circle so I am guessing 
> we have -1 multiple times to represent the nodes in the different circle. If that is the 
> case is it possible for there to be an intersection and what would that value be?

This was an example of a selector vector, which indicates how a graph is partitioned, 
i.e. which of its vertices are in a set $$S$$ and which vertices are in the complementary 
set $$\overline{S}$$. By definition, there is never a vertex that belongs to both these sets, 
so there is no third value of the vector. 


#### Quinquan asks:

> What is the role of orthogonal diagonalization in the context of quadratic forms? 
> Like does it simplify quadratic forms associated with symmetric matrices?

Diagonalization lets us, essentially, reduce the study of quadratic forms to the study of 
forms represented by diagonal matrices. Such forms are easy to classify, solve optimization 
problems with etc. 


#### Quinquan asks:

> My question is, when I was doing problem 2 on the homework I was researching things related to 
> the problem and went down a rabbit hole and found something called dynamic programming. 
> Is that related to anything we do in this class? 

Dynamic programming is a technique used to solve certain optimization problems in mathematics 
and also to structure various algorithms in computer engineering. It could be applied to write 
code that searches for solutions of some problems we encountered in this course (minimum vertex 
cover etc.).
