### Weekly Digest 5: Questions and Answers

<br/>

#### Xu asks:

> In the context of optimization problems like the assignment problem, 
> how important is it to consider both computational feasibility and optimality?

Both of these are important. The goal is to get a solution that is optimal (or as close 
to optimal as possible), and to compute such a solution efficiently. 


#### Himanshu asks:

> 1. Are there more than one way to look at the edges of the graph? Like can we define 
     the edge to be anything we want?
> 2. Are there no algorithms for paths that go back and forth along the same edge? 


1. Edges connect vertices of a graph. Vertices and edges can represent various 
   things, depending on a particular application. 
2. Powers of the adjacency matrix of a graph compute the number of paths, where paths 
   can use repeatedly the same edge. Computations of paths that do not repeat 
   any edge are more complicated and in general take more time.


#### Grace asks:

> Are the network style graphs related to the topic of applied linear algebra in that matrices 
> can help us solve info about the graph? Or is there another way in which it is all connected, 
> like bipartite graphs representing the assignment problem?

Graph theory is connected to linear algebra in many different ways. 
I will explain a few more such connections in this course.


#### Zhen asks:

> 1. Why is finding the minimum vertex cover important in graph theory, and how does it relate 
>    to optimization problems? 
> 2. How does understanding different types of paths in graphs contribute to solving complex network 
>    optimization problems?

1. The problem of finding a minimum vertex cover **is** an optimization problem. Beside direct 
   application of this problem, it is very closely related to other problems in graph theory:
   finding a maximum independent set of a graph, a maximum clique etc. 
2. Various problems in graph theory are related to studying paths in a graph, and some will involve 
   paths of a specific type: simple paths, Hamiltonian paths, cycles etc. 


#### Xin asks:

> Can we get minimum vertex cover from other places? I think this knowledge is more abstract and 
> similar to topology.

"Cover" has many different meanings in mathematics. In particular, in topology we often use covers 
of topological spaces. However, "verted cover" and "minimum vertex cover" are notions specific to graph 
theory. There are several different ways of associating a topological space to a graph (or vice versa), 
so graph theory does have various relationships to topology. 


#### Sean asks:

> Do these topics, especially the ones related to graph theory have any applications in finance?

Linear and integer programming are very often used in finance, for example for portfolio optimization
or capital budgeting. Graph theory (or network theory) are used too, see e.g. 
<a href="https://link.springer.com/book/10.1007/978-3-319-09683-4" target="_blank">this book</a>.


#### Aurora asks:

> What is the purpose of having multiple edges between vertices, as in can multiple edges be 
> represented as one instead, but simply weighted more if there are more connections?

It is true that instead of considering multiple edges between vertices we can use weighted edges.
However, sometimes using multiple edges may be more intuitive. For example, one of the first
graphs studied in mathematics was the graph of 
<a href="https://en.wikipedia.org/wiki/Seven_Bridges_of_K%C3%B6nigsberg" target="_blank">bridges of Königsberg</a>.
In this graph every vertex represents a different part of the city of Königsberg (two shores of a river 
and two islands on the river), and each edge is a bridge connecting two of these parts. In this case it 
is more natural to use two edges to indicate that there are two bridges connecting the same parts of the city, 
than to have one edge of weight two. 


#### Jonathan asks:

> What's the difference between a simple graph and an undirected graph?

A simple graph does not have multiple edges and self-edges (i.e. edges that start and end at the same vertex).


#### Samuel asks:

> If you could put everyone on earth in to a matrix, could you prove the theory that everyone 
> is connected by at most six degrees of separation. 

Yes. For this, we could take the adjacency matrix $$A$$ of the graph showing connctions between people, 
and compute the sum of its first 6 powers $$A^1 + A^2 + \dots + A^6$$. Entries of this matrix would 
give the number of ways any two people can be connected either directly or indirectly through at most 
six acquaintances. If this matrix would not contain any zeros, it would mean that any two people are 
connected in this way, so there are at most 6 degrees of separations between them. 


#### Quinquan asks:

> All the graphs that we saw in class were either directed or undirected. 
> Can we have a graph with directed and undirected edges at the same time?

It would be possible to define such a graph, but I have not seen this used anywhere. 
In cases where it could be useful, it would be probably easier to use a directed graph, 
by replacing each undirected edge by two directed edges going in both directions. 
