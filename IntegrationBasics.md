---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
---

# Welcome to Calculus BC!

Presentation slides made by itsdawei

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 p-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>


<!--TODO: replace with my own github; also git inti this project-->
<a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
  class="abs-br m-6 text-xl icon-btn opacity-50 !border-none !hover:text-white">
  <carbon-logo-github />
</a>

---

# Review: Integration Rules

1. $\int f(x)dx = F(x) + C$ if and only if $F'(x) = f(x)$
2. $\int a f(x)dx = a \int f(x) dx$
3. $\int -f(x)dx = - \int f(x) dx$
4. $\int [f(x) \pm g(x)]dx = \int f(x) dx \pm \int g(x) dx$

<br>

### Remark
$$
\int f(x) \cdot g(x) dx \ne \int f(x) dx \cdot \int g(x) dx
$$

<br>

### Bad Example
(32) Evaluate $\int x^2 \cos x dx$.
$$
\int x^2 \cdot \int \cos x dx = \frac{x^3}{3} \cdot \sin x + C
$$

---

# The U-Substitution Method

<v-clicks>

## The Chain Rule for Differentiation
$$
\frac{d}{dx}F(g(x)) = f(g(x))g'(x), \text{ where } F' = f
$$

## The Integral of a Composite Function
$$
\int f(g(x))g'(x)dx = F(g(x)) + C
$$

## Making a U-Substitution
Let $u = g(x)$, then $du = g'(x)dx$
$$
\int f(g(x))g'(x)dx = \int f(u)du = F(u) + C = F(g(x))+C
$$

</v-clicks>

---

# Procedure for U-Substitution
1. Given $f(g(x))$; let $u = g(x)$.
2. Differentiate: $du = g'(x)dx$.
3. Rewrite the integral in terms of $u$.
4. Evaluate the integral.
5. Replace $u$ by $g(x)$.
6. Check your result by taking the derivative of the answer.

<br>

## Try it yourself
(29) If $f(x)$ is an antiderivative of $\frac{e^x}{e^x+1}$ and $f(0) = \ln(2)$,
find $f(\ln 2)$. 

Evaluate $\int \frac{x^2}{(x^3-8)^5} dx$.

Evaluate $\int 3(\sec^2 x) \sqrt{\tan x} dx$

Evaluate $\int 2x^2 \cos(x^3) dx$

---

# Integration by Parts

<br>

$$ \begin{aligned}
\frac{d}{dx}(uv) = u\frac{dv}{dx} + v \frac{du}{dx} \\
uv = \int u\frac{dv}{dx} + \int v\frac{du}{dx} \\
\int u \frac{dv}{dx} = uv - \int v \frac{du}{dx}
\end{aligned} $$

<v-click>

## How to Choose $u$ and $dv$? (LIPET)
- **L**ogarithmic
- **I**nverse Trig.
- **P**olynomial
- **E**xponential
- **T**rig.

</v-click>

---

# Try it yourself

<br>

<v-clicks>

$\int xe^{-x}dx$

Let $u = x$ and $dv = e^{-x}dx$ since $x$ is a **P**olynomial, which comes
before **E**xponential in **LIPET**.

$$
\int xe^{-x}dx = -xe^{-x} - \int -e^{-x}dx = -xe^{-x} - e^{-x} + C
$$

$\int x \sin(4x) dx$

Let $u = x$ and $dv = \sin(4x)$, since $x$ is a **P**olynomial, which comes
before **T**rig in **LIPET**.

$$
\int x \sin(4x)dx = \frac{-x}{4}\cos(4x) + \frac{1}{4}\int\cos(4x)dx =
\frac{-x}{4}\cos{4x} + \frac{1}{16}\sin(4x)+C
$$

</v-clicks>

---

# Integration by Partial Fractions

<br>

$\int \frac{dx}{x^2+3x-4}$

$\int \frac{x^5 + 2x^2 + 1}{x^3 - x}$

---

# Integration Practice

1. Evaluate $\int\frac{1}{x^2}dx$.
2. Evaluate $\int\frac{x^3-1}{x}dx$.
3. Evaluate $\int x \sqrt{x^2-1}dx$.
4. Evaluate $\int \sin{x} dx$
5. Evaluate $\int \cos(2x) dx$
6. Evaluate $\int \frac{\ln{x}}{x}dx$
7. Evaluate $\int xe^{x^2}dx$
8. $\int x \cos x dx$
9. $\int \frac{5}{(x+3)(x-7)}dx$

---

## Evaluate $\int\frac{1}{x^2}dx$.
<v-click>

Rewrite as $\int x^{-2}dx = \frac{x^{-1}}{-1} + C = -\frac{1}{x} + C$.

</v-click>

## Evaluate $\int\frac{x^3-1}{x}dx$.
<v-click>

Rewrite as $\int (x^2-\frac{1}{x})dx = \frac{x^3}{3} - \ln |x| +C$.

</v-click>

## Evaluate $\int x \sqrt{x^2-1}dx$.
<v-clicks>

Rewrite as $\int x(x^2-1)^{1/2}dx$. Let $u = x^2-1$.

Thus, $\frac{du}{2} = xdx \to \frac{1}{2}\int u^{1/2}du = \frac{u^{3/2}}{2^{3/2}} + C
= \frac{1}{3}(x^2-1)^{3/2} + C$.

</v-clicks>

---

## Evaluate $\int \sin{x} dx$
<v-click>

$-\cos x + C$

</v-click>

## Evaluate $\int \cos(2x) dx$
<v-click>

Let $u = 2x$ and obtain $\frac{1}{2}\sin 2x + C$.

</v-click>

## Evaluate $\int \frac{\ln{x}}{x}dx$
<v-click>

Let $u = \ln x$; $du = \frac{1}{x}dx$ and obtain $\frac{(\ln x)^2}{2}+C$.

</v-click>

---

## Evaluate $\int xe^{x^2}dx$
<v-click>

Let $u = x^2$; $\frac{du}{2} = xdx$ and obtain $\frac{e^{x^2}}{2}+C$ 

</v-click>

## $\int x \cos x dx$
<v-clicks>

Let $u=x$, $du=dx$, $dv=\cos x dx$, and $v=\sin x$,

then $\int x \cos x dx = x \sin x - \int \sin x dx = x \sin x + \cos x + C$

</v-clicks>

## $\int \frac{5}{(x+3)(x-7)}dx$
<v-click>

Rewrite as $\int (\frac{-1/2}{x+3} + \frac{1/2}{x-7})$, then solve:
$$
\begin{aligned}
\int (\frac{-1/2}{x+3} + \frac{1/2}{x-7}) =& -\frac{1}{2}\ln |x+3| + \frac{1}{2}\ln |x-7| + C \\
=& \frac{1}{2} \ln |\frac{x-7}{x+3}|+C
\end{aligned}
$$

</v-click>

<style>
h2 {
  margin: 0
}

</style>

---

# Homework

Practice Problems 1 to 25

---
