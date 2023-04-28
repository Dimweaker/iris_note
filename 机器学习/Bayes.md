# 贝叶斯定理(Bayesian theorem)

## 公式

$$
\underbrace{ f_{\tiny{{Y|X}}}(C_k|x) }_{Posterior}
= \frac{\overbrace{f_{\tiny{X,Y}}(x,C_k)}^{Joint}}{f_{\tiny{X}}(x)}
= \frac{\overbrace{f_{\tiny{X|Y}}(x|C_k)}^{Likelihood}\overbrace{p_{\tiny{Y}}(C_k)}^{Prior}}{\underbrace{ f_{\tiny{{X}}}(x)}_{Evidence}}
$$

其中，$f_{\tiny{{Y|X}}}(C_k|x)$为**后验概率**(posterior)，又叫**成员值**(membership score)，比较后验概率的大小，可进行分类。
$f_{\tiny{X,Y}}(x,C_k)$为**联合概率**(Joint)。
$f_{\tiny{X}}(x)$为**证据因子**(evidence)，仅代表$x$的分布情况。
$p_{\tiny{Y}}(C_k)$为**先验概率**(prior)，表示样本中$C_k$的占比。
$f_{\tiny{X|Y}}(x|C_k)$为**似然概率**(likelihood)，表示
$C_k$中出现$x$的可能性。

## 似然概率

似然概率$f_{\tiny{X|Y}}(x|C_k)$本身是条件概率,它描述的是给定类别$Y=C_k$中$X=x$出现的概率。
似然概率可用概率密度函数$PDF$描述，而概率密度函数可对标签为$C_k$的样本作高斯$KDE$估计得到。

## 先验概率

先验概率$p_{\tiny{Y}}(C_k)$描述的是样本集合中$C_k$的占比。

$$
p_{\tiny{Y}}(C_k) = \frac{count(C_k)}{count(\Omega)}
$$

## 联合概率

联合概率$f_{\tiny{X,Y}}(x,C_K)$描述事件$Y=C_k$和$X=x$同时发生的可能性。

## 证据因子

证据因子$f_{\tiny{X}}(x)$实际上是$X$的边缘概率密度函数$PDF$，与分类无关，可对所有样本作$KDE$估计得到。

## 后验概率

后验概率$f_{\tiny{{Y|X}}}(C_k|x)$指在事件$X=x$条件下，$Y=C_k$发生的概率，即已知$X=x$,$X$来自于$Y=C_k$的概率。后验概率也被叫作成员值。

$$
f_{\tiny{{Y|X}}}(C_k|x) = \frac{f_{\tiny{X,Y}}(x,C_k)}{f_{\tiny{X}}(x)}
$$
