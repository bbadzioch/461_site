### Weekly Digest 5: Questions and Answers

<br/>


#### Xu asks:

> How does König's Theorem apply in the context of bipartite graphs?

König's theorem I explained in class deals explicitly with the 
assignment problem. Since every assignment problem has an associated 
bipartite graph, this theorem can be reformulated in terms of bipartite 
graphs. 

There is also a different König's theorem on bipartite graphs. 
It says that the size of a maximum matching set of a bipartite 
graph is the same as the size of a minimum vertex cover of this graph. 


#### Sean asks:

> Not a super technical question but can these topics be applied to neural networks, 
> I know classical graph theory applies so I am wondering if the topics we are discussing 
> have any relevance?

There are two ways to look at this. One is, if these topics can be used to study 
neural networks, design neural networks etc. I don't know this. Neural networks have 
underlaying graphs, but they involve much more structure: activation functions, 
training algorithms etc. A different question is, if neural networks can be used 
to solve problems in graph theory (e.g. the assignment problem, finding a minimum 
vertex cover of a graph etc.). There has been quite a lot of research done in this 
direction, comparing speed and accuracy of computations done using neural networks
to other methods, such as linear and integer programming. See  e.g. 
<a href="https://ieeexplore.ieee.org/document/8371290" target="_blank">this</a> or
<a href="https://digital.library.adelaide.edu.au/dspace/bitstream/2440/121335/1/Gibbons2019_MPhil.pdf" target="_blank">this</a>.
The conclusion seems to be that there are tradeoffs. For example, the simplex method 
will always solve the assignment problem correctly, but sometimes slower than a neural 
network. However, a solution found by a neural network is not guaranteed to be always 
correct. 


#### Grace asks:

> How are unimodularity and Cramer's rule connected? 
> And how does that all connect back to integer programming?

In class I explained how Cramer's rule can be used to show that the incidence matrix 
of a bipartite graph is totally unimodular. This, in turn, implied that the linear 
program for an assignment problem always has an integer solution, so it is actually 
gives a solution of an integer program. 


#### Aurora asks:

> 1. When was Konig's Theorem developed and discovered?
> 2. What other methods are we going to use to solving other network problems?

1. Around 1915. 
2. We will stay with networks for a few weeks. I will show how to use 
   various linear algebra methods to find the number of connected components of 
   a network, perform spectral partitioning of a network etc. 


#### Jonathan asks:

> How can you quickly tell when there's a solution for an assignment problem?

There are various theorems that help with this, König's Theorem that I started 
explaining last week is one of them. 


#### Samuel asks:

> In Konig’s theorem does $$j$$ have the same value as $$i$$? 

These are indexes of job candidates and job positions, respectively.
They are not the same. 


#### Angelo asks:

> A question I have is regarding the bipartite graph in lecture note 14. 
> I am having a difficult time understanding why the two bipartite graphs 
> are considered to have no solutions. Is it that $$P_1$$ and $$P_3$$ need to connect 
> to another $$C$$ value other than $$C_1$$ to say the bipartite graph has a solution? 

Yes. In this example, two positions $$P_1$$ and $$P_3$$ have only one 
candidate $$C_1$$ who is interested in them. Since a candidate can be hired
for only one position, it is not possible to fill all positions in such case. 


#### Quinquan asks:

> Cramer's Rule is primarily designed for solving systems of linear equations. 
> How Cramer's Rule can be extended to solve systems of nonlinear equations. 
> What challenges arise in applying it to nonlinear systems?

I don't know of extensions of Cramer's rule to nonlinear equations. Some systems of 
nonlinear equations can be linearized, and then Cramer's rule can be used to solve 
them. 