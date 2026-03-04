With conditional information on the level of distribution of the primes, the author shows that there are infinitely often two primes in a given $k$-tuple for sufficiently large $k$. With the same approach unconditionally, the author establishes the existence of very small gaps between primes which go slowly compare to the size of primes.

Let $n \in \mathbb{N}$, $\mathcal{H}=\{h_1,\ldots,h_k\}$, $h_i\in \mathbb{N}\cup\{0\}$, $h_i < h_j \le h$, $i < j$, the $k$-tuple is

$$
(n+h_1,\, n+h_2,\, \ldots,\, n+h_k).
$$

Let $\nu_p(\mathcal{H})$ denote the number of distinct residue classes modulo $p$ occupied by the integers $h_i$, and called $\mathcal{H}$ is admissible if $\nu_p(\mathcal{H}) < p$ for all $p$ primes. For square free $d$, we extend the definition to $\nu_d(\mathcal{H})$ by multiplicity. Take $N > h_k$, the goal is to construct a suitable $w(n) \ge 0$ for which

$$
\sum_{N < n \le 2N}\left(\sum_{i=1}^k \theta(n+h_i)-\rho\log 3N\right)w(n) > 0.
$$

where $\rho > 0$. This yields that there exist $n\in (N,2N]$, s.t. there are at least $\lfloor \rho \rfloor +1$ prime components in the $k$-tuple. Therefore, $w(n)$ functions to detect the prime components of this tuple and it is natural to use the Selberg-style weight

$$
w(n)=\left(\sum_{\substack{d\mid P(n)\\ d\le R}} \lambda(d)\right)^2
$$

where $P(n)=(n+h_1)\cdots(n+h_k)$, $R < N^{\frac15}$. In their arguement, they relied on the $k$-th generalized Von Mangoldt function

$$
\Lambda_k(n)=\frac{1}{k!}\sum_{d\mid n}\mu(d)\left(\log \frac{n}{d}\right)^k
$$

which vanishes if $n$ has more than $k$ distinct prime factors. Hence, they select

$$
W(n):=\left(\sum_{\substack{d\mid P(n)\\ d\le R}} \mu(d)\,\frac{1}{m!}\left(\log \frac{R}{d}\right)^m\right)^2,
$$

$$
\lambda(d):=\mu(d)\,\frac{1}{m!}\left(\log \frac{R}{d}\right)^m
$$

for some $m=k+\ell$. Note if a component is highly composite then the whole weight would be dragged down to $0$.


Let

$$
\mathfrak{S}(\mathcal{H}):=\prod_p \left(1-\frac{1}{p}\right)^{-k}\left(1-\frac{\nu_p(\mathcal{H})}{p}\right).
$$

since $\nu_p(\mathcal{H})=k$ for $p > h$ if admissible, then such singular series is convergent. We expand the sum above and obtain

$$
\sum_{d_1,d_2\le R}\lambda(d_1)\lambda(d_2)
\left(
\sum_{i=1}^k \sum_{\substack{N < n \le 2N\\ [d_1,d_2]\mid P(n)}} \theta(n+h_i)
-\rho\log 3N \sum_{\substack{N < n \le 2N\\ [d_1,d_2]\mid P(n)}} 1
\right).
$$

Notice that for $p\mid P(n)$, then $n\equiv -h_i\pmod p$ for some $h_i$'s, and $\nu_p(\mathcal{H})$ counts the number of solutions of $n$ modulo $p$. Then by the Chinese Remainder Theorem, we have the parentheses in the above equal to

$$
k\left(\nu_q(\mathcal{H})^*\right)\left(\frac{X_N}{\varphi(q)}+O(E(N,q))\right)
-\rho\log 3N\, \nu_q(\mathcal{H})\left(\frac{N}{q}+O(1)\right)
$$

where

$$
q=[d_1,d_2],
$$

$$
X_N=\sum_{N < n \le 2N}\theta(n),
$$

$$
E(N,q)=\sup_{(a,q)=1}\left|\sum_{\substack{N < n \le 2N\\ n\equiv a\, (\mathrm{mod}\ q)}}\theta(n)-\frac{X_N}{\varphi(q)}\right|,
$$

$$
\nu_q(\mathcal{H})^*=(\nu_{p_{{\alpha}_1}}(\mathcal{H})-1)\cdots(\nu_{p_{{\alpha}_t}}(\mathcal{H})-1),
\qquad q=p_{{\alpha}_1}\cdots p_{{\alpha}_t},
$$

since for $p\mid P(n)$, $n\equiv -h_j\pmod p$, $n+h_i\equiv h_i-h_j\pmod p$,  and we need $(h_i-h_j,p)=1$ for $\theta(n+h_i)\ne 0$, thus $\nu_p(\mathcal{H})-1$ residue classes modulo $p$.

