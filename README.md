## Exact Calculation

### Return
The expected return of each asset will be calculated by

$$E\left[r_i\right]=\mu_i$$

where $\mu_i$ is the mean of the historical data. Thus, the total expected return for a portfolio is given by

$$\sum_{i=1}^n w_i\mu_i=\mathbf{w}^T\mathbf{\mu}.$$

where $\mathbf{\mu}=\left[\mu_1,\ldots,\mu_2\right]^T$ is the vector of the expected returns and $\mathbf{w}=\left[w_1,\ldots,w_2\right]^T$ is the vector of the weights of each stock in the portfolio.


### Risk

The risk is measured as the variance of the returns given by

$$\sigma_i^2=\textrm{Var}\left(r_i\right)=E\left[\left(r_i-\mu_i\right)^2\right]$$

and the covariance between two assets $i$ and $j$ is given by

$$\sigma_{ij}=\textrm{Cov}\left(r_i,r_j\right)=E\left[\left(r_i-\mu_i\right)\left(r_j-\mu_j\right)\right].$$

Using matrix notation, the covariances can be put into a covariance matrix, $K$, such that

$$K=\left[\sigma_{ij}\right].$$

The total variance of the portfolio is going to be

$$\sigma_P^2=E\left[\left(r_P-\mu_P\right)^2\right]=\sum_{i=1}^n\left(\sigma_iw_i\right)^2+2\sum_{i=1}^{n-1}\sum_{j=i+1}^nw_iw_j\sigma_{ij}=\mathbf{w}^TK\mathbf{w}$$

## Risk-Return Problem

If we want an expected return $r_0$, then the problem becomes,

$$
\textrm{minimize } \mathbf{w}^TK\mathbf{w}
$$
such that
$$
\mathbf{w}^T\mathbf{\mu}=r_0\\
w_i\ge0,\forall i\\
\mathbf{w}^T\mathbf{e}=1
$$

where $\mathbf{e}=\left[1,1,\ldots,\right]^T$ is a vector of all ones. The solution becomes

$$\mathbf{w}=K^{-1}\left[\begin{array}{cc}\mathbf{\mu}&\mathbf{e}\end{array}\right]A^{-1}\left[\begin{array}{c} r_0\\1\end{array}\right]$$

where $A$ is given by

$$A=\left[\begin{array}{cc}\mathbf{\mu}^TK^{-1}\mathbf{\mu}&\mathbf{\mu}^TK^{-1}\mathbf{e}\\
\mathbf{\mu}^TK^{-1}\mathbf{e}&\mathbf{e}^TK^{-1}\mathbf{e}\end{array}\right].$$
