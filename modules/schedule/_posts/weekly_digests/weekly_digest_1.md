### Weekly Digest 1: Questions and Answers

<br/>

#### Grace asks:

> What do we gain by having an inequality/equality form of a linear program? 
> Is this what we do to avoid graphing since there can be too many extreme points?

Bringing a linear program to an inequality/equality form is meant to make the program 
more uniform. Without this, some constraints would be given by equalities and some by 
inequalities, some variables could be only non-negative, while others could assume 
both positive and negative values. Then in the process of looking for solutions we would 
need to deal with all these various cases. By rewriting a program in, say, the equality form 
we assure that all constraints are equalities and all variables are non-negative, which makes
it somewhat to solve.


#### Sean asks:

> The only question I have is how many questions on average are the homeworks.

I am not sure, since I have not prepared all assignments yet. It will be less than 10.


#### Jonathan asks:

> In some of the notes we went took in class, for some of the $$x$$ variables, 
> there are $$x^+$$ and $$x^-$$ variables. I don't really understand why we denote these variables 
> like this,  so my question is what do these $$x^+$$ and $$x^-$$ variables mean for a problem?

This is just notation. In the equality or inequality form of a linear program we want all variables to 
satistfy the non-negativity constraint $$x_i \geq 0$$. If in the original program a variable $$x_i$$
can have any (positive and negative) values, then we can replace it by two non-negative variables $$x_{i}^{+} \geq 0$$ 
and $$x_{i}^{-}\geq 0$$, and set $$x_i = x_{i}^{+} - x_{i}^{-}$$. The notation is motivated by this formula: 
to get $$x_i$$ we add $$x_{i}^{+}$$ and subtract $$x_{i}^{-}$$.


#### Samuel asks:

> In class you put a lot of emphasis on the fact that in the real world sometime there will be thousands 
> of decision variables and constraints. What is an example where this is the case? I'm thinking Amazon maybe?

Recall the example on minimizing shipping costs from factories to warehouses. In a realistic application,
a company may have 10 factories and and, say, 100 warehouses located around the world. Moreover, each factory 
will manufacture not a single product but, say, 1000 different products. All these products need to be shipped 
from factories from warehouses. The linear program minimizing the shipping costs will have a variable $$x_{ijk}$$ that 
indicates the quantity of the product $$P_i$$ that should be shipped from the factory $$F_j$$ to the warehouse $$W_k$$. 
This gives  $$10 \times 100 \times 1000 = 1,000,000$$ variables. In this setting, we will also have many extra constrains. 
For example, it may happen that the total weekly production of products $$P_1$$ and $$P_2$$ in some factory is limited to 
500 items, so if we choose to manufacture e.g. 400 copies of $$P_1$$, then we can produce at most 100 copies of $$P_2$$. 
We will need to include all such dependencies in the linear program. Some version of this is probably used by Amazon, 
since Amazon sells millions of different products that need to be shipped from central hubs to regional and local distribution 
centers before they are sent to customers. 


#### Himanshu asks:

> 1. Isn't the minimum always going to be at the origin? Like in the case of the farming problem, if the farmer did not grow any crops, it 
>    would be the minimum. So are there cases where (0,0) is not the minimum?
>
> 2. While discussing the unboundedness case, are there cases where there is no maximum and minimum?


1. The minimum of the objective function need not be at the origin. One reason for this is that the origin may not 
   give a feasible solution. For example, in the farming problem if we add an additional constraint that the farmer needs 
   to grow at least 50 acres of crops, (i.e. $$x_1 + x_2 \geq 50$$), then this will not be satisfied 
   if $$x_1 = 0$$ and $$x_2 = 0$$. Even if the origin gives a feasible solution, it needs not give the minimum. Where the minimum is will depend on the objective function. 

2. This can happen. Take e.g. the objective function $$z = x_1 - x_2$$ and constraints $$x_1 \geq 0$$, $$x_2 \geq 0$$. Then $$z$$ 
   can be both arbitrarily large and arbitrarily small.


#### Xu asks:

> 1. When faced with a linear programming problem, how can one determine if there is a unique optimal 
>    solution, or if multiple solutions exist? 
> 2. Are there scenarios where no optimal solution is possible?

1. I will talk about the simplex method, which a way of solving linear programs. Using this method it is also 
   possible to check if a solution is unique or not. 

2. I talked about it in class: a linear program will not have a solution if it is not feasible. It also may have 
   no solutions if it is unbounded.


#### Laura asks:

> Is there a Gradescope code somewhere where I would be able to join the class on Gradescope? 
> The link just sends me to the Gradescope homepage.

Gradescope will be set up by the time the first homework is assigned.


#### Aurora asks:

> 1. Will we be looking at other modeling strategies or programs other than linear programming? 
> 2. What type of jobs would use linear programming? 
> 3. What type of example problem would linear programming be beneficial to use?

1. In this courses we will look at various applications of linear algebra. Some of them will be related 
to mathematical modelling. 

2. Logistics, operations research, data analysis, financial analysis, production planning, supply chain management etc. 

3. Several applications of linear programming will show up in this course, but the ones we have seen already
   are representative to how linear programming is used in practice.


#### Xin asks:

> I want to know what form of homework is, Do I get enrollment to Gradescope? 

Each homework assignment will consist of a few exercises related to the course content. 
Gradescope will be set up by the time the first homework is assigned.


#### Zhen asks:

> 1. If it's infinitely close to zero can I just set the minimum value to zero？
> 2. Is it possible that it doesn't have a maximum and a minimum?

1. The minimum of the objective function in a linear program 
   (if it exists) will be either 0 or some other number. I am not sure what you mean by infinitely 
   close to zero? 

2. Yes, I talked about it in class. A linear program may not have a minimum or maximum if it is 
   either unfeasible (i.e. it has not feasible solutions) or if its feasible region is unbounded.


#### Michael asks:

> What exactly is a slack variable? I am a little confused but I think if I see it being used in an actual 
> problem (opposed to general form) then I will understand what it means. Maybe I am overthinking it.

Slack variables are used to replace inequality constraints in a linear program by equivalent equality constraints. 
Saying that variables $$x_1, \dots, x_n$$  satisfy an inequality $$a_1x_1 + \dots + a_nx_n \leq b$$ is 
equivalent to saying that these variables  satisfy the equality  $$a_1x_1 + \dots + a_nx_n + s = b$$
for some $$s\geq 0$$. The new variable $$s$$ is called the slack variable, because it picks up the slack
between the left hand side and the right hand side of the inequality. 


#### Quinquan asks:

> Is there only one type of linear programming?

Yes, linear programming is what I described in class. There are various methods of solving linear programs though.
