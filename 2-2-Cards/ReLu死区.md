---
creationDate: 2023-10-24 00:51
card_type: 机器学习
---
## 为什么会出现ReLu死区
ReLu函数图像如下：
![[Pasted image 20231024005314.png|350]]
当一个神经元接收到大于0的时候，这个神经元会输出一个正值，此时功能正常。
当一个神经元接收到小于0的时候，这个神经元的输出和导数都为0，导致其无法正常更新。为什么导数为0？
$$
\begin{aligned}
&对于LOSS = (y-y_{target})^{2} ,\\
&y = wx+b \\
& 对LOSS求导，得 \frac{\partial L}{\partial w} = \frac{\partial L}{\partial y} * \frac{\partial y}{\partial w} =2(wx+b)x \\
&由于神经元输出的一直为0，即y=0，所以，对于\frac{\partial y}{\partial w}，一直就为0，\\&就得到L对w的偏导数就为0，无法反向更新w，进行w迭代更新
\end{aligned}
$$






