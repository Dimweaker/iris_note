# 朴素贝叶斯分类(Naive Bayes classification)

## 分类原理

朴素贝叶斯分类的核心思想就是比较后验概率$f_{\tiny{{Y|X}}}(C_k|x)$的大小。

## 贝叶斯定理

参见[贝叶斯定理](Bayes.md)

## 成员值

由于$\sum_{k=1}^nf_{\tiny{{Y|X}}}(C_k|x)=1,f_{\tiny{{Y|X}}}(C_k|x)\in[0,1]$，后验概率也被称作**成员值**(membership score)。

## 联合概率

当证据因子$f_{\tiny{X}}(x)$不为$0$时，有

$$
f_{\tiny{{Y|X}}}(C_k|x)=\frac{f_{\tiny{X,Y}}(x,C_k)}{f_{\tiny{X}}(x)}
$$

可以看到，由于对于某个确定的$X=x$，证据因子是确定的。也就是说，后验概率与联合概率成正比。，所以如果要确定$X=x$的分类，只需要比较联合概率的大小。

## “朴素”之处

朴素贝叶斯分类的“朴素”之处在于——假设特征之间**条件独立**(conditional independence)

### 特征独立

特征独立，简单来说，就是因变量$x$中的各个因子相互独立，即：

$$
f_{\tiny{X}}(x)=\prod_{j=1}^Df_{\tiny{X_j}}(x_j)
$$

### 特征条件独立

特征条件独立，是在各条件下，因变量$x$中的各个因子相互独立。

$$
f_{\tiny{X|Y}}(x|C_k)=\prod_{j=1}^Df_{\tiny{X_j|Y}}(x_j|C_k)
$$

### 朴素贝叶斯优化

$$
\widehat{y} = \argmax_{C_k}p_{\tiny{Y}}(C_k)\prod_{j=1}^Df_{\tiny{X_j|Y}}(x_j|C_k)
$$



