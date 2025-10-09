
$$
Var[X+Y] + Var[X] + Var[Y] + 2E[D_X,D_y]
$$
$$
2E[D_X,D_y] = Cov[X,Y]
$$
Covariances are difficult to directly calculate.

Instead use covariance properties.

### Covariance Properties

covariances are symmetric
$$
Cov[X,Y] = Cov[Y, X]
$$

Covariance with a constant is zero
$$
Cov[X, c] = 0
$$

$$
Cov[aX + bY, W] = aCov[X, W] + bCov[Y, W]
$$
Constants don't vary
$$
Cov[X+c, Y] = Cov[X, Y]
$$

$$
Cov[X, X] = Var[X]
$$
$$
Cov[X, Y] = E[(X-u_x)(Y-u_y)] = E[XY-u_xY - Xu_y + u_xu_y] = E[XY] - u_xE[Y] - u_y E[X] + u_x u_y
$$
$$
Cov[X, Y] = E[XY] - u_x u_y
$$