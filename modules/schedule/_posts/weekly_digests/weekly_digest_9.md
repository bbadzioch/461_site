### Weekly Digest 9: Questions and Answers

<br/>

#### Aurora asks:

> Are there various forms of the spectral partitioning algorithm? 
> If so, what are they, how do they apply to problems, and what makes 
> them different from the one we are discussing in class?

There are various ways in which spectral partitioning can be used. One can use 
several eigenvectors (instead of just one) either to split a graph into more 
than two pieces, or to improve the results of splitting into two pieces. 
It is also possible to apply spectral partitioning to the situation when either 
edges or vertices have some associated weights. There are other variations too.


#### Zhen asks:

> 1. Why do we use a Laplacian matrix to look at networks, and how is it different 
     from just a list of which points are connected?
> 2. How does drawing a network help us figure out how to break it into parts?

1. The starting assumption to the partitioning problem is that the graph is connected, 
   so the list vertices that are connected would be the list of all vertices of the graph. 
   The Laplacian matrix is used for the partitioning problem which seeks to divide the graph 
   while cutting the smallest possible number of edges. 
2. The usual application is the opposite of what you suggest: knowing how to partition a graph, 
   may help us create a better plot of the graph. Vertices that are in the same partition 
   should be drawn closer together, since they are more tightly connected. 



#### Jonathan asks:

> Are all square matrices symmetric? 

No. 


#### Xin asks:

> Why orthonormal is important with condition (1') and (3) 

Orthonormality is not important for stating these conditions, but the fact that 
the Laplacian matrix is symmetric, and so it is orthonormally diagonalizable, 
helps to find a solution to the relaxed partitioning problem. 


#### Xu asks:

> How do we determine the optimal number of partitions for a given graph? 

The spectral partitioning method as I explained it, splits a graph into two 
parts. It is possible to modify it to get a splitting into a bigger number 
of pieces. One  such modification involves using eigenvectors of the Laplacian 
together with the k-means clustering algorithm. In such case, it is possible 
to use some techniques related to k-means, such as the elbow method, to try to estimate 
the optimal number of partitions.


#### Grace asks:

> What are the benefits of spectral partitioning?

Partitioning by itself provides useful information about a graph, which groups 
of vertices are more tightly connected and also how difficult it is to split 
the graph into pieces. Since computing the exact optimal partitioning of a graph 
is difficult, spectral partitioning is one of the methods used to get an approximation 
of the optimal partitionining in a way that is computationally efficient. 


#### Samuel asks:

> Is there any way to tell quickly just by looking at a matrix that it has $$n$$ 
> linearly independent eigenvectors?

For matrices that are in some special forms (e.g. are symmetric) it is possible.
In general, no. 


#### Himanshu asks:

> 1. What happens when the value of $$\lambda_2$$ is zero?
> 2. How do you calculate vector $$u_2$$ (from the example we did) if we did not have the code for it? 

1. This would mean that the Laplacian has at least two linearly independent 
   eigenvectors for the eigenvalue 0, which implies that the graph is not connected. 
2. In general, if we have an eigenvalue $$\lambda$$ of a matrix $$A$$, then the corresponding 
   eigenvectors are the vectors in the null space of the matrix $$A - \lambda I$$. The nulspace
   can be computed using row reduction. There are also other ways of computing eigenvalues and
   eigenvectors, I will talk about it somewhat later. 


#### Quinquan asks:

> How minimizing the Cheeger constant can lead to balanced partitions in a graph? 
> Is it because of the minimized edges in graph partitioning?

The Cheeger constant is a number that can be computed for a graph, and that expresses 
how tightly connected the graph is. Bigger Cheeger constants means that we have to cut 
more edges in order to partition the graph. The Cheeger constant has a fixed value for 
each graph, so it cannot be minimized. 
