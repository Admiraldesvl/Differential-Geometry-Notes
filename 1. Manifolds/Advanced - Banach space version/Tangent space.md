## Definition

Let $X$ be a manifold of class $C^p$ with $p \geq 1$. Let $x$ be a point of $X$. Consider the triple
$$
(U,\varphi,v)
$$
where $(U,\varphi)$ is a triple and $x \in U$, and $v$ is an element of the vector space in which $\varphi(U)$ lies.

> **(Equivalence relation)** Two such triples $(U,\varphi,v)$ and $(V,\psi,w)$ are **equivalent** if we have
> $$
> (\psi\circ\varphi^{-1})'(\varphi(x))v=w.
> $$
> That means, the derivative of $\psi\circ\varphi^{-1}$ at *the point* $\varphi(x)$, which is a *linear operator*, maps $v$ to $w$. 

*Proof of equivalence relation.* We say $(U,\varphi,v)\sim(V,\psi,w)$ if the equation above holds. A word of warning: by definition of $C^p$-manifold, we do not know whether $\varphi$ is a $C^p$-morphism or not. All we know is that $\varphi\circ\psi^{-1}$ and $\psi\circ\varphi^{-1}$ are $C^p$-morphisms.

First, we shall show that $(U,\varphi,v)\sim(U,\varphi,v)$. One only needs to notice that
$$
\operatorname{id}'(y)=(\varphi\circ\varphi^{-1})'(y)=\operatorname{id}
$$
for all $y$. That is,
$$
(\varphi\circ\varphi^{-1})'(\varphi(x))v=v.
$$
Second, if $(U,\varphi,v)\sim(V,\psi,w)$, then $(V,\psi,w)\sim(U,\varphi,v)$. Equivalently, we shall prove that if
$$
(\psi\circ\varphi^{-1})'(\varphi(x))v=w,
$$
then
$$
(\varphi\circ\psi^{-1})'(\psi(x))w=v.
$$
Since we have
$$
(\varphi\circ\psi^{-1})'(\psi(x))w=(\varphi\circ\psi^{-1})'(\psi(x))\circ(\psi\circ\varphi^{-1})'(\varphi(x))v,
$$
we only need to show that the composition of linear operators on the right side is the identity map.

Notice we have
$$
\operatorname{id}'(y)=(\varphi\circ\psi^{-1}\circ\psi\circ\varphi^{-1})'(y)=(\varphi\circ\psi^{-1})(\psi\circ\varphi^{-1}(y))\circ(\psi\circ\varphi^{-1})(y)
$$
By putting $y=\varphi(x)$, we have
$$
\operatorname{id}'(\varphi(x))=\operatorname{id}=(\varphi\circ\psi^{-1})(\psi(x))\circ(\psi\circ\varphi^{-1})(\varphi(x)).
$$
Finally, if $(U,\varphi,v)\sim(V,\psi,w)$, $(V,\psi,w)\sim(W,\rho,u)$, then $(U,\varphi,v)\sim(W,\rho,u)$. That said, we now have
$$
(\psi\circ\varphi^{-1})'(\varphi(x))v=w
$$
and
$$
(\rho\circ\psi^{-1})'(\psi(x))w=u,
$$
we need to prove that
$$
(\rho\circ\varphi^{-1})'(\varphi(x))v=u,
$$
or equivalently,
$$
(\varphi\circ\rho^{-1})(\rho(x))u=v
$$


Again, we only need to show that
$$
(\varphi\circ\rho^{-1})'(\rho(x))\circ(\rho\circ\psi^{-1})'(\psi(x))\circ(\psi\circ\varphi^{-1})'(\varphi(x))=\operatorname{id}.
$$
To do this, notice that
$$
\operatorname{id}'(y)=\{(\varphi\circ\rho^{-1})\circ(\rho\circ\psi^{-1})\circ(\psi\circ\varphi^{-1})\}'(y)=\{(\varphi\circ\rho^{-1})\circ(\rho\circ\psi^{-1})\}'(\psi\circ\varphi^{-1}(y))\circ(\psi\circ\varphi^{-1})'(y)
$$
Meanwhile
$$
\begin{aligned}
\{(\varphi\circ\rho^{-1})\circ(\rho\circ\psi^{-1})\}'(\psi\circ\varphi^{-1}(y))&=(\varphi\circ\rho^{-1})'(\rho\circ\psi^{-1}(\psi\circ\varphi^{-1}(y)))\circ(\rho\circ\psi^{-1})'(\psi\circ\varphi^{-1}(y)) \\
&=(\varphi\circ\rho^{-1})'(\rho\circ\varphi^{-1}(y))\circ(\rho\circ\psi^{-1})'(\psi\circ\varphi^{-1}(y))
\end{aligned}
$$
Therefore we finally get
$$
\operatorname{id}'(\varphi(x))=(\varphi\circ\rho^{-1})'(\rho(x))\circ(\rho\circ\psi^{-1})'(\psi(x))\circ(\psi\circ\varphi^{-1})'(\varphi(x))=\operatorname{id}
$$
as desired.

---

An equivalence class of such triples is called a **tangent vector** of $X$ at $x$. The set of such tangent vectors is called the **tangent space** of $X$ at $x$, which will be denoted by $T_x(X)$. Each chart $(U,\varphi)$ determines a bijection of $T_x(X)$ on a Banach space, namely the equivalence class of $(U,\varphi,v)$ corresponds to the vector $v$. By means of such a bijection, it is possible to transport to $T_x(X)$ the structure of topological vector space given by the chart, and it is immediate that the structure is independent of the chart selected. 

## Derivative

Recall that, if $U,V$ are open in Banach spaces, then to every morphism of class $C^p$, we are able to associate its derivative $Df(x)$ to each point $x$. If now $f:X \to Y$ is a morphism of one manifold into another, then by means of charts, we can interpret the derivative of $f$ on each chart at $x$ as a mapping
$$
df(x)=T_xf:T_x(X) \to T_{f(x)}(Y)
$$
which has the following properties. If $(U,\varphi)$ is a chart at $x$ and $(V,\psi)$ is a chart at $f(x)$ such that $f(U) \subset V$, and $\overline{v}$ is a tangent vector at $x$ represented by $v$ in the chart $(U,\varphi)$, then
$$
T_xf(\overline{v})
$$
is the tangent vector at $f(x)$ represented by $Df_{V,U}(x)v$. //TODO: a commutative diagram.