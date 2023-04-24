# 贝叶斯定理(Bayesian theorem)

## 公式

$$
\underbrace{ f_{\tiny{{Y|X}}}(C_k|x) }_{Posterior}
= \frac{\overbrace{f_{\tiny{X,Y}}(x,C_K)}^{Joint}}{f_{\tiny{X}}(x)}
= \frac{\overbrace{f_{\tiny{X|Y}}(x|C_K)}^{Likelihood}\overbrace{p_{\tiny{Y}}(C_K)}^{Prior}}{\underbrace{ f_{\tiny{{X}}}(x)}_{Evidence}}
$$

其中，$f_{\tiny{{Y|X}}}(C_k|x)$为**后验概率**(posterior)，又叫**成员值**(membership score)，比较后验概率的大小，可进行分类。
$f_{\tiny{X,Y}}(x,C_K)$为**联合概率**(Joint)。
$f_{\tiny{X}}(x)$为**证据因子**(evidence)，仅代表$x$的分布情况。
$p_{\tiny{Y}}(C_K)$为**先验概率**(prior)，表示样本中$C_k$的占比。
$f_{\tiny{X|Y}}(x|C_K)$为**似然概率**(likelihood)，表示$C_k$中出现$x$的可能性。

