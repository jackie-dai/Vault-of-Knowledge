
## How do we represent data?
images - patches
text - word parts

## Capturing context
![[Pasted image 20251119174728.png]]

### Token embeddings
- pieces of text or patch of a image in vector form
$x_n \epsilon R^D$

### Token Keys - vector representation of the descriptor of a token
$$
k_n = (W^k)^T X_n
$$
*The learned weight matrix * the token embedding*

### Token Queries - vector representation of a token that acts as a search query/question
$$
q_n = (W^q)^T X_n
$$
*The learned weight matrix * the token embedding*

Our goal is to find similarities between token queries and token keys. This is important so that we can relate words to other words. For example in a sentence, relating "it" to the noun they are referring to.



