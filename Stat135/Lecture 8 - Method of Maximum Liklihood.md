
MLE is useful because it can be applied to a number of problems and has nice theoretical properties

Algorithm *if the join density is i.i.d*
1.  find liklihood function
	1. $lik(\theta)= \Pi_f(X_i|\theta)$
2. Log liklihood
	1. $l(\theta)=\Sigma log[f(X_i|\theta)]$
3. Find partial derivatives with respect to the parameters
4. Set each partial derivative equal to zero and solve for the parameter to find the MLE