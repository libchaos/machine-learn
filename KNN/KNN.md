## KNN 算法描述

### 输入： 训练数据集
$$T=\{(x_1,y_1),(x_2,y_2),...,(x_N,y_N)\}$$
其中

$x_i \in \mathbf X \subseteq \mathbf R^n$ 是 n 维实例特征向量

$y_i \in \mathbf Y =\{c_1,c_2,...,c_K\}$是实例的类别，$i=1,2,...,N$

### 输出： 预测实例$x$所属类别$y$

### 算法执行流程：

- 根据给定距离度量方法(一般情况下使用欧氏距离)， 从训练集中寻找出于x最近的k个样本点， 记为$N_k(x)$
- 根据多数投票原则，确定实例x所属的类别y

$$y = argmax 	\Sigma_{x \in N_k(x)} I(y_i, c_j), i=1,2,...,N; j = 1, 2, 3..., k$$

其中$I$为指示函数


$$
I(x, y)=
\begin{cases}
1, &\text{if x = y} \\
0, &\text{if x \neq y}
\end{cases}
$$








