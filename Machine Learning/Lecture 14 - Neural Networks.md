
## Linear Models

### Higher Dimensions
Each feature adds a extra dimension 
	2 features -> 2D

TODO: proof that data points are sparse (in textbook)

Pros: better at linearly separating
Cons: difficult to manage so much data (10 features -> 10^10 bins)

## Neural Network

### Biological Neuron

![[Pasted image 20251023145042.png]]
Dendrites: collects signals from other neurons
Soma (cell body): sums signals from dendrites and processes
Axon: transmits signals to other cells

Synapses
- excitatory 
- inhibitory

### Artificial Neuron

Summation unit + activation function

### Activation Function
Example: Step function
$$
f(x) = 
\begin{cases}
1 & x > 0 \\
	0 & x < 0 
\end{cases}
$$


If the value is positive -> activate neuron
otherwise if the value is negative -> don't do anything



## Neurons
Building and gate with a neuron


In order to build the XOR gate, we need more than one neuron
![[Pasted image 20251105155932.png]]

## Neural Network

![[Pasted image 20251105160550.png]]Each $Z_i$ is a neuron (can also be multiple connected neurons like in the XOR example). Each neuron takes in every input. The subscript (1) in $Z_1^2$
