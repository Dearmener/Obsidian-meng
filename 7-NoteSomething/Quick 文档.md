[[Quick Latex用法]]
## 功能
### 4. 在`\sum \int \frac`后自动加上大括号
当输入`(sum\limits_{i=1}^n x+1)`后，在其后加上空格就会在左右两侧加上大括号
![[Pasted image 20230602145833.png]]
$$
\left(\sum\limits_{i=1}^{n} x+1\right)
$$
$$
\left( \frac{asdf}{b}\right)
$$
### 5. 自动在有上标或者下标的地方加上大括号
$$
e^{-\lambda}
e_{ -\lambda}
$$
$$
x+(x+\frac{1}{2})
$$
$$
\begin{align*}
ia\\
sdaf\\
fads\\
\frac{f}{a}\\
int\\ main /\frac{}{}man\\
jdak .n s
\end{align*}
$$
$$
\begin{pmatrix}a & b & c & d \\ e & f & g & h \\ i & j & k & l \\ m  & n & o & p\end{pmatrix}
$$
$$
\alpha \\
\mathbf{thishissoemitndkjakdut}
$$
$$
\begin{align*}
\alpha \\
\sqrt{asdf}\\
\cdot\\
\text{fasdf}\\
\infty\\
\binom{5}{22} \\
\times\\
fdas
\quad asdf fdas dsaf ds af\\
\quad fadsfasdfasdfasdfi \quad fasdf sdkjlfjsdathisda;fj Jk\\

\end{align*}
$$


## Text Generate
使用latex生成一个4* 4的矩阵


$$
\begin{pmatrix}
a & b & c & d \\
e & f & g & h \\
i & j & k & l \\
m & n & o & p
\end{pmatrix}
$$
使用latex生产一个4*16的矩阵jk

可以使用\begin{matrix}和\end{matrix}命令来创建矩阵，其中每个元素用&符号分隔，每行用\\符号分隔。例如，以下代码将创建一个4×16的矩阵：
$$
\begin{matrix}
a_{1,1} & a_{1,2} & \cdots & a_{1,16}\\
a_{2,1} & a_{2,2} & \cdots & a_{2,16}\\
\vdots  & \vdots  & \ddots & \vdots \\
a_{4,1} & a_{4,2} & \cdots & a_{4,16}
\end{matrix}
你可以根据需要更改矩阵的元素。
$$

$$

\begin{pmatrix} 1 & 2 & 2 & 3 & 123 \\ 123  & daf & fa & fda & fdsa\\ 123 & f_{x} fsda  & fa & fdsa & f & \\ 123dfa & fa & fdsaa & fdsf & fas \\ \end{pmatrix}
$$
