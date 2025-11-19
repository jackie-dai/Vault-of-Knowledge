
## Scanning Network
We are going to scan through the network in patches (receptive fields) and applying a kernel to the patch to convolute it.


## Kernels/Feature Extractors

![[Pasted image 20251118222642.png]]
*Examples of horizontal and vertical line detector kernels

Results:
![[Pasted image 20251118223104.png]]

Each kernel can only extract one feature, so we need to use multiple kernels to extract multiple features.

*Note: kernels will always be square M x M*

![[Pasted image 20251118224626.png]]
Input image: $J * K * C$
Kernel: M x M x C
Output (feature map) dimensions: (J-M+1)x(K-M+1)

**With stride and padding**
$$
(\frac{J+2P-M}{S} + 1) * (\frac{J+2P-M}{S} + 1)
$$

## Pooling
To detect features at different scale, we can down sample features by pooling

2x2 pooling would divide the feature into 2x2 areas. We would then apply a function to pick one pixel from the 2x2 area to keep (for example max function)

## CNN Design
image <- convolution <- pooling <- flatten <- feed into classifer/neural network

![[Pasted image 20251118233615.png]]

Convolution
	scanning with a kernal and dot producting with sections of the image

Pooling
	subsampling each feature map 
		examples are max pooling or average pooling

flatten image into ndarray to feed into the neural network

**Parameter Size**
(Kernel size *  kernel size + bias (1)) * num of kernels
3 * 3 + 1 = 10 * 8 = 80

## Pytorch

### Defining a convolution layer
![[Pasted image 20251118233710.png]]

Initializing a convolution layer
```
def __init__(self, num_classes=10):
	super().__init__()
	
	self.conv1 = nn.Conv2d(3, 8, kernel_size=3, padding=1)
```


