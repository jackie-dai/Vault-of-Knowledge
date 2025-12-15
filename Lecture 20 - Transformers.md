
All LLMs (claude, gpt, gemini) have one thing in common. In the background they are run by transformers

## What is a Transformer?
The predominant underlying architecture in most LLMs. It can also be applied to CNNs

### Multi-layer Perceptron (MLP)
A transformer is made of MLPs

## The problem with convolutional networks
The issue is that CNNs scan in patches. But patches are independent from each other, there is no broader context beyond that patch.

**Receptive Field**: The width of what's visible to a single neuron.

![[Pasted image 20251214160141.png]]
Neuron's have a limited 