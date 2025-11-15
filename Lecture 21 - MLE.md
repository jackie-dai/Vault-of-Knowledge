
## Steps for Finding the MLE

Let’s capture our sequence of steps in an algorithm to find the MLE of a parameter given an i.i.d. sample. See the **Computational Notes** at the end of this section for other ways of finding the MLE.

- Write the likelihood of the sample. The goal is to find the value of the parameter that maximizes this likelihood.
- To make the maximization easier, take the log of the likelihood function.
- To maximize the log likelihood with respect to the parameter, take its derivative with respect to the parameter.
- Set the derivative equal to 0 and solve; the solution is the MLE.