### Weekly Digest 11: Questions and Answers

<br/>

#### Sean asks:

> What fields are these topics most important in?

Data analysis, mathematical modeling, optimization, machine learning etc. 


#### Aurora asks:

> 1. What other techniques besides PCA are there for dimensionality reduction? 
> 2. Is it a common practice to use multiple dimensional reduction techniques to 
>    enhance the overall effectiveness? 

1. There are many of them. Manifold learning, locally linear embedding, autoencoder, 
   kernel PCA, Independent Component Analysis etc. See e.g. 
   <a href="https://arxiv.org/ftp/arxiv/papers/1403/1403.2877.pdf">this paper</a> for 
   more information. PCA is one of the most commonly used methods, and several 
   other methods were developed as enhancements of PCA. 
2. Do you mean if it often happens that several dimensionality reduction methods are 
   applied to the same data? This is not unusual, for example in experimenting which 
   technique will work the best for given data. Also, some methods combine a few 
   other methods.
   

#### Himanshu asks:

> 1.  Whats the advantage of finding the trace of a matrix?
> 2.  Could you give a practical example of how the first principle component helps us out?

1. It is not so much an advantage, but rather a fact that the trace of a matrix naturally 
   appears in various settings. For example, as I explained in class, the total variance of 
   a data matrix, which is a useful characteristic of the data, is given by the trace 
   of the covariance matrix. 
2. I gave one such example in class last week, with analyzing exam scores. I will show another 
   example this week. 


#### Xu asks:

> How do we determine the definiteness of a quadratic form, and what implications does it 
> have for the associated matrix? 

Classification of a quadratic form depends on eigenvalues of the symmetric matrix defining 
the form. If all eigenvalues are positive, the form is positive definite etc. This fact gives 
a relationship between properties of matrices and properties of their quadratic forms. 


#### Grace asks:

> How will we decide the number of principal components to retain?

The answer will depend on a particular situation - the data being analyzed 
and what one wants to do with the data. There are some rules that people sometime 
follow - e.g. that one should use enough components to capture at least 90% or 95% 
of the total variance. One can also plot eigenvalues of the covariance matrix 
and see if at some point they start decreasing less rapidly. Sometimes it is a matter 
of experimentation, using different numbers of principal components with some training 
data, and checking which number works best. 

#### Jonathan asks:

> What is a covariance matrix? 

The definiton is in the lecture notes 24, page 102.


#### Angelo asks:

> 1. In lecture note 24 with the mention of a trace value. Would the trace of any matrix 
>    be the sum of values from the first number going down in a diagonal motion or does 
>    that vary depending on the matrix? 
> 2. Also, when finding the $$m_X$$ value as shown in lecture note 23, are we always going to 
>    have to round down for the $$m_X$$ value or do we just follow the traditional number rounding rule? 


1. Trace of a matrix is always the sum of entries on the main diagonal of the matrix. 
   It is defined for square matrices only. 
2. In these notes $$m_X$$ denotes the mean of a data vector $$X$$. In practical computations
   one may need to round it to some number of decimal digits. If so, the usual way is to round 
   to the nearest digit. 


#### Xin asks:

> How to combine PCA with the graph and use in real life.

I am not very familiar with application of PCA to graphs, but apparently there are some. 
See, for example, <a href="https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=3a6018ba9f17dbbf8034af1bbcd13082bf21a6d4">this paper</a>


#### Zhen asks:

> 1. How does PCA determine the importance of each principal component in a dataset?
> 2. Can PCA be used effectively on datasets where the variables have different units 
>    of measurement, and if so, what preprocessing steps might be necessary before applying PCA?

1. Importance of PCA components depends on the amount of the total variance of the data that they 
   capture. This, in turn, is equal to the corresponding eigenvalue of the convariance matrix.
2. Before applying PCA, data should be preprocessed, so that all feature vectors have more or less 
   the same scale. 

#### Samuel asks:

> Is the value of the slope of the best fit line of covariance the actual value?

I am not sure if this is what you mean, but finding the first principal component 
of data is not the same as finding the best fit line in the linear regression sense. 


#### Qinquan asks:

> On page 107, notes 25, when $$||u_1|| = 1$$ and $$Var(Y) =u^T(1/N * A * A^T)u$$, why $$Var(Y)$$ is the 
> largest if $$u$$ is a unit eigenvector corresponding to the largest eigenvalue $$\lambda_1$$ of $$C_A$$?

This follows from the constrained optimization of quadratic forms that I talked about previously. 
See lecture notes 22, page 94. 