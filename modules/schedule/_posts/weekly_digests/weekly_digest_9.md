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
2. The usual application is the opposite of what you suggest: if we know how to partition a graph, 
   then it may help us to create a better plot of the graph. Vertices that are in the same partition 
   should be drawn closer together, since they are more tightly connected. 



#### Jonathan asks:

> Are all square matrices symmetric? 

No. 


#### Xin asks:

> Why orthonormal is important with condition (1') and (3) 

Orthonormality is not important for stating these conditions, but the fact that 
the Laplacian matrix is symmetric, and so it is orthonormally diagonalizable, 
helps to find a solution to the relaxed partitioning problem. 





########################
########################
########################
########################
########################
########################

#### Xu asks:

> How does the complexity of graph partitioning algorithms vary depending on 
> the characteristics of the graph, such as size, density, and structure?

It is difficult to answer this in such generality. Briefly, all known algorithms 
for finding optimal partitioning have an exponential complexity. The spectral 
partitioning method that I will explain is much faster, but it gives only 
an approximated solution. 


#### Jonathan asks:

> Why can't every matrix be diagonalizable? 

An $$n\times n$$ matrix is diagonalizable if and only if it has $$n$$ linearly 
independent eigenvectors. Some matrices do not have that many linearly 
independent eigenvectors. With some more work, it possible to give 
other, possibly more intuitive, explanations how it happens that some matrices 
are not diagonzalizable. You can read e.g. about the Jordan canonical form of a matrix.





#### Sean asks:

> What are some good online resources for extra help?

For each topic I am talking about in this course there are many online resources, 
but there is no one place that I know of that would cover them all. If there is 
anything which is unclear or that could use any additional explanation, please 
come to my office hours and I will help. 


#### Xin asks:

> What is the different between Partitioning and relaxation problems? 

The partitioning problem can take a very long time to solve for larger graphs. 
It is much easier and faster to find a solution to the relaxed partitioning 
problem. This solution can be then used to compute an approximated partitioning 
of the graph. 


#### Himanshu asks:

> Is there are a specific reason we chose $$-1$$ if i belongs to $$\overline{S}$$? 
> As generally if one condition results in $$1$$, then the other results in $$0$$.

This convention, using $$1$$ and $$-1$$ values, is makes it more convenient to state 
the relaxed partitioning problem. It would be possible to use $$1$$ and $$0$$ instead, 
but then computations would be more awkward.


#### Grace asks:

> Is there a measurement for the quality of a partition? How is the quality measured, if so? 
> How does the type of problem vary it?

The goal of partitioning is to split the graph into pieces with specified numbers of vertices, 
by cutting as few edges as possible. Depending on the context, we can add further restrictions 
which  let us decide that some partitioning is better that some other one. However, the general 
partitioning problem does not make such distinctions. 

 
#### Samuel asks:

> I know I already asked this in office hours, but, do you have an example of a graph where 
> the max clique is not the minimum number of colors needed like the hw question.

Take e.g. a graph with vertices 1, 2, 3, 4, 5 that are connected in a circular fashion. That 
is, there is an edge joining 1 with 2, 2 with 3, 3 with 4, 4 with 5 and 5 with 1. The maximum 
clique in this graph consists of two vertices, but it is easy to check that the graph cannot be 
colored with 2 colors. There is a <a href="https://en.wikipedia.org/wiki/Mycielskian">more general construction</a> 
of graphs that have only cliques with 2 vertices, but require $$n$$ colors to color them. 



#### Quinquan asks:

> What does the notation $$E(S,\overline{S})$$ mean in the context of graphs (notes 21), like 
> how does it relate to graph partitioning?

For a given graph $$G$$, $$S$$ is some subset of vertices of $$G$$ and $$\overline{S}$$ is the set 
vertices of $$G$$ that are not in $$S$$. Then $$E(S,\overline{S})$$ is the set of edges connecting vertices
in $$S$$ with vertices in $$\overline{S}$$. These are the edges that need to be removed to separate 
the set $$S$$ from the rest of the graph. 

