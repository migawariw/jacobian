3変数 $(x, y, z)$ における極座標系では、ヤコビアンの式は以下のように与えられます。

$$
J = \begin{vmatrix}
\frac{\partial x}{\partial r} & \frac{\partial y}{\partial r} & \frac{\partial z}{\partial r} \\
\frac{\partial x}{\partial \theta} & \frac{\partial y}{\partial \theta} & \frac{\partial z}{\partial \theta} \\
\frac{\partial x}{\partial \varphi} & \frac{\partial y}{\partial \varphi} & \frac{\partial z}{\partial \varphi} 
\end{vmatrix}
$$

ここで、$r$、$\theta$、$\varphi$は極座標系における変数であり、以下のような関係が成立します。

$$
\begin{aligned} 
x &= r\sin(\varphi)\cos(\theta) \\
y &= r\sin(\varphi)\sin(\theta) \\
z &= r\cos(\varphi)
\end{aligned}
$$

これらの関係を用いて、ヤコビアンを計算します。

まず、各変数の偏微分を求めます。

$$
\begin{aligned}
&\frac{\partial x}{\partial r} = \sin(\varphi)\cos(\theta) \\
&\frac{\partial x}{\partial \theta} = -r\sin(\varphi)\sin(\theta) \\
&\frac{\partial x}{\partial \varphi} = r\cos(\varphi)\cos(\theta) \\
&\frac{\partial y}{\partial r} = \sin(\varphi)\sin(\theta) \\
&\frac{\partial y}{\partial \theta} = r\sin(\varphi)\cos(\theta) \\
&\frac{\partial y}{\partial \varphi} = r\cos(\varphi)\sin(\theta) \\
&\frac{\partial z}{\partial r} = \cos(\varphi) \\
&\frac{\partial z}{\partial \theta} = 0 \\
&\frac{\partial z}{\partial \varphi} = -r\sin(\varphi)
\end{aligned}
$$

これらの式を用いて、ヤコビアンを計算します。

$$
\begin{aligned}
J &= 
\begin{vmatrix}
\sin(\varphi)\cos(\theta) & \sin(\varphi)\sin(\theta) & \cos(\varphi) \\
-r\sin(\varphi)\sin(\theta) & r\sin(\varphi)\cos(\theta) & 0 \\
r\cos(\varphi)\cos(\theta) & r\cos(\varphi)\sin(\theta) & -r\sin(\varphi)
\end{vmatrix} \\
&= (-r\sin^2(\varphi)\cos(\theta)-r\cos^2(\varphi)\cos(\theta))\sin(\varphi)\sin(\theta) 
- (\sin(\varphi)\sin(\theta) \cdot r\cos(\varphi)\cos(\theta) - \sin(\varphi)\cos(\varphi)\cos(\theta) \cdot r\sin(\varphi)\cos(\theta))\sin(\varphi)\cos(\theta) \\
&\quad + (r\cos(\varphi)\cos(\theta) \cdot r\sin(\varphi)\cos(\theta) - r\cos(\varphi)\sin(\theta) \cdot (-r\sin(\varphi)\sin(\theta)))\cos(\varphi) \\
&= r^2\sin(\varphi)\cos^2(\varphi)\sin(\theta)\cos(\theta) - r^2\sin^2(\varphi)\cos^2(\theta)\sin(\theta) + r^2\sin^2(\varphi)\cos(\varphi) \\
&= r^2 \sin(\varphi)
\end{aligned}
$$

よって、3変数 $(x, y, z)$ における極座標系のヤコビアンは$J=r^2\sin(\varphi)$となります。
