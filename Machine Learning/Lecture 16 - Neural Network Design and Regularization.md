
Q: Why don't we set all activation weights to zero?
A: All values will remain identical throughout the learning process

## Symmetry
We want to break symmetry in our weight activations 

With random weight initialization, we break weight symmetry.  Most commonly we sample from the uniform distribution 
$$
Uniform[-\epsilon, \epsilon]
$$Choosing the right $\epsilon$ is important because we don't want the activations to become too large or vanish across layers

*Keep variance across layers constant*

 