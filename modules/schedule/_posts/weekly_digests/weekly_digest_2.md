### Weekly Digest 2: Questions and Answers

<br/>


#### Himanshu asks:

> 1. What happens when $$b_i < 0$$ ? We never went over those type cases. 
>
> 2. What's the advantage of using the simplex method to find the extreme points, like why can't 
>    we just subsititute like we did in the farmer example? 

1. The process deals with this is called phase I of the simplex method. We will get to it. 

2. I showed that the farmer's example can be solved by finding all extreme points, and then 
   checking which of them gives the biggest value of the objective function. This worked only 
   because this was a very small linear program, with 2 variables and 3 constaints. Linear programs
   used in practical applications have thousands of variables and constraints. The number of 
   extreme points for such programs is so large, that it would be impossible to compute them all using 
   even the most powerful computers. The advantage of the simplex method is that it usually requires 
   calculating relatively few critical points. Using this methods, large linear programs can be often 
   solved in a matter of seconds or minutes.



#### Samuel asks:

> The name simplex tableau makes me curious if we will be learning that python library in this course?

I am not sure which library you refer to, but there are several Python libraries that 
can be used to solve linear programming problems. I will explain how to use `scipy` for this. 


#### Xin asks:

> I want to know how much knowledge is related to Python this semester. Currently, in the first assignment, 
> I have not seen anything related to Python.

I will show how to use Python to solve linear programs this week. Later on, we will 
use Python from time to time for various computations.



#### Grace asks:

> In regards to the simplex method example we were working on in class - since we are trying 
> to maximize it, are we going through all the feasible solutions (by pivoting) and then 
> selecting the maximized one by the one with the highest $$z$$ value?

This is mostly correct, except that the main benefit of the simplex method is that it 
does not go though *all* basic feasible solutions. Instead, it goes through a sequence 
of *some* basic feasible solutions, at every step increasing the value of $$z$$. Most of the basic 
feasible solutions are never used, since the simplex method never goes to a basic feasible solution 
that would give a lower value of $$z$$ that the one that has been already found. This speeds up 
the computations a lot. Linear programs that would take years to solve using a computer 
by calculating all basic feasible solutions, can be usually solved in a matter of minutes or 
seconds using the simplex method. 



#### Aurora asks:

> 1. What are the limitations of the simplex method?
> 2. How is the implementation process for this method with coding?

1. There are some cases when the simplex method will travel through most critical points
   of the feasible region before reaching the solution. In such cases, computations
   may be very slow. 
2. To implement the simplex method from scratch, one would need to write code that 
   performs the pivot step, and then run this code in a loop as many times
   as needed to get the solution. There are many libraries that already do this, so 
   we can use them instead of writing our own implementation.



#### Zhen asks:

> During the learning process, I have reached some questions. 
> 1. How does the simplex method select pivot elements during iterations? 
> 2. Are there alternative methods for solving systems of linear equations, 
>    and when might they be preferred over the Gaussian elimination method?

1. Pivot elements (or rather free and basic variables used in each pivot step)
   are selected so that the objective function will increase. Various enhancements
   of the simplex method use additional pivoting rules, that are intended to make 
   computations more efficient.
2. LU factorization is usually used by computers to solve sytems of linear equations. 
   It is based on the Gaussian elimination, but it has computational advantages.


#### Jonathan asks:

> In some of the notes, it shows the basic variables are out of order like this: 
> $$[0\ 1\ 0\ 1\ 0\ 0\ 0\ 0\ 1 ]$$. I wanted to ask if this is still correct or we have 
> to move the rows around and if the basic variables need to be first or if doesn't matter 
> if the free variables or the basic variables go first for a row.

Basic variables do not need to come before free variables. We keep the ordering 
variables the same all the time, and we just keep track which variables are basic and which are 
free at each pivot step. 


#### Quinquan asks:

> When a matrix is in reduced row echelon form with no free variables, 
> does it mean there is only one basic feasible solution?

Yes. From the perspective of linear programming, this is an uninteresting 
situation, since this unique feasible solution will be both the minimum 
and the maximum of the objective function, since there are no other choices. 
