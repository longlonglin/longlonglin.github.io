---
title: 'Chernoff Bound'
date: 2017-08-11
permalink: /posts/2017/08/Chernoff-Bound/
tags:
  - Math
  - Probability and Statistics
---

For $i=1,..,n$, let $X_i$ be independent random variables that take the value 1 with  probability $p_i$ and 0 otherwise. Suppose at least one of the $p_i$ is nonzero. Let $X=\sum\limits_{i=1}^N{X_i}$, and let $\mu = E[X] = \sum\limits_{i=1}^N{p_i}$

## Multiplicative Chernoff Bound

#### Upper Tail

We first focus on bounding $Pr[X > (1+\delta)\mu]$ for $\delta > 0$

We have $Pr[X>(1+\delta)\mu] = Pr[e^{tX} > e^{t(1+\delta)\mu}]$ for all $t>0$, later we will select an optimal value for $t$. By Markov's inequality, we have:

$$Pr[e^{tX}>e^{t(1+\delta)\mu}] \le \frac{E[e^{tX}]}{e^{t(1+\delta)\mu}}$$

Then, since the $X_i$ is independent:

$$E[e^{tX}] = E[e^{t(X_1+X_2+...+X_n)}] = E[\prod\limits_{i=1}^N{e^{tX_i}}]=\prod\limits_{i=1}^N{E[e^{tX_i}]}$$

We can compute $E[e^{tX_i}]$ explicitly: this random variable $e^{tX_i}$ is $e^t$ with probability $p_i$, and 1 otherwise (because $X_i$ be independent random variables that take the value 1 with  probability $p_i$ and 0 otherwise)

$$\prod\limits_{i=1}^N{E[e^{tX_i}]} = \prod\limits_{i=1}^N{(p_i\cdot e^t + (1-p_i))} = \prod\limits_{i=1}^N{(1+p_i\cdot(e^t-1))}$$

We have $1+x < e^x$ for all $x>0$. As long as at least one $p_i > 0$, we have:

$$\prod\limits_{i=1}^N{(1+p_i\cdot(e^t-1))} < \prod\limits_{i=1}^N{e^{p_i\cdot(e^t-1)}} = e^{(p_1+p_2+...+p_n)\cdot(e^t-1)} = e^{(e^t-1)\mu}$$

Whence:

$$Pr[X>(1+\delta)\mu]<\frac{e^{(e^t-1)\mu}}{e^{t(1+\delta)\mu}}$$

It's time to choose $t$. Differentiating the right-hand side shows we attain the minimum at $t=\ln(1+\delta)$, which is positive when $\delta$ is. This $t$ value yields Chernoff bound:

$$Pr[X>(1+\delta)\mu] < (\frac{e^\delta}{(1+\delta)^{(1+\delta)}})^\mu$$

#### Lower Tail

We use the same technique to bound $Pr[X<(1-\delta)\mu]$ for $\delta > 0$, then we have:

$$Pr[X<(1-\delta)\mu]=Pr[-X>-(1-\delta)\mu]=Pr[e^{-tX}>e^{-t(1-\delta)\mu}]$$

for any $t>0$, if we proceed as before, that is apply Markov's inequality, use the approximation $1+x<e^x$, then pick $t$ to minimize the bound, we have:

$$Pr[X<(1-\delta)\mu]<(\frac{e^{-\delta}}{(1-\delta)^{(1-\delta)}})^\mu$$

## Bounding the bounds

#### Lower Tail

Above bounds are difficult to use, so in practice we use cruder but friendlier approximations:

Recall $\ln{(1-x)}=-x-\frac{x^2}{2}-\frac{x^3}{3}-...$, thus if $\delta\le 1$, we have:

$$\ln{(1-\delta)>-\delta -\frac{\delta^2}{2}}$$

Exponentiating both sides, raising to the power of $1-\delta$ and dropping the highest order term yields:

$$(1-\delta)^{1-\delta}>e^{-\delta+\frac{\delta^2}{2}}$$

Thus, for $0 < \delta < 1$:

$$Pr[X<(1-\delta)\mu] < e^{-\frac{\delta^2\mu}{2}}$$

## Upper Tail

Similarly, for $Pr[X>(1+\delta)\mu] < (\frac{e^\delta}{(1+\delta)^{(1+\delta)}})^\mu$, by Taylor Series, $\ln{(1+\delta)}=\delta-\frac{\delta^2}{2}+\frac{\delta^3}{3}...$, so 

$$\ln{(1+\delta)}>\delta - \frac{\delta^2}{2}+\frac{\delta^3}{3}$$

Exponentiating both sides, raising to the power of $1+\delta$ and dropping the highest order term yields:

$$(1+\delta)^{1+\delta}> e^{\delta+\frac{\delta^2}{2}-\frac{\delta^3}{6}}$$

Thus,

$$ (\frac{e^\delta}{(1+\delta)^{(1+\delta)}})^\mu < (e^{-\frac{\delta^2}{2}+\frac{\delta^3}{6}})^{\mu}$$

With the fact that $0 \le \delta\le1$, so $\delta^3 < \delta^2 \Longrightarrow -3\delta^2+\delta^3\le -2\delta^2 \Longrightarrow -\frac{\delta^2}{2}+\frac{\delta^3}{6}\le -\frac{\delta^2}{3}$

$$ (\frac{e^\delta}{(1+\delta)^{(1+\delta)}})^\mu < (e^{-\frac{\delta^2}{3}})^{\mu}$$

Finally,

$$Pr[X>(1+\delta)\mu] < e^{-\frac{\delta^2\mu}{3}}$$

In addition, If we use Inequality $\ln(1+\delta)\ge \frac\delta{1+\frac\delta{2}}$, we can also derive that

$$Pr[X>(1+\delta)\mu] < e^{-\frac{\delta^2\mu}{2+\delta}}$$

Since $e^{-\frac{\delta^2\mu}{2+\delta}} < e^{-\frac{\delta^2\mu}{3}}$, this new upper bound is tighter

## Two-sided Chernoff Bound

Moreover, $e^{-\frac{\delta^2\mu}{3}}>e^{-\frac{\delta^2\mu}{2}}$

$$Pr[ |X-\mu| > \delta\mu] < 2e^{-\frac{\delta^2\mu}{3}} $$

Or

$$Pr[ |X-E(X)| > \delta E(X)] < 2e^{-\frac{\delta^2E(X)}{3}} $$

If using tighter bound,

$$Pr[ |X-E(X)| > \delta E(X)] < 2e^{-\frac{\delta^2E(X)}{2+\delta}} $$

## References

[1] [http://crypto.stanford.edu/~blynn/pr/chernoff.html](http://crypto.stanford.edu/~blynn/pr/chernoff.html)

[2] [Randomized Algorithms by Motwani and Raghavan](https://rajsain.files.wordpress.com/2013/11/randomized-algorithms-motwani-and-raghavan.pdf)

[3] [http://www.cs.rochester.edu/u/ltran/robust/PROOFS.PDF](http://www.cs.rochester.edu/u/ltran/robust/PROOFS.PDF)