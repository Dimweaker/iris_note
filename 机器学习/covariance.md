# 协方差(covariance)

## 定义

协方差 (covariance) 描述的是随机变量联合变化程度。
联合变化，简单来说，描述的是一个变量随另一个变量的变化。

$$
cov(X_1,X_2)=\frac{1}{n-1}\sum_{i=1}^{n}(x_1^{(i)}-\mu_1)(x_2^{(i)}-\mu_2)
$$

其中，$\mu_k$为均值

## 协方差矩阵

### 定义

$$
\mathit{\Sigma} = \begin{bmatrix}
\sigma_1^2 & cov(X_1,X_2) & \cdots & cov(X_1,X_n) \\
cov(X_2,X_1) & \sigma_2^2 & \cdots & cov(X_2,X_n) \\
\vdots & \vdots & \ddots & \vdots \\
cov(X_n,X_1) & cov(X_n,X_2) & \cdots & \sigma_n^2
\end{bmatrix}
$$

即$\mathit{\Sigma}_{i,j} = cov(X_i,X_j)$
注意到$cov(X_i,X_i)=var(X_i)=\sigma_i^2$
其中$var$为方差，$\sigma$为标准差

## 线性相关性系数(linear correlation coefficient)

### 定义

线性相关系数，也叫**皮尔逊相关系数(Pearson correlation coefficient)**，它刻画了随机变量间线性关系的强度，具体定义为：

$$
\rho_{1,2} = corr(X_1,X_2) = \frac{cov(X_1,X_2)}{\sigma_1\sigma_2}
$$

显然，$\rho \in [-1,1]$

值得注意的是，$\rho$相当于协方差归一化，也相当于对两个随机变量的$z$分数（z-score）求协方差

$$
\rho_{1,2} = corr(X_1,X_2) = cov(\frac{X_1-\mu_1}{\sigma_1},\frac{X_2-\mu_2}{\sigma_2})=cov(z_1,z_2)
$$

显然，$corr(X_i,X_i)=1$,
并且，$corr(X_i,X_j)=corr(X_j,X_i)$

### 相关系数矩阵

$$
P = \begin{bmatrix}
1 & \rho_{1,2} & \cdots & \rho_{1,n} \\
\rho_{2,1} & 1 & \cdots & \rho_{2,n} \\
\vdots & \vdots & \ddots & \vdots \\
\rho_{n,1} & \rho_{n,2} & \cdots & 1
\end{bmatrix}
$$