We first deal with the error term. Let $\omega(q)$ be the number of prime divisors of $q$, then $\nu_q(\mathcal{H})\le k^{\omega(q)}=d_k(q)$. The error is then bounded by

$$
(\log R)^{2m}k\sum_{q\le R^2}\mu(q)^2\, d_k(q)\, d_3(q)\, E(N,q)
$$

where we have the number of possible $q=[d_1,d_2]$ with $d_1,d_2\le R$ is bounded by the number of representations of $q$ written as $3$ factors, i.e. $d_3(q)$. Give the bound

$$
\sum_{q\le x}\mu(q)^2\frac{d_k(q)}{q}\le (k+1+\log x)^{k+1},
\qquad
\sum_{q\le x}\mu(q)^2 d_k(q)\le x(k+1+\log x)^{k+1},
$$

we have the error is

$$
kR^2(3\log R)^{3k+2m+1}+k(\log R)^{2m}
\sqrt{\sum_{q\le R^2}\frac{\mu(q)^2d_{9k^2}(q)}{q}}
\sqrt{\sum_{q\le R^2} q(E(N,q)-1)^2}.
$$

by the trivial bound for $E(N,q)-1\le \dfrac{2N}{q}\log N$, we have the bound for the latter term

$$
\ll k(\log R)^{2m}\sqrt{\log(R)^{k+2\ell}}\sqrt{2N\log N}
\sqrt{\sum_{q\le R^2}(E(N,q)-1)}
$$

$$
\ll kN(\log N)^{\frac{9k^2+1-A}{2}}
$$

where we applied the Bombieri-Vinogradov Theorem by letting $R\ll N^{\frac14}/\log N^B, B=B(m,A) \text{ where } m,A,k\le \sqrt{\log N}/18 \text{ are constants}.$ Hence, the error is $N^{1-\varepsilon}$.


The author uses the Perron's Formula to calculate the main term.  
Let $(c)$ denote the contour $s=c+it$, $-\infty < t < \infty$. For $c > 0$, we have

$$
\frac{1}{2\pi i}\int_{(c)} \frac{x^s}{s^{k+1}}\,ds=
\begin{cases}
0 & \text{if } 0 \le x \le 1,\\[4pt]
\dfrac{1}{k!}(\log x)^k & \text{if } x \ge 1.
\end{cases}
$$

Then it gives

$$
\sum_{d\le R}\frac{\lambda(d)\nu_d(\mathcal{H})}{d}
=\frac{1}{2\pi i}\int_{(1)} F(s)\frac{R^s}{s^{k+1}}\,ds
$$

where

$$
F(s)=\sum_{d=1}^{\infty}\frac{\mu(d)\nu_d(\mathcal{H})}{d^{1+s}}
=\prod_p\left(1-\frac{\nu_p(\mathcal{H})}{p^{1+s}}\right).
$$

We write

$$
G_{\mathcal{H}}(s)=\prod_p\left(1-\frac{\nu_p(\mathcal{H})}{p^{1+s}}\right)
\left(1-\frac{1}{p^{1+s}}\right)^{-k}
$$

$$
=\prod_p\left(1+\frac{k-\nu_p(\mathcal{H})}{p^{1+s}}+O_h\!\left(\frac{k^2}{p^{2+2\sigma}}\right)\right)
$$

since $\nu_p(\mathcal{H})=k$ for $p > h$, then it is analytic and uniformly bounded for $\sigma > -\frac12+\delta$ for any $\delta > 0$. Also, we see that

$$
F(s)=\frac{G_{\mathcal{H}}(s)}{s(1+s)^k},
\qquad G_{\mathcal{H}}(0)=\mathfrak{S}(\mathcal{H}).
$$

Note, if $\mathcal{H}$ not admissible, then the integrand has a simple pole at $0$ in the region bounded by $\mathcal{L}: s=-\dfrac{c}{\log(|t|+2)}+it$ and $(1)$ with residue $\mathfrak{S}(\mathcal{H})$; if $\mathcal{H}$ is not admissible, then it is analytic everywhere. Therefore, we can calculate the integral by moving to the contour $\mathcal{L}$, plus an extra term of $\mathfrak{S}(\mathcal{H})$.  
As for the main term, we write $d_1=a_1a_{12}$ and $d_2=a_2a_{12}$, $a_1,a_2,a_{12}$ are relative prime to each other, then $q=a_1a_2a_{12}$. Therefore, after some expansion of terms, we may apply the Perron's Formula twice and obtain new $F(s_1,s_2)$, $G_{\mathcal{H}}(s_1,s_2)$ with $G_{\mathcal{H}}(0,0)=\mathfrak{S}(\mathcal{H})$, Then we are done by evaluating the integral.
