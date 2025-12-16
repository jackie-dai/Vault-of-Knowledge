## LLM Architecture
Goal: predict the next word (token) in a sentence (ordered tokens).

![[Pasted image 20251215125927.png]]

### Constructing input embeddings 
Each token is mapped to a token id in a dictionary. 
![[Pasted image 20251215124841.png]]
The token ID serves as the index to the row the token is located on in the learned embedding table (matrix)
![[Pasted image 20251215124932.png]]
Add positional encoding
![[Pasted image 20251215130019.png]]
Ex: sinusoidal positional encoding

Now, pass your token embeddings into the transformer architecture. The output is a 1xD vector.
We multiply it by the learned embedding table. Finally softmax to produce probability of the token being the next token
![[Pasted image 20251215130241.png]]
