
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

Why can't we just average all the context into a vector and add it to our input?
![[Pasted image 20251214163743.png]]
Not all context is equally important (i.e some words are not as important to understanding the context of bank)

![[Pasted image 20251214164934.png]]

### Softmaxing

![[Pasted image 20251214210458.png]]
```
For each token, you first apply a weight matrix (e.g., , , ) to transform it into query, key, and value vectors. These vectors are then used to compute attention scores via the softmax function applied to the inner product of queries and keys. The attention scores are used to weight the value vectors, producing the final representation for each token.
```
*A.I explanation for the diagram*

	
![[Pasted image 20251214210407.png]]code equivalent:
```
def scaled_dot_product_attention(Q: torch.Tensor, K: torch.Tensor, V: torch.Tensor):
	(B, N, d_k) = Q.shape
	(_, _, d_v) = V.shape
	
	K_T = K.transpose(-2, -1)
	dot_product = (Q @ K_T) / (d_k ** 0.5)
	
	attention = F.softmax(dot_product, dim=-1)
	return attention @ V
```

