### Weekly Digest 13: Questions and Answers


<br/>


#### Stephanie asks:

> Are random walks truly random if they converge or have a steady state vector?

It is not different than tossing a coin: if you toss it many times, then the fraction
of heads and tails obtained will be converging to 0.5. This does not make a coin toss
not random.


#### Nick F. asks:

> Is it possible to calculate where two items on a Markov chain will intersect?
> For example, if two different people are walking on the same path network,
> could we figure out the probability of them reaching the same point?

This can be modeled as a Markov chain with states given by pairs of vertices,
and transition probabilities describing chances that two people who are at
vertices $$i$$ and $$j$$ will move, respectively, to vertices $$k$$ and $$l$$.
The the probability of these people reaching the same point is the probability
that they will transition to a state where both vertices are the same.


#### Chase asks:

> Is there any way to tell if there exists a steady state vector for a stochastic
> matrix, without manually calculating the markov chain?

As I explained in class last week, every stochastic matrix has a steady state vector.
It is not true though that a Markov chain will always converge to it.


#### Yuzhang asks:

> I'm uncertain whether I fully comprehend the concept of a probability vector.
> Is it simply a type of random vector where the sum of its entries equals 1?

Yes, also all entries of a probability vector are non-negative, since they are meant
to represent some probabilities.


#### Alice asks:

> Are there any limitations to the use of steady-state vectors in analyzing Markov chains?

Steady state vectors deal only with long-term probabilities, which does not solve
all questions related to Markov chains.


#### Giacomo asks:

> How can you confirm if you have found all of the steady state vectors of
> a stochastic matrix that is not regular?

It is true that every stochastic matrix $$P$$ has a steady state vector. It is not
true though that this vector is unique, or that a Markov chain with the
transition matrix $$P$$ will converge to it. Both of these facts are true if the
transition matrix is regular.


#### Nick L. asks:

> What is the purpose of the stochastic matrix?

A stochastic matrix is simply a square matrix with non-negative entries and such that
the the sum of each column is equal to 1. These matrices appear in different contexts,
for example the transitiom matrix of any Markov chain is stochastic, so it is useful
to have a name for them.


#### Huixin asks:

> Do we obtain the fraction of the total variance captured by the first two principal
> components by dividing the sum of the largest two eigenvalues by the total variance of the data?

Yes, this is correct.


#### Alan asks:

> In regard to long term markov chains, will the steady state vector always exist
> or is it possible that there is no long term fixed probability?

Every stochastic matrix $$P$$ has a steady state vector. It is not
true though that this vector is unique, or that a Markov chain with the
transition matrix $$P$$ will converge to it. Both of these facts are true if the
transition matrix is regular.


#### Keith asks:

> If transition matrix $$P$$ has entries $$p_{ij}\geq 0$$, is there a way to determine whether
> $$P$$ is regular? For some matrices, we can tell at a glance that they are not regular:
> the transition matrix corresponding to the gambling model (p.135) is not regular because of
> its first column, for example. With respect to the Perron-Frobenius Theorem, we would like
> to know whether a transition matrix is regular.

There are some easy criteria that quarantee that a matrix is not regular.
To check that a matrix is regular for sure, we can compute a power of the matrix
and check if it has only non-zero entries. If $$P^n$$ satisfies
this condition, then so does $$P^{n+k}$$ for any $$k \geq 0$$, so any high enough
power will do. There are some resuts which say what is the lowest power
that will work, so in practice we only need to compute one specific power.


#### Pavan asks:

> 1. Google's PageRank basically says that pages are ranked according to higher probabilities.
> From a math perspective, is probability the only factor that determines the popularity of a page?
> 2. When you write $$P^n$$ converges for gambling or weather models, what does it mean for the model?

1. This is how it worked in the original Google PageRank model. I am sure that over time Google has been
   tweaking its webpage rankings to incorporate other factors.

2. It in the weather model it means that the predictions if a day will be raining or sunny $$n$$
   days from now do not depend substantially neither on $$n$$ nor on the weather today, if $$n$$
   is large enough. In the gambling model, it means that how much money the gambler will have after
   playing the game $$n$$ times for large $$n$$ does not depend on $$n$$, but it does depend on how
   much money he has when he starts playing.


#### Yingkun asks:

> Will we have another assignment? If so, will there be an office hour for us to discuss it?

I have not decided yet, I will let you know on Wednesday. If there will be an assignment,
I will schedule office hours next week.

#### Anthony asks:

> Is it possible to create a Markov chain model of two mutual events?

It depends on what you mean precisely.

