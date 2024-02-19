### Weekly Digest 3: Questions and Answers

<br/>

#### Xu asks:

> How can we systematically determine a good initial basic feasible solution 
> to improve the performance of the algorithm?

Computations of the initial basic feasible solution are done in so-called Phase 1 of
the simplex method. I have not talked about it yet, but I will explain it this week. 


#### Aurora asks:

> What are some of the pivoting rules that you mentioned in class for improving efficiency 
> with the simplex algorithm?

At every pivot step of the simplex method, we must select a free variable that we want 
to increase. Sometimes there will be only one free variable that increases the objective
function, and then there is only one choice. However, usually there are many 
possible free variables to choose from. Pivoting rules specify how to make this choice. 
For example, such a rule may say that we should always choose the variable with the 
largest positive coefficient in the objective function. A different rule may say that 
we should always choose a variable with the smallest index. There are other options 
too. It is an open question if it is possible to find pivoting rules that are better than 
all other possibilities, i.e. that give the solution of every linear program using 
the least number of computations. All known pivoting rules do not have this property: each 
of them works well in some cases, but is not optimal in some other cases. 


#### Himanshu asks:

> 1. When are some of the cases when $$n=1000$$ or more happen?
> 2. If we know that the problem is unbounded by looking at the implex tableau, 
>    is it necessary to go on and do the pivot step?

1. For one example, see my response to Samuel's question in 
   <a href="{{site.baseurl}}/modules/schedule/week_2/" target="_blank">Digest 1</a>. 
   For a different example, consider the situation described in Exercise 2 of
   <a href="{{site.baseurl}}/assets/homework/hw_1.pdf" target="_blank">Homework 1</a>. 
   In a realistic setting, there will be no machines that can cut rods in one specific way 
   only. Instead, a machine will be able to cut a rod into pieces of any length. However, 
   the factory will still want to cut as few rods as possible to fulfill its orders, so
   it can minimize the usage of the material. The procedure to plan production will be as 
   follows. Lets say that we need to produce $$n_i$$ pieces of length $$l_i$$ for $$i=1, 2, \dots, k$$.
   We can consider all possible pattens of cutting a rod into pieces of lengths $$l_i$$. 
   Then we can set a linear program that will tell us how many rods should be cut using each 
   cutting pattern in order to meet the demand, while minimizing the total number of rods cut. 
   In this settig, the number of possible cutting patterns can easily reach thousands, 
   which will give thousands of decision variables. 

2. As soon as we know that a problem is unbounded, there is no need to continue, 
   since it is known that the problem has no solution.


#### Jonathan asks:

> How do you know when you are dealing with unboundedness? 

I explained this in class last week. Please see the 
<a href="{{site.baseurl}}/assets/annotated_notes/mth461_annotated_notes_7.pdf" target="_blank">notes</a>
on unboundedness handling.


#### Samuel asks:

> Is the simplex method optimal for more complex systems?

The simplex method and its variants works well in many cases. In some other cases, 
the are other methods for solving linear programs (the ellipsoid mathod, the interior point 
method etc.) that may work better.


#### Grace asks:

> 1. With degeneracy problems, is the only difference in the process 
>    that a pivot step along the way may not increase the value of z? 
> 2. How much does it matter that we make $$x_1$$ and $$x_2$$ 
>    free versus say $$s_1$$ in the example we saw in class?

1. Yes, a degenerate pivot step in the simplex method is a pivot step that 
   does not increase the objective function. 
2. In the starting setup of that example, $$x_1$$ and $$x_2$$ are free - 
   this is not a choice that we make, but it follows from the way the simplex 
   tableau looks at the beginning. Then we perform a pivot step which makes 
   $$s_1$$ into a free variable (while making $$x_1$$ basic).


#### Zhen asks:

> Are there any variations or extensions of the simplex method, and how do they impact 
> the expectation? How does the computational complexity of the simplex method compare to 
> other optimization algorithms?

The simplex method has been evolving all the time since it was invented, with the goal 
of making it more efficient. Due to this, there are now many variants of this method. 
See, for example 
<a href="https://repository.rice.edu/server/api/core/bitstreams/141e92b5-3821-41d1-ad68-ece751e1f186/content" target="_blank">this paper</a>
for an account of these developments. The simplex method has exponential complexity relative 
to the number of variables and constraints. Some other methods (e.g. the interior point method
or the ellipsoid method) have polynomial complexity. In practical applications though, 
variants of the simplex method usually perform as well or better than these other methods.


#### Angelo asks:

> 1. In lecture note 7 why is it more efficient to increase $$x_1$$ instead of $$x_2$$ in the first pivot step? 
> 2. Also, in lecture note 6 what exactly makes a solution free or basic? Would a free variable be when the feasible 
>    solutions are 0 and a basic variable be when one or both are any number but 0? 

1. Increasing $$x_1$$ in the first pivot step of that example would give the solution in 2 pivot steps. 
   Increasing $$x_2$$ leads to computations that require 3 pivot steps. 
2. At every pivot step of the simplex method, we keep track which variables are free and which are basic. 
   Basic variables correspond to the columns of the simplex tableau that have one entry equal to 1 and 
   the remaining entries equal to 0. When we know which variables are free and which are basic, we can 
   compute a basic feasible solution by setting free variables to 0. Values of the basic variables are 
   determined by this choice. Thus the process is going in the opposite direction than you suggested: first 
   we identify which variables are free, and then we make these variables equal to 0 to get a basic feasilble
   solution. 


#### Quinquan asks:

> Can a problem exhibit both unboundedness and degeneracy simultaneously in linear programming?

Yes. It is possible that the simplex method will go through one or more degenerate steps before 
it shows that the problem is unbounded. 

