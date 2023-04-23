# 最近质心分类（Nearest Centroid Classifier,NCC）

## 原理

不采用投票，而计算不同类别样本簇的质心$\mu_m$;查询点$q$离哪个分类质心最近就被划定为这一类。
其中，数据质心定义为：

$$
\mu_k = \frac{1}{count(C_k)}\sum_{i \in C_k}x^{(i)T}
$$



