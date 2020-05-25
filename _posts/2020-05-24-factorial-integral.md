---
layout: post
title: "A fun integral"
date: 2020-05-24
---

I found this piece in a folder named "Math derivations" which I created in 2017 in the summer after my college graduation. Posting here for your enjoyment :)

---

Today, I had to solve the integral:

$$\int_0^\infty x^3 \ \exp\left(-x^2\right) \ \mathrm{d}x $$

It is probably solvable by parts, but being lazy and being a fan of Feynman, I decided to differentiate under the integral sign

I started with the integral:

\begin{align}
        \int_0^\infty x \ \exp\left(-Mx^2\right) \ \mathrm{d}x = \frac{-1}{2M} \ \left.\exp\left(-Mx^2\right) \right|_0^\infty = \frac{1}{2M}
\end{align}

Now comes the trick: I differentiated both sides *with respect to M*, several times...

\begin{align}
    \int_0^\infty x^3 \ \exp\left(-Mx^2\right) \ \mathrm{d}x = \frac{1}{2M^2} \\[1em]
    \int_0^\infty x^5 \ \exp\left(-Mx^2\right) \ \mathrm{d}x = \frac{2}{2M^3} \\[1em]
    \int_0^\infty x^7 \ \exp\left(-Mx^2\right) \ \mathrm{d}x = \frac{6}{2M^4}
\end{align}

Have you noticed a pattern? It is easy to see (and trivial to prove by induction) that

\begin{align}
    \int_0^\infty x^{2n-1} \ \exp\left(-Mx^2\right) \ \mathrm{d}x = \frac{(n-1)!}{2M^n}
\end{align}

We're done! By replacing $M = 1$ and $n = 2$, my original integral is solved. We also arrived at a more general formula to solve the integral for odd powers of $x$. 

But the fun doesn't stop there. Let's put $M=1$ to get

$$(n-1)! = 2\int_0^\infty x^{2n-1} \ \exp\left(-x^2\right) \ \mathrm{d}x$$

A simple change of variable $t=x^2$ gets us:

$$(n-1)! = \int_0^\infty t^{n-1} \ \exp\left(-t\right) \ \mathrm{d}t$$

Guess what, the right hand side is exactly the Gamma function, which is the natural extension of the factorial function to real numbers.

$$(n-1)! = \Gamma(n) = \int_0^\infty t^{n-1} \ e^{-t} \ \mathrm{d}t$$

And that is pretty neat.





