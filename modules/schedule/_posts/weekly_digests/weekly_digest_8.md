### Weekly Digest 8: Questions and Answers


<br/>

#### Stephanie asks:

> What kind of problems can we solve with graph partitioning?
> Also, i might have missed this but how did you find the Laplacian?

Graph partitioning is used to predict what is the most likely way in
which a network will split into two parts when some edges are removed.
This is applied to communications networks, social networks etc.

The Laplacian of a graph is defined $$D - A$$ where $$D$$ the diagonal degree matrix
and $$A$$ is the adjancency matrix of the graph.


#### Yuzhang asks:

> Can the Laplacian matrix be used for directed graphs?

There is no good generalization of the Laplacian to directed graphs.
This is one of the reasons why the study of directed graphs is more diffucult
than the study of undirected ones.


#### Giacomo asks:

> Could you please explain the following equivalence: $$v^TLv=\sum_i\deg(i)\cdot x_i^2=\sum_{\substack{i<j \\ i \sim j}}x_i^2+x_j^2$$
> Found on page 76 of mth461_notes_21.


The first equality comes directly from performing matrix multiplication.
The second holds since an edge between two vertices $$i$$ and $$j$$ adds 1 to
$$\deg(i)$$ and also adds 1 to $$\deg(j)$$. Thus instead of taking the sum over
all vertices we can take the sum over all edges of the graph.


#### Chase asks:

> In the relaxation problem, why do we take $$v_P^T L v_P \geq v_R^T L  v_R$$?
> What does this achieve?

$$\tfrac{1}{4} v_P^T L v_P$$ gives the smallest number of edges that need to be removed
in order to separate a set of vertices of a given size from the rest of the graph.
This number is what we are interested in, but it is difficult to compute. On the other
hand, the number $$v_R^T L v_R$$ can be calculated quite easily. The inequality gives us
an estimate of how hard it is to partition the graph: if says that to do it we need to remove
at least $$\tfrac{1}{4} v_R^T L v_R$$ edges (but perhaps more).


#### Alan asks:

> Is the solution achieved in the partitioning problem from lecture just a lower bound?
> Or will the smallest integer equal or above $$\tfrac{k(N-k)}{N}\lambda_2$$ always be the minimum?

This number is obtained from the solution of the relaxed problem, and thus it gives only a lower
bound on the minimal number of edges that need to be removed to partition the graph. The actual
minimal number of edges can be bigger than the integer obtained by rounding up $$\tfrac{k(N-k)}{N}\lambda_2$$.


#### Huixin asks:

> Does an objective function have to consist of all the decision variables? Will there be parts of the decision
> variables that are only used for constraints and other parts that compose objective function and constraints?

It is possible that only some decision variables will show up in the objective function. Equivalently,
we can assume that the objective function uses all decision variables, but some of them are taken
with the coefficient 0, so they do'nt influence values of the function.



#### Alice asks:

> What is an example in real-life situations of using a partitioning problem?

I talked about it in class. Graph partitioning can be used to detect communities
of people in social networks, check for vulnerabilities in communication or
transportations networks etc.



#### Keith asks:

> 1. In the relaxed partitioning problem, my understanding is that $$N$$ and $$|S|$$ (the number
> of nodes and the size of the set we are interested in) are givens, and we are solving
> a linear program for the selector vector that minimizes $$|E(S,\overline{S})|$$ by
> minimizing $$v^T L v$$. In condition (2) on p.79 of the notes, we have
> a chain of equations. In the second to last equation, how do we get the $N$ in
> the numerator of $$c_1\cdot\frac{N}{\sqrt{N}}$$?
>
> 2. On the syllabus, there is a list of topics that might be considered in the course.
> Will we have time to discuss many more of them? What about Markov chains, polynomial
> interpolation, and singular value decomposition?


1. The optimization problem coming from the graph partitioning is not a linear program since
   both the objective function and the constraints are not linear functions (they involve
   products of coordinates of the vector $$v$$). As for formula, it is obtained as the
   dot product $$(c_1u_1)\cdot v$$ where $$v$$ is the vector with all coordinates equal to 1.
   By definition $$u_1 = \tfrac{1}{\sqrt{N}} v$$, so
   $$c_1u_1\cdot v = \tfrac{c_1}{\sqrt{N}} (v \cdot v)$$. But $$v\cdot v = N$$.

2. We will not have time for all these topics, but we will get to some of them.



#### Carter asks:

> Is there a resource to learn more about the Laplacian's connection to the Laplace transform you
> alluded to in class?

You can have a look e.g. at the book *Networks, an Introduction* by Mark Newman, beginning of
the chapter on the graph Laplacian. Note the graph Laplacian is derived there using first derivarives
of a certain function, while the Laplace operator involves second derivatives. This is fine since
the function used in the book represents the rate of flow, so it is by itself the derivative of
a function representing the flow itself. By the way, this book gives a nice introduction to
the theory of networks with many applications.



#### Yingkun asks:

> The homework completion time this time was about a week shorter than last time. Will the future
> homework be about a week each time?

Homeworks are due two weeks after they are posted. For Homework 3 it was 3 weeks because
of the spring break.



#### Nick F. asks:

> When we say $$v \cdot [1, 1, ... 1]^T = k - (N - k)$$, does the vector need to be entirely 1s,
> or is it a selector vector that can have negative ones?

If $$v$$ is a selector vector, then this condition says that if has to have $$k$$ entries equal to 1
and $$$N-k$$ entries equal to -1.


#### Pavan asks:

> What's the application for diagonalization theorem and spectral theorem? Is it just to show relations
> between eigenvalues and eigenvectors for square diagonalizable matrices? Or are there applications
> in other Math topics which may or may not be covered in this course?

Network partitioning that we are dealing with now is one such application. The Principal Component Analysis
that I will talk about soon is another.


#### Anthony asks:

> What applications are there for graph partitions?

I talked about it in class. Graph partitioning can be used to detect communities
of people in social networks, check for vulnerabilities in communication or
transportations networks etc.


#### Zoe asks:

> How close in general is the solution of the relaxed problem as opposed to the solution
> of the partitioning problem?

The relaxed problem provides a lower bound on the number of edges that need to be removed
to partition a given graph. Later on I will talk about Cheeger inequality that gives an upper
bound of a similar form. Taken together these bounds provide a range of possible values that may
apprear in the partitioning problem.


#### Jonah asks:

> Is it possible to solve the partitioning problem by brute force? In other words can we consider
> every subset of $$V$$ containing $$k$$ points and then count how many edges are connecting the given
> subset and the complement? Perhaps this would be one way of finding the smallest number of edges.

It is theoretically possible, but practically impossible. For example, for a graph with 200 vertices
and for $k=100$ there would be more than $$10^{30}$$ subsets to check. It we could do the computations
for a billion of these subsets each second, it would take more than $$10^{13}$$ years to finish
the calculations.
