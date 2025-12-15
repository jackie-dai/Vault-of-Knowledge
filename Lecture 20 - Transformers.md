
All LLMs (claude, gpt, gemini) have one thing in common. In the background they are run by transformers

## What is a Transformer?
The predominant underlying architecture in most LLMs. It can also be applied to CNNs

### Multi-layer Perceptron (MLP)
A transformer is made of MLPs

## The problem with convolutional networks
The issue is that CNNs scan in patches. But patches are independent from each other, there is no broader context beyond that patch.

**Receptive Field**: The width of what's visible to a single neuron.

![[Pasted image 20251214160141.png]]
A neuron can only see what it is told. The top neuron has knowledge of all the neurons below it (within the triangle).

Weakness: only the top layers of the network has all the context

## Solution: Transformer Architecture
Why is context important?

"I swan across the river to get to the other **bank**"

"I walked across the road to get cash from the other **bank**"

Bank could mean multiple definitions but we can only tell from context found in the rest of the sentence.

**Token embeddings**: The transformer model takes as input a set of N token embeddings vectors in $R^D$ representing the basic building of an image or text. For example, patches for images and words for sentences

Input: X~matrix of $R^{NxD}$, where there is a row for each N token and D columns for the the size of the feature vector for each token
Output: Y~matrix of $R^{NxD}$