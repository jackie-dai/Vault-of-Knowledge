

## Numerical Differentiation
Advantage
- Can apply to any error function 
- Easy to implement
Disadvantage
- Expensive
- Approximate

## Automatic Differentiation


## Backward Propagation

### Adjoint variable

1(e^v_3) + 1(1)


## Optimizers

### Gradient Descent
![[Pasted image 20251109014222.png]]
Oscillates on the vertical axis, making it risky to use high learning rates $\alpha$

### Adaptative Gradient Descent (AdaGrad)
AdaGrad dynamically adapts the learning rate for each weight component. For large gradients, the learning rate will be small. While small gradients will have large learning rates.
![[Pasted image 20251109015016.png]]

Downside: the learning rate decays (because it is divided by a cumulative number) so the last few iterations converges slowly.


