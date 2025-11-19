
## Scanning Network
We are going to scan through the network in patches (receptive fields) and applying a kernel to the patch to convolute it.


## Kernels/Feature Extractors

![[Pasted image 20251118222642.png]]
*Examples of horizontal and vertical line detector kernels

Results:
![[Pasted image 20251118223104.png]]



image <- convolution <- pooling <- flatten <- feed into classifer/neural network

Convolution
	scanning with a kernal and dot producting with sections of the image

Pooling
	subsampling each feature map 
		examples are max pooling or average pooling

flatten image into ndarray to feed into the neural network


