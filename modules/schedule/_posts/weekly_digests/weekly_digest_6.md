### Weekly Digest 6: Questions and Answers

<br/>


#### Stephanie asks:

> 1. Do we use vertex covers when we model traffic flow?
>
> 2. And are there disadvantages to solving a relaxed linear program rather
> than the original?

1. I don't know of such applications, but it is possible that they exist.
2. Usually the solution of a relaxed linear program will give only an approximated
   solution of the integer program we are really interested in. In some cases this
   appoximation can be helpful, but in other cases it may be too far from the solution
   of the integer program to be of use.

#### Chase asks:

> What is the significance of network theory in relation to what we are going to do with
> linear algebra applications? Are we going to be utilizing the path count from a node to
> a node? I just want to know where we are going with this.

Our next goal will be to look at some applications of linear algebra to network theory
(connectivity of networks, partitioning of networks, random walks on networks etc.).
Path counting in a graph is a small application of adjacency matrices that will
came handy later on.