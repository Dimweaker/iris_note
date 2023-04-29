## 高斯朴素贝叶斯

高斯朴素贝叶斯分类和朴素贝叶斯分类的流程和原理基本相同。只是朴素贝叶斯中，我们用高斯$KDE$估计来估算似然概率，而这里我们使用高斯分布。

## 似然概率

如果假设特征之间条件独立：

$$
f_{\tiny{X|Y}}(x|C_k)=\prod_{j=1}^Df_{\tiny{X_j|Y}}(x_j|C_k)
$$

假设条件边际服从高斯分布：

$$
f_{\tiny{X_j|Y}}(x_j|C_k)=\frac{\exp(-\frac{1}{2}(\frac{x_j-\mu_{j|C_k}}{\sigma_{j|C_k}})^2)}{\sqrt{2\pi}\sigma_{j|C_k}}
$$

结合可得，

$$
f_{\tiny{X|Y}}(x|C_k)=\frac{\exp(-\frac{1}{2}\sum_{j=1}^D(\frac{x_j-\mu_{j|C_k}}{\sigma_{j|C_k}})^2)}{(2\pi)^{\frac{D}{2}}\prod_{j=1}^D\sigma_{j|C_k}}
= \frac{\exp\left(-\frac{1}{2}(x-\mu_k)^T\Sigma_k^{-1}(x-\mu_k)\right)}{\sqrt{(2\pi)^D|\Sigma_k|}}
$$

## 联合概率

结合上面的式子，联合概率就可以表示为：

$$
f_{\tiny{X,Y}}(x,C_k)=p_{\tiny{Y}}(C_k)f_{\tiny{X|Y}}(x|C_k)=p_{\tiny{Y}}(C_k)\frac{\exp\left(-\frac{1}{2}(x-\mu_k)^T\Sigma_k^{-1}(x-\mu_k)\right)}{\sqrt{(2\pi)^D|\Sigma_k|}}
$$

## 分类

最大化联合概率：

$$
\widehat{y} = \argmax_{C_k}p_{\tiny{Y}}(C_k)\frac{\exp(-\frac{1}{2}\sum_{j=1}^D(\frac{x_j-\mu_{j|C_k}}{\sigma_{j|C_k}})^2)}{(2\pi)^{\frac{D}{2}}\prod_{j=1}^D\sigma_{j|C_k}}
$$

