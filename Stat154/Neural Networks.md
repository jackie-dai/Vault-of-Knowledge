
![[Pasted image 20261118085016.png]]

A simple neural network takes in a scalar input x and outputs a scalar output f(x)
$$
f(x)=\phi_0 + \Sigma_i \phi_d h_d 
$$
$\phi_0$ + the sum of the weighted hidden units
$$
h_d=a(\theta_{d_0} + \theta_{d1}x) \space \space a=ReLU(x)
$$
$$
ReLU(x)=Max(0,x)
$$


## Training Loop