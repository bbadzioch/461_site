### Weekly Digest 7: Questions and Answers

<br/>

#### Xin asks:

> I have a question about the April 8th Monday class because I just received an hour ago, 
> it will be canceled or remotely?

There will be no class that day. I would really prefer these questions to relate to the 
course content though.


#### Aurora asks:

> How would you figure out which singular vertices does the resulting matrix 
> the code calculates be in location on the plot? 

I updated
<a href="{{site.baseurl}}/assets/notebooks/connected_components.html" target="_blank">the notebook</a>
I used in class to show labels of vertices. This is controlled by the argument `with_labels` of 
the function  `nx.draw_networkx`. Setting this argument to `True` shows vertex labels, setting it 
to `False` hides the labels. As it is common in Python, vertices are labeled starting at 0, so 
the vertex corresponding to the first row and the first column of the adjacency matrix is the vertex 
number 0 and so on. 


#### Himanshu asks:

> 1. Did we find a formula for finding the average dimension of $$\text{Null}(S)$$ given $$n$$ and $$m$$?
> 2. Why do gigantic components happen? Like is it some feature of the random library in python?

1. I will need to ask for a clarification of this question: I am not sure what is $$S$$, $$m$$ and $$n$$ here. 
2. This is a feature of random graphs. One can prove that under some assumptions a randomly generated graph 
   will have one and only one giant component. 

#### Grace asks:

Does graph sparsity affect the efficiency and accuracy of the linear algebraic methods for analyzing graph 
connectivity? If so, what are the implications?

There are special methods for performing various computations with sparse matrices. They are usually much 
faster than generic methods, that work for all matrices. 

#### Sean asks:

> Who was the main pioneer of linear programming?

George Dantzig would be probably considered as one, since he invented and published the simplex method. 
However, linear programs were used and even solved using similar methods before Dantzig by Fourier, 
Kantorovich, Leontief, Koopmans and others. 


#### Zhen asks:

> 1. What are the differences between Integer Programming and Linear Programming?
> 2. What are some common methods or algorithms used to solve Integer Programming problems?

1. In integer programs the goal is to find an optimal solution consisting of integers. 
   In linear programs a solution can consist of arbitrary real numbers. Integer programs 
   are much more difficulat to solve in general. 

2. The main two methods of solving integer programs are branch-and-bound and Gomory's cut. 
   Both of these methods involve repeatedly solving linear programs. Often these two methods 
   are used together to speed up computations. 


#### Xu asks:

> How does the connectedness of a graph impact its properties, such as traversal algorithms 
> and network reliability?

In order to traverse the whole graph starting from a single vertex, the graph must be connected. 
I am not sure what you mean by network reliability. 


#### Jonathan asks:

> How do you permute the columns of a table?

Permutation is rearrangement. Thus you permute columns of a table but arranging them in 
some different order. 


#### Quinquan asks:

What is the minimum number of edges required for a graph with n vertices to be connected?

$$n-1$$ edges. 
