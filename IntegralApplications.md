---
# try also 'default' to start simple
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
---

# Integration Applications

Presentation slides made by _itsdawei_

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 p-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>


<a href="https://github.com/itsdawei/calcbc_slidev" target="_blank" alt="GitHub"
  class="abs-br m-6 text-xl icon-btn opacity-50 !border-none !hover:text-white">
  <carbon-logo-github />
</a>

---

# Riemann Sums (The Rectangle Method)

(47) Let $f$ be a continuous function on [0,6] that has selected values as shown
below:

| $x$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
|---|---|---|---|---|---|---|---|
| $f(x)$ | 1 | 2 | 5 | 10 | 17 | 26 | 37 |

Using three midpoint rectangles of equal widths, find an approximate value of

$$
\int^6_0 f(x) dx
$$

---

# First Fundamental Theorem of Calculus
If $f$ is continuous on $[a,b]$ and $F$ is an antiderivative of $f$ on $[a, b]$,
then

$$
\int^b_a f(x) dx = F(b) - F(a).
$$

## Try it yourself
Evaluate $\int^2_0 (4x^3+x-1)dx$

Evaluate $\int^\pi_{-\pi}\sin x dx$

If $\int^k_{-2} (4x+1)dx = 30$, $k>0$, find $k$.

If $f'(x) = g(x)$, and $g$ is a continuous function for all real values of $x$,
express $\int^5_2 g(3x) dx$ in terms of $f$.

Evaluate $\int^4_0 \frac{1}{x-1} dx$

Using a graphing calculator, evaluate $\int^2_{-2} \sqrt{4-x^2}dx$.

---

# Second Fundamental Theorem of Calculus
If $f$ is continuous on $[a,b]$ and $F(x) = \int^x_a f(t) dt$, then $F'(x) = f(x)$
at every point $x$ in $[a,b]$. In other words,

$$
\frac{d}{dx} \int^x_a f(t) dt = f(x)
$$

## Try it yourself

Evaluate $\int^\pi_{\pi/4} \cos(2t) dt$.

If $h(x) = \int^x_3 \sqrt{t+1} dt$ find $h'(8)$.

Find $\frac{dy}{dx}$; if $y = \int_1^{2x} \frac{1}{t^3} dt$.

Find $\frac{dy}{dx}$; if $y = \int^1_{x^2} \sin t dt$.

Find $\frac{dy}{dx}$; if $y = \int_{x}^{x^2} \sqrt{e^t+1} dt$.

---

# Checkpoint 

$F(x) = \int^x_1 (t^2 - 4) dt$, integrate to find $F(x)$ and then differentiate
to find $f'(x)$.

<v-click>

$$
\begin{aligned}
F(x) =& \left[\frac{t^3}{3} - 4t\right]^x_1 \\
=& \left(\frac{x^3}{3} - 4x\right) - \left( \frac{1^3}{3} - 4(1)\right)
\end{aligned}
$$

</v-click>

<v-click>

$$
F'(x) = 3\left(\frac{x^2}{3}\right) - 4 = x^2 - 4
$$

</v-click>

---

# Improper Integrals

For infinite intervals of integration,

$$
\int^\infty_a f(x)dx = \lim_{l\to\infty}\int_a^l f(x) dx
$$

$$
\int^b_{-\infty}f(x)dx = \lim_{l \to -\infty}\int^b_l f(x) dx
$$

$$
\int_{-\infty}^{\infty}f(x)dx = \int_{-\infty}^c f(x) dx + \int_c^{\infty} f(x) dx
$$

## Practice

Evaluate $\int^\infty_1 \frac{1}{x}dx$.

Evaluate $\int^\infty_{-\infty} xe^{-x^2} dx$.

---

# Infinite Discontinuities



