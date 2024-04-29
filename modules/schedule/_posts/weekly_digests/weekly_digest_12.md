### Weekly Digest 12: Questions and Answers

<br/>

#### Zhen asks:

> 1. How would you explain the purpose of finding the orthogonal projection of a vector $$v$$ onto $$u$$ ?
> 2. Why might it be beneficial to use Principal Component Analysis (PCA) on a data set with many variables?

1. Orthogonal projects are used very often and has several applications. For example, while talking
   about PCA I used it to explain the geometric interpretation of principal axes. 
2. PCA is used to decrease the number of dimensions of data, while preserving as much information as possible. 
   Lower dimensional data is easier to compute with and easier to analyze. 


#### Himanshu asks:

> 1. How much time do we save using the PCA (like from our example of going from 784 to 250ish)?
> 2. Are there any courses (at UB or online) that you would recommend which teach MNIST? 

1. It is usually not about time, but about bringing data to a more convenient form and filtering out 
   noise. The first principal components (the ones with bigger variance) usually contain useful 
   information (e.g. related to the actual shape of handwritten digits). Further principal components 
   are considered as capturing mostly noise (e.g. some random shadings in the images of digits). 
   By forgetting these noisy components, we separate useful information from the noise. 
2. MNIST is just a dataset. There are no courses that teach MNIST, but several courses in machine 
   learning, data analysis or artificial intelligence most likely use MNIST to demonstrated various 
   methods and algorithms. Among math courses, you may see MNIST or some its variants in MTH 448. 


#### Xu asks:

> How can we determine the optimal number of principal components to retain in PCA, 
> especially in scenarios where we're dealing with high-dimensional data?  

The answer will depend on a particular situation - the data being analyzed 
and what one wants to do with the data. There are some rules that people sometimes 
follow - e.g. that one should use enough components to capture at least 90% or 95% 
of the total variance. One can also plot eigenvalues of the covariance matrix 
and see if at some point they start decreasing less rapidly. An often used method is 
cross-validation, which amounts to using different numbers of principal components 
with some training data, and checking which number works best. 


#### Jonathan asks:

> What are the main applications for PCA? What fields use it the most? 

PCA is most commonly used a dimensionality reduction technique. It is used 
in data analysis and machine learning. 


#### Aurora asks:

> If a dataset contains outliers, how does PCA account for it or how do 
> we account for it to still effectively use PCA?

PCA is sensitive to outliers, the same way as $$L_2$$ regression is. 
For this reason, data should be checked for outliers before PCA is applied. 
There are some methods for this. 


#### Sean asks:

> Do people ever make art out of these topics. For example people have made art 
> about the Collatz Conjecture so I’m wondering if there is any graph related art? 

I have not seen art made with PCA, but PCA is often used to analyze satellite photos, 
and the resulting images look quite artistic, see 
<a href="https://www.researchgate.net/figure/Sentinel-2A-PCA-Composite-bands-8-4-2_fig3_326925661">
this one</a>, for example.  


#### Samuel asks:

> Is demeaning data necessary or is it more for the presentation of the results?

It is necessary, without it PCA will give wrong results.


#### Xin asks:

> I have question about Python code, If I used python from your post, how can I use it in my HW?

I am afraid I don't understand the issue. Please ask me in person (in class, after class, 
at office hours) and I will try to help. 


#### Angelo asks:

> 1. In lecture note 27 I saw the proj being used and wondered if I could get more insight about it. 
>    I have seen proj in previous courses before but I would still like more clarification about what 
>    proj means and what it does and how we compute it. 
> 2. Another question I have is about the difference matrix. When computing the difference matrix do 
>    the matrices have to have the same dimensions or can we take the difference matrix from matrices 
>    of different dimensions just like how we can multiply a 2x3 and a 3x2 matrix? 

1. Orthogonal projection of a vector $$v$$ onto a vector $$u$$ decomposes $$v$$ into a vector that 
   is a scalar multiple of $$u$$ and a vector which is orthogonal to $$u$$. A different way of looking 
   at this is that the orthogonal projection produces a vector which is a scalar multiple of $$u$$, 
   but at the same time is as close to $$v$$ as possible.  

2. Addition and subtraction of matrices are defined only for matrices of the same dimensions. 


#### Grace asks:

> Why do we always have to use demeaned data for PCA?

One way to look at it is that PCA provides a new coordinate system for a given set of data. 
The origin of this coordinate system is the center (i.e. the mean) of the data. Demeaning 
shift the data, so that this new origin of the coordinate systems agrees with the usual origin.