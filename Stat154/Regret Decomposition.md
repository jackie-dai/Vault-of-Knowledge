
## Three types of fitted models
$f^*$ the best overall predictor
$\bar{f}$ the best line for the whole population
$\hat{f}$ the fitted line from the sample

## True Risk
$R(f)$ is the error from the true population

Approximation error: the error from restricting the shape (for example just straight lines)
Estimation Error: error from the fitted line (cost of fitting on limited data)

Regret = Approximation Error + Estimation 



### Ridge Regression 

$y=\Sigma(y_i - \hat{y}_i)^2 + \lambda \Sigma\beta_i^2$ 

$\lambda$ shrinks the coefficients to zero

Expected prediction error = noise + variance + $bias^2$
	