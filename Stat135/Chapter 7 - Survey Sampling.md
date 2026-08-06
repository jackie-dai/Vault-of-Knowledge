There are many cases where we won't have the full dataset. This is where sampling comes from because we can estimate the population mean from the sample mean. Of course, there will be 

Population Mean
$$
=\frac{1}{N} \Sigma x_i
$$

Population Total
$$
=Nu
$$
Population Variance
$$
\frac{1}{N} \Sigma(x_i - u)^2
$$

$X_i$ - is a sample of a member of the sampled population (random variable)
$x_i$ - is a member of the population (fixed)

A simulation is used for acquiring the sampling distribution
It is done by taking n sample means of

samples of size n
n samples
taking the sample mean of each sample and plotting it in histogram

![[Pasted image 20260804132741.png]]
*As the sample size increases, the distribution becomes more narrow towards the mean*

Estimating standard error by using finite population correction
![[Pasted image 20260805222025.png]]

### Estimation of the population variance

unbiased estimate 
$$
S^2=\frac{s^2}{n}(1-\frac{n}{N})
$$
s-sample standard deviation
n-sample size
N-population total



TODO: write out how to estimate standard error of sample mean and applying to standard error of population total
![[Pasted image 20260806104905.png]]


Variance and standard error estimation for the dichotomous case / proportion
![[Pasted image 20260806105133.png]]

Calculating the standard deviation of the sample mean with the finite population correction 
![[Pasted image 20260806133752.png]]