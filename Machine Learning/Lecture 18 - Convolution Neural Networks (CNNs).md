
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
Output dimensions: (J-M+1)x(K-M+1)


image <- convolution <- pooling <- flatten <- feed into classifer/neural network

Convolution
	scanning with a kernal and dot producting with sections of the image

Pooling
	subsampling each feature map 
		examples are max pooling or average pooling

flatten image into ndarray to feed into the neural network


