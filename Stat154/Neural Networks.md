
![[Pasted image 20261118082811.png]]

A simple neural network takes in a scalar input x and outputs a scalar output f(x)
$$
f(x)=\phi_0 + \Sigma_i \phi_1 a(\theta_{d0}+\theta_{d1}x) 
$$
$\phi_0$ + the sum of the weighted hidden units
$$
h_d=ReLU(\theta_{d_0} + \theta_{d1}x)
$$
ReLU(bias + weight0 * x)
$$
ReLU(x)=Max(0,x)
$$