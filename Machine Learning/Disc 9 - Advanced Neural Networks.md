
## How to 
### How do we improve convergence?
Use better optimization schemes (beyond vanilla gradient descent)
- Lecture 13: Momentum, Learning rate schedules, Adaptive learning rates (AdaGrad, RMSProp), Adam (RMSProp + Momentum)
Apply normalization to achieve a better operating region
- Lecture 16: Data, Batch, and Layer normalization
Use techniques to avoid the vanishing gradients problem
- Lecture 14: ReLU, Soft ReLU, or Leaky ReLU activation functions
- Lecture 17: Residual (skip connections)
-

### How do we reduce overfitting?
Use fewer trainable parameters
- Disc 8
Add L2 regularization to the error/loss function
- Lecture 17: Apply weight decay in the gradient update
Employ ensembles of models
- Lecture 17: combine the predictions of indepedent models
- Lecture 17: Use dropout to emulate ensembles with one network by randomly "disabling" neurons during each iteration of SGD

## Convolution

Multilayer Perceptron (MLP)
- fully connected
![[Pasted image 20251104173747.png]]
