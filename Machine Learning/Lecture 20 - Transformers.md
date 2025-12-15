
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

Token positioning matters for text and images, but not sets of objects
![[Pasted image 20251214220615.png]]

## Methods for positional encoding

### Learned positional encoding
Rather than just passing tokens into the network. First, we can add a vector I_n that is randomly initialized and trained on the absolute position of the token.

$$
X_n =x_n+I_n
$$
*Essentially we are passing in the token + semantic information on the positioning*

The weakness: The max N positions needs to be known in advance.

### Rotary Positional Embeddings (RoPE)
Today most models use some variation of RoPE which applies a rotation matrix to the key and query vectors by a fixed amount based on that position.

By rotating a vector by $\theta_n$, we can tell the relative position of one token to another (if one token comes before the other token) because $\theta_n$ changes with n, n being the position of the token


## Transformer Architecture 
![[Pasted image 20251215103856.png]]

## The Encoder Transformer
Builds representation of input (ex: like context embedded tokens)
![[Pasted image 20251215103753.png]]
- Construct input embeddings
	- Ex: Pixel patches for images, tokens for text
- Apply positional encoding
	- Learned Positional Encoding, Sinusoidal encoding, RoPE
- Repeated transformer blocks
- Use final output in downstream task
	- Ex: pooling
	
*Encoder transforms are primarily used in computer vision models rather than language models.


## Generative AI
Knowledge is being able to predict the next word (token) in a sentence

**Basic Auto Regressive Decoding**
![[Pasted image 20251215105824.png]]
Compute the token given theordered tokens so far

### Byte Pair Encoding 
Initialize tokens to be the entire alphabet. Then, identify the pairs of tokens that occur most frequently together (scan the internet). This creates words as tokens but for less used words we just tokenize it letter by letter. 

### Casual Masking
**During training**, we make predictions on the token but in the attention layer we have access to all tokens in the input sequence in order to understand the context and assign appropriate attention to each token.

The issue: the model can cheat by looking at future tokens while trying to predict the next token.

The solution: Masked Attention
Limit the tokens that it can see to only the tokens before the current and nothing beyond. 

Now the model cannot cheat by looking at future tokens but it still has the context of everything before the current token it is on.
