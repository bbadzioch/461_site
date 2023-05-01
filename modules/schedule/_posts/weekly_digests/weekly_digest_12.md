### Weekly Digest 12: Questions and Answers


<br/>


#### Stephanie asks:

> How do we answer question 2 of the simple weather model? Would it just be the $$P$$ matrix.

I will talk about it. It is not the transition matrix.


#### Yuzhang asks:

> I'm curious if there's a Python library available for Markov chain applications.

Computations on Markov chains, at least to the extent covered in this course,
involve just linear algebra - matrix multiplication, matrix inverse, eigenvectors
etc. For this reason the Python libraries we have been using until now (primarily `numpy`)
will suffice.


#### Chase asks:

> What specifically is a Markov Chain? Is it any linear matrix that represents state transitions,
> where future state transitions can be found by putting the matrix to a power? Or is a Markov
> Chain just a matrix that represents states?


Formally, a Markov chain is a sequence of random variables satisfying certain properties that
describe how these variables are related to one another. For us in this course, a Markov chain
is a structure that consists of some number of states, of state vectors $$X_n$$ that describe
the probability that the sytem will be in a given state after $$n$$ step, and of a transition
matrix $$P$$ that gives probabilities that the system will transition from one state to another
in one step. Since $$X_n = P^n X_0$$, to specify a Markov chain it is enough to know $$P$$ and
$$X_0$$.


#### Giacomo asks:

> Could you provide a short definition of what a Markov chain is along with its uses?

See my response to Chase's questions directly above regarding the definition of a Markov chain.
I will show some applications of Markov chains in class.



#### Huixin asks:

> It seems that the possible future states are fixed if we use the Markov Chain to predict the future
> event. But I think the probability of the weather on someday may be affected by many factors. If we use
> Markov Chains to predict the future weather, and the weather changes suddenly one day, (1) should we
> still use the original transition matrix to compute with the state vector of that day? (2) How to predict
> the other weather conditions if they are not the relationship like rainy and sunny? For example, one
> day can be sunny and snowy at the same time. And the probabilities of windy, rainy, sandstorms and
> typhoons etc. may not be summed up to 1. Should these cases be computed separately or put into the
> same transition matrix?

1. The Markov chain weather model is just a simple example of a Markov chain. Weather models used
for forecasting are much more complex and they do inforporate a lot of factors.

2. It would be possible to modify the Markov chain used in class to predict other weather events too.
   At the same time though, not everything can be modelled as a Markov chain. There are many other tools
   useds in mathematical modelling.


#### Alan asks:

> 1. One of the assumptions of the power method is that $$|\lambda_1| > |\lambda_2| > {\dots} > |\lambda_n|$$.
> Does this method fall through if there are "duplicate" eigenvalues?
> 2. Also under HW6 it says that the due date is Wednesday 4/26, 11:59 PM. This was when HW5
> was due so I'm guessing that is a mistake?

1. If some eigenvalue repeats then there is more than one linearly independent eigenvector
   corresponding to this eigenvalue. The power method will still compute an eigenvector
   and its associated eigenvalue, but in general the eigenvector will depend on the choice
   of the vector used to start the power method. That is, different choices of the initial
   vector will result in different eigenvectors (all of them corresponding to the same eigenvalue).
2. This was typo (now fixed).



#### Nick L. asks:

> Will the power method not work if either assumption is not true?

It may still work, but with some complications - see the answer to Alan's question directly above.



#### Carter asks:

> 1. Since each invertible matrix has an inverse, would a vector say, v = (1, 0) or really any valid
> probability vector, give the probability of the previous state?
> 2. Can all discrete probability problems be converted to a Markov chain?
> 3. Are there applications for this in computer systems such as computer networks, guessing
> how a network could fail, etc...

1. This does not quite work this way. In particular, transition matrices of Markov chains need
   not be invertible.
2. No. Markov chains are stochastic processes of satisfying certain conditions. These conditions
   are not satisfied in all cases.
3. Yes. For example, Google PageRank algorithm is based on a Markov chain. I will talk about it.


#### Keith asks:

> Is there a relationship between the *transition matrix* and *stochastic matrix* defined in the notes?
> Are they the same thing? Also, the same question for the *state vector* and *probability vector*.
> In the simple rain/sun example of p.124, we seem to have used a stochastic matrix and probability vector,
> but this was also our example for the (n-step) transition matrix and state vector.

The transition matrix of a Markov chain is always a stochastic matrix, but stochastic matrices show up
in contexts not related to Markov chains too. The relationship between state vectors in a Markov chain
and probability vectors is analogous: every state vector is a probability vector, but probability vectors
are used not only for Markov chains.


#### Nick F. asks:

> Can we have independent sets of vertices in a Markov chain?

I am not sure what you mean. Markov chains have states, not vertices, and
it is not clear what it would mean for states of a Markov chain to be independent.


#### Pavan asks:

> Is it possible to use Markov chains in predicting behavior of complex systems?
> For example, to predict behavior in agent-based models?

Yes. In fact, many agent-based models can be seen as Markov chains. See for example
[this paper](http://www.umass.edu/preferen/gintis/acm-tist-markov.pdf).



#### Yingkun asks:

> I found that this week's homework deadline is on the 26th on the webpage.
> Is this the correct deadline for the assignment?

It as a typo, I fixed it.



#### Anthony asks:

> Will the power method fail if there are complex eigenvalues?
> Is there another method of calculating eigenvalues if they were complex?

Under the assumption we used (the matrix consists of real numbers and
absolute values of all eigenvalues are different), the matrix will not
have complex eigenvalues. The power method does not work for computing
complex eigenvalues, but there are other methods that do.


