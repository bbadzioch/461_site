### Weekly Digest 4: Questions and Answers

<br/>

#### Sean asks:

> When going over the assignment problem and problems like this is there a clear 
> relation to graph theory/prevalent ideas in graph theory or was the specific 
> examples we went over in class the extent in which graph theory is used? 

There are many connections between graph theory and problems related to the assignment 
problem. We will get to some of them in this course.  



#### Xu asks:

> How $$L_1$$ regression differs from $$L_2$$ regression?

I talked about it in class. In their definitions, $$L_1$$ and 
$$L_2$$ regression use different notions of the distance 
(the sum of absolute values vs. the square  root of the sum of squares). 
In their properties, $$L_1$$ regression is less sensitive to outliers 
in the data than $$L_2$$. On the other hand, $$L_2$$ regression is almost 
always uniquely defined, while $$L_1$$ regression need not to be unique.
 

#### Aurora asks:

> 1. What other examples are integer programming used for? 
>
> 2. What scenarios are integer programming optimal?

1. A lot of problems can be representented by integer programs. We will 
see some of them in this course (minimum vertex cover, graph coloring, 
graph partitioning etc.), but the are many others (the travelling salesman problem, 
the knapsack problem etc.)

2. I am not sure if I understood the question, but if you are asking 
in what cases the (relaxed) linear program will give the optimal solution of 
an integer program, then it happens very rarely. It works for the assignment problem, 
but it is a very special case. 



#### Grace asks:

> 1. $$L_2$$ regression on its surface seems more useful than $$L_1$$ since it gives 
>    a unique solution rather than infinitely many. What is an application where it would 
>    make sense to use $$L_1$$ regression?
> 
> 2. We had discussed LP relaxation to solve integer programs, and part of this includes 
>    three different possibilities (LP solution is integer solution, gives a useful estimate, 
>    or isn't useful). Which outcome is the most common with LP relaxation?

1. It is true that $$L_2$$ regression is used more often than $$L_1$$, and non-uniqueness
   of $$L_1$$ is one of the main reasons for it. There are cases though, where $$L_1$$
   regression may be a better fit. One way to decide it, is based on probability theory: 
   $$L_2$$ regression is related to the normal distribution of the error terms 
   in the data, while $$L_1$$ regression is related to the Laplace distribution. As a side note, 
   some methods used in data analysis use a combination of $$L_1$$ and $$L_2$$, see e.g. the 
   <a href="https://en.wikipedia.org/wiki/Lasso_%28statistics%29" target="_blank">LASSO method</a>.
  
2. The LP relaxation of an integer program will almost never give integer solutions. This is 
   why the assignment problem is so special. As for the other two possibilities: useful or
   not useful estimate, I am not sure which one is more common. To some extent this is a matter 
   of coming up with the right approach. Even if one representation of a problem in the form of 
   an integer program has useless LP relaxation, it may be possible to reformulate the problem 
   and get something useful. 


#### Xin asks:

> I have a question about how long we can get our homework grade.

The first assignment should be graded sometime this week. These digest questions 
are primiarily intended to be about the course content though. 


#### Zhen asks:

> 1. In $$L_1$$ regression, how does the use of absolute values of errors impact the model’s robustness, 
>    and can you provide an example where L1 regression would be more suitable than $$L_2$$ regression?
> 
> 2. What are the main challenges associated with solving optimization problems involving discrete decision 
>    variables, and how does the branch-and-bound technique address these challenges in integer programming?

1. $$L_2$$ regression is used more often than $$L_1$$, but there are cases, where $$L_1$$
   regression may be a better fit. One way to decide it is based on probability theory: 
   $$L_2$$ regression is related to the normal (or Gausssian) distribution of the error terms 
   in the data, while $$L_1$$ regression is related to the Laplace distribution. As a side note, 
   some methods used in data analysis use a combination of $$L_1$$ and $$L_2$$, see e.g. the
   <a href="https://en.wikipedia.org/wiki/Lasso_%28statistics%29" target="_blank">LASSO method</a>.

2. Branch-and-bond is a method of solving linear programs by replacing them by many linear programs. 
   The details would go beyond the scope of this course though. 


#### Himanshu asks:

> 1. Which degenerate case does $$L_2$$ regression does not give a line? 
> 
> 2. What is the difference between $$L_1$$ and $$L_2$$ regression? 

1. If you are using $$L_2$$ regression to approximate data points $$(x_i, y_i)$$
   by a linear function, then you will always get a linear function whose graph is a line. 
   It is possible though, that this line will not be uniquely defined. This will happen 
   if all values $$x_i$$ are the same. 

 2. I talked about it in class. In their definitions, $$L_1$$ and 
    $$L_2$$ regression use different notions of the distance 
    (the sum of absolute values vs. the square  root of the sum of squares). 
    In their properties, $$L_1$$ regression is less sensitive to outliers 
    in the deta than $$L_2$$. On the other hand, $$L_2$$ regression is almost 
    always uniquely defined, while $$L_1$$ regression need not to be unique.


#### Jonathan asks:

> What is an incidence matrix?

The definition and an example are in the lecture notes 
(<a href="{{site.baseurl}}/assets/annotated_notes/mth461_annotated_notes_11.pdf" target="_blank">part 11</a>, page 39).


#### Samuel asks:

> This question is hard to ask without the image but in notes 9 when you plot $$L_1$$ and $$L_2$$ regressions 
> there are other best fit lines i can imagine for $$L_2$$. Does this graph have a flaw or are there multiple 
> ways to approach least square?

In the case shown in these notes, there is only one best fit line for $$L_2$$ regression. 
In almost all cases $$L_2$$ regression has exactly one solution. If you would like to show me what 
other possibilities you see, we can talk about it. 


#### Angelo asks:

> A question I have is about the bipartite graph. I understand that every edge connects some node in 
> $$V_1$$ with some node in $$V_2$$ but the graph itself looks messy. Is there an alternative method 
> where you can get the same results but end up with a much cleaner-looking graph?

In practical applications graphs are usually messy. This is why we need various methods 
(e.g. integer programming) to answer questions about them. 


#### Quinquan asks:

> Can the assignment problem be solved efficiently for a lot of constraints or large instances?

Yes. It can be solved using linear programming, which in general is efficient. There are also other 
methods for solving the assignment problem, e.g. the Hungarian method. 
