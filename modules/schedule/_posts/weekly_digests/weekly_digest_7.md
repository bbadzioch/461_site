### Weekly Digest 7: Questions and Answers


<br/>

#### Chase asks:

> What do the double line brackets mean? You use them on page 7 of annotated notes 19.

I think you mean $$|| \mathbf{u} ||$$. This is the length of the vector $$\mathbf{u}$$
which is defined as the square root of the dot product of the vector with itself:
$$|| \mathbf{u} || = \sqrt{\mathbf{u} \cdot \mathbf{u}}$$.


<br/>

#### Stephanie asks:

> What is we were given constraints in the assignment problem where if person 1 got the job,
> then person 2 does not want to work with them. How do we go > about solving this?
> Can we still use a score table?

I am not sure if it is possible to formulate this as an assignment ptoblem, but it
can be still represented as an integer program, by adding some constraints to the program
respresenting the assignment problem.


<br/>

#### Yuzhang asks:

> I am not sure what the relaxed program is. And what's the difference between
> the relaxed program and the integer program?

In an integer program we are only interested in solutions that are given by integers.
In a relaxed program we drop this condition and look for solutions that can be given
by any real numbers. Since the relaxed program is a linear program, it can be solved
using the simplex method and its solutions can be used as an approximation of solutions
of the original integer program.


<br/>

#### Giacomo asks:

> What are other applications of the Laplacian outside of graph theory?

The Laplacian, as we are using it in this course, is defined for graphs and so
it is specifically used to study properties of graphs. However, in mathematics
Laplacian is also the name of a differential operator that has many applications
in real analysis, differential equations, differential geometry etc. The Laplacian
of a graph is obtained as a special instance of this differential operator.


<br/>

#### Nick L. asks:

> Will connected components in subgraphs help consistently? Or are they uncommon?

The structure of connected components is one of the main features of any graph.
If one studies some subgraphs of a given graph then usually it will be useful to look
at connected components of these subgraphs. This usefulness may depend on specific
applications though.



<br/>

#### Huixin asks:

> On the sixth page of note 19, what does "dot product of $$B^T{\mathbf v}$$ with itself" mean?
> Does it mean $$B^T{\mathbf v} \cdot B^T{\mathbf v}$$ or $${\mathbf v} \cdot {\mathbf v}$$?
> Why is the product scalar $$||{\mathbf v}||^2$$ instead of a new matrix?

It means $$B^T{\mathbf v} \cdot B^T{\mathbf v}$$. If you think about it as a matrix
multiplication, then the result is 1 $$\times$$ 1 matrix. Since this matrix has only
one entry, it can be considered as a scalar. This scalar is equal to $$|| B^T{\mathbf v} ||^2$$


<br/>

#### Carter asks:

> Is there a difference between the solve assignment function in the notes and in the homework?
> When I run the homework file it returns a non integer solution.

In the first two homework exercises the main goal is to represent the problems as
an assignment problem and compute the associated score tables. After that, the solution
is obtained the same way as we did it in class i.e. using the simplex method. You don't
need to calculate the solution manually though, since I provided the code that does the computations.
You should never get a non interger solution. If you do, please talk to me or send me an email
with results of your computations and I will check what is going on.


<br/>

#### Alice asks:

> For some of the examples in the connectedness of graphs, it is obvious that the graph is
> not connected using the adjacency matrix, can it ever be sufficient to just use the adjacency
> matrix to determine if a graph is connected?

The situations when it is easy to see that a graph is not connected by just looking at the adjacency
matrix happen usually when either the graph is small or if its vertices are given in a specific order
(all vertices of one connected component followed by all vertices of the second connected component etc.)
In practical applications graphs are usually large (with hundreds or thousands of vertices) and their
vertices come in a random order. Checking connectedness of such graph requires some computations.


<br/>

#### Yingkun asks:

> This week, I got more interested in the Laplacian of matrix. There is a direct connection between
> it and graph. For a simple graph, we have $$L = D-A$$. For the undirected graph, we have $$L = BB^T$$.
> So, for the undirected graph, does it also have a theorem to represent L?

The Laplacian matrix $$L$$ is defined for undirected graphs only. The formula $$L = D-A$$ could be
used to define an analog of the Laplacian for directed graphs, but the resulting matrix does not have
properties analogous to what we get for undirected graphs.


<br/>

#### Keith asks:

> We've considered graphs in terms of structures such as vertex covers, cliques, and independent sets.
> We've seen theorems relating these structures in simple connected graphs. Experimenting with these
> structures, I noticed that if a graph is not connected, then a minimum vertex cover might also be
> a maximum independent set, which leads me to wonder whether these structures are meaningful or important
> for the analysis of graphs that are not simple and connected.

A minimum vertex cover may be at the same time a maximum independent set even for a connected graph.
If a graph is not connected, then typically its properties are studied one connected component at a time
(since e.g. a minimum vertex cover of such graph will be the union of minimum vertex covers of the individual
components).

The notions of a minimum vertex cover and a maximum independent set make sense and are useful for graphs that
are not simple. It just becomes somewhat more complicated to represent the problem of finding these sets
as an integer program in such case.


<br/>

#### Nick F:

> Why is it relevant that the eigenvalues of a Laplacian of a graph are greater than or equal to 0?
> Is there a problem with negative eigenvalues?

Negative eigenvalues are not a problem, but the fact that the Laplacian does not have negative
eigenvalues will be important for the next topic, where we will look at partitionings of graphs.



<br/>

#### Jonah:

> Is there a connection between the Laplacian of a graph and the Laplacian of a differential
> function?

Yes, the Laplacian of a graph can be seen as a discretized version of the Laplacian defined
for functions.