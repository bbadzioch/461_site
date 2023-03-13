### Weekly Digest 6: Questions and Answers

<br/>


#### Stephanie asks:

> 1. Do we use vertex covers when we model traffic flow?
>
> 2. And are there disadvantages to solving a relaxed linear program rather
> than the original?

1. I don't know of such applications, but it is possible that they exist.
2. Usually the solution of a relaxed linear program will give only an approximated
   solution of the integer program we are really interested in. In some cases this
   appoximation can be helpful, but in other cases it may be too far from the solution
   of the integer program to be of use.


#### Chase asks:

> What is the significance of network theory in relation to what we are going to do with
> linear algebra applications? Are we going to be utilizing the path count from a node to
> a node? I just want to know where we are going with this.

Our next goal will be to look at some applications of linear algebra to network theory
(connectivity of networks, partitioning of networks, random walks on networks etc.).
Path counting is a small application of adjacency matrices but it will came handy later on.


#### Yuzhang asks:

> I am not sure what's the difference between the cover and vertex cover mentioned on the
> "16. Minimum vertex cover of a graph" note. Specifically, what's the difference between
> the minimum vertex cover and minimum cover?

I see that at one point in the annotated notes I wrote "minimum cover" as a shorthand
for "minimum vertex cover". There is no difference, I meant the same thing.


#### Nick L.  asks:

> When looking for maximum independent sets or cliques for application to real-world purposes,
> what would determine the best ones if there are multiple that meet the requirements of being the max set?

This will depend on a specific application. In some cases, when there are several
possible solutions it is possible to add  additional constraints to focus only
on the solution we are really interested in.


#### Carter  asks:

> Does all of graph theory boil down to linear algebra? Or do other fields of math come in too?

Linear algebra is the focus of this course, but there are many branches of mathematics that
are used in graph theory: combinatorics, abstract algebra, topology, probability theory etc.
Conversely, graph theory is used in a lot of different areas of mathematics and in many types
of practical problems.


#### Alan  asks:

> How much more complicated would the example: "Example. In the graph pictured above, how many
> paths of length 2 are there that start at the vertex 2 and end at the vertex 4?", become of
> the length desired increased to 3, or higher?

I talked about it in class. If $$A$$ is the adjacency matrix of a graph, then entries of the
matrix $$A^2$$ give the number of paths of length 2 between any two vertices, but in general
entries of the matrix $$A^n$$ give the number of paths of length $$n$$.


#### Alan  asks:

> What are the practical applications of knowing the number of paths in a graph?

This was just small application of adjacency matrices, but we will use the same approach
later for describing random walks on graphs. This in turn has many applications. For example,
it provides the basis for the Google search engine. I will explain this somewhat later.


#### Zoe asks:

> What are some uses of the minimum vertex cover of a graph?

I have mentioned a few of possible applications in class. One of them was that the complement
of a minimum vertex cover if a maximum independent set which may represent e.g. the biggest
possible number of events in some schedule that do not have time conflicts etc.


#### Pavan asks:

> I was looking at the Proposition from page 57 (From Notes 17. Paths in Graphs) and noticed
> that $$n\geq 1$$, $$c_ij$$ is the entry in $$A^n$$ that gives the number of paths of length
> $$n$$ from vertex $$j$$ to vertex $$i$$. Shouldn't there be an upper bound for n as well?

The number $$n$$ is the length of paths. The proposition is true for any value $$n=1, 2, \dots$$.


#### Huixin asks:

> If the length of the path is long enough, which means a path can go back to the vertex
> where the last path starts, how can we calculate the number of paths? In the example of
> note #17, there are just paths of length 2, so we can list all of the possibilities for
> each path from each vertex. But If the direction of a path can go back,
> I think the possibilities will be endless.

The total number of paths of all lengths will be infinite, but the number of paths of
a fixed length $$n$$ will be finite, and the proposition in then notes explains how to
count them.


#### Nick L. asks:

> Are there always $$n$$ number of eigenvalues for an $$n\time n$$ matrix?

No, a matrix can have at most $$n$$ different eigenvalues, but it can have fewer.


#### Keith asks:

> 1. How are directed bipartite graphs typically represented as matrices?
> I assume the number of edges and vertices is doubled in an incidence matrix,
> and this is how we account for edges that connect vertices in only one direction.
> Is this correct? Or is there a more efficient way of representing a directed bipartite graph?
>
> 2. Also, I learned row operations, but I recently heard that there are column operations.
> Are these essentially different from row operations, or are they just row operations on
> the transpose of a matrix?


1. A bipartite graph is a type of a graph so it can be represented by an incidence
   matrix or an adjacency matrix like any graph. There is no need to double edges or vertices.
   On the other hand, the adjacency and incidence matrices of a bipartite graph will have some
   special special properties that are not true for other types of graphs. For example, it is known
   that if a graph is bipartite, $$A$$ is its adjacency matrix and $$\lambda$$ is an eigenvalue
   of $$A$$, then the number $$-\lambda$$ is an eigenvalue as well. This property does not hold
   for graphs which are not bipartite.
2. The latter - these are row operations on the transpose.


#### Yingkun asks:

> Is the order of graph equal to the order of minimum vertex cover plus the order of maximum
> independent set ?

Yes, this is true. The order of a graph is the number of vertices of the graph. Given a minimum
vertex cover of a graph, all vertices which are not in the minimum vertex cover form a maximum
independent set. Thus taken together we get all vertices of the graph.


#### Jonah asks:

> Is there a connection between the notion of open cover (from Real Analysis) and vertex cover
> (from Graph Theory)? The vertices are like open sets and the edges are like points. A vertex cover
> is a collection of vertices such that every edge in the graph touches one of the vertices.
> Similarly, an open cover of a set S is a collection of open sets such every point of S belongs
> to one of the open sets. And a set S is compact if every open cover has a finite subcover.
> Is it possible that there exist "compact" graphs G such that every vertex cover of G has
> a subcover which is also a minimum vertex cover?

It is possible to make such a connection. A more immediate analog of compactness would be that
in a compact graph each vertex cover contains a vertex cover consisting of finitely many vertices.
For finite graphs this is always the case (since the whole graph has finitely many
vertices), but for infinite graphs it is an interesting property. The question for which graphs
every vertex cover contains a minimum vertex cover is interesting too. I don't know how to
answer it, but I would guess that there are some known results going in this direction.


#### Anthony asks:

> Does there exist a graph, $$G$$ where its complement, $$G'$$ does not exist?

No, the complement always exists. It has the same vertices as $$G$$ and all edges
that are not present in $$G$$.

