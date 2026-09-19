# 求$|\overrightarrow{OP}|$最小值的五种解法

已知$\overrightarrow{OA},\overrightarrow{OB},\overrightarrow{OC}$两两垂直，$|\overrightarrow{OP}|^2 = m^2 + n^2 + l^2$，约束条件：$m + 2n + 3l = 3$。

## 方法1：柯西不等式法
根据柯西不等式：
$$
(m^2 + n^2 + l^2)(1^2 + 2^2 + 3^2) \geq (m\cdot1 + n\cdot2 + l\cdot3)^2
$$
代入条件：
$$
(m^2 + n^2 + l^2)\cdot14 \geq 3^2 = 9
$$
得
$$
m^2 + n^2 + l^2 \geq \frac{9}{14}
$$
$$
|\overrightarrow{OP}| \geq \sqrt{\frac{9}{14}} = \frac{3\sqrt{14}}{14}
$$

## 方法2：点到平面距离法
以$O$为原点建立空间直角坐标系，$P(m,n,l)$满足平面方程 $x + 2y + 3z = 3$。
$|\overrightarrow{OP}|$是原点到平面上点$P$的距离。
平面$Ax+By+Cz+D=0$原点距离公式：
$$
d = \frac{|D|}{\sqrt{A^2+B^2+C^2}}
$$
平面改写：$x+2y+3z-3=0$
$$
d = \frac{3}{\sqrt{1+4+9}} = \frac{3\sqrt{14}}{14}
$$

## 方法3：二次函数配方法
由约束得 $m = 3 - 2n - 3l$，代入：
$$
|\overrightarrow{OP}|^2 = (3-2n-3l)^2 + n^2 + l^2
$$
整理为关于$n$的二次函数：
$$
= 5n^2 + (12l-12)n + 9l^2-18l+9
$$
当 $n=\dfrac{6-6l}{5}$ 取最小值，代入得到关于$l$二次函数：
$$
|\overrightarrow{OP}|^2 = \frac{14}{5}l^2 - \frac{42}{5}l + \frac{9}{5}
$$
配方：
$$
= \frac{14}{5}\left(l-\frac{9}{14}\right)^2 + \frac{9}{14}
$$
最小值$\dfrac{9}{14}$
$$
|\overrightarrow{OP}|_{\text{min}}=\frac{3\sqrt{14}}{14}
$$

## 方法4：向量投影法
约束改写点积：
$$
\overrightarrow{OP} \cdot (\overrightarrow{OA}+2\overrightarrow{OB}+3\overrightarrow{OC}) = 3
$$
令$\boldsymbol{u}=\overrightarrow{OA}+2\overrightarrow{OB}+3\overrightarrow{OC}$
$$
|\boldsymbol{u}|=\sqrt{1^2+2^2+3^2}=\sqrt{14}
$$
点积定义：
$$
\overrightarrow{OP}\cdot\boldsymbol{u} = |\overrightarrow{OP}|\cdot|\boldsymbol{u}|\cdot\cos\theta = 3
$$
$\cos\theta\le 1$
$$
|\overrightarrow{OP}| = \frac{3}{\sqrt{14}\cdot\cos\theta} \geq \frac{3}{\sqrt{14}} = \frac{3\sqrt{14}}{14}
$$

## 方法5：拉格朗日乘数法
构造拉格朗日函数：
$$
L = m^2+n^2+l^2 + \lambda(m+2n+3l-3)
$$
求偏导等于0：
$$
\begin{cases}
\dfrac{\partial L}{\partial m}=2m+\lambda=0 \\[4pt]
\dfrac{\partial L}{\partial n}=2n+2\lambda=0 \\[4pt]
\dfrac{\partial L}{\partial l}=2l+3\lambda=0 \\[4pt]
\dfrac{\partial L}{\partial \lambda}=m+2n+3l-3=0
\end{cases}
$$
解得：$\displaystyle m=\frac{3}{14},\ n=\frac{3}{7},\ l=\frac{9}{14}$
$$
|\overrightarrow{OP}|^2=\frac{9}{14},\quad |\overrightarrow{OP}|_{\text{min}}=\frac{3\sqrt{14}}{14}
