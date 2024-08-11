---
title: A motivation for Taylor's Theorem
description: Using definitions and examples to attmept to motivate Taylor's Theorem
author: Kush R
categories: [Calculus]
tags: [Calculus]
math: true
---


# A motivation for Taylor's Theorem
First define $o(\Delta t)$ as the set of all real-valued functions $g$ such that 
$$ \lim \limits_{t \to 0} \frac{g(\Delta t)} {\Delta t} = 0$$
Here, we regard $\Delta t$ as a variable in and of itself. However, for the sake of intuition, putting $\Delta t = s-t$ and using the properties of the derivative will yield the observation that we can approximate $f(t + \Delta t) = f(t) + f'(t) \Delta t + o(\Delta t)$, or $f(s) = f(t) + f'(t)(s-t) + o(s-t)$. Regardless, the quantity $\Delta t$ can be regarded as a variable. 

Without proof, we assert that $f = o(\Delta t)$ if $$\lim_{\Delta t \to 0} \left | \frac{f(\Delta t)}{\Delta t} \right| = 0$$
Intuitively, all this means is that the function $f(\Delta t)$ gets closer and closer to $0$ as $\Delta t$ gets smaller and smaller, or that the points get closer and closer together. We use this fact to develop a linear approximation. Consider the following graphic: 
![enter image description here](https://i.ibb.co/2nYVtvF/image.png)
More  specifically, observe that as the blue line gets closer to the point where the blue and red line intersect, the value of g(x) on the blue line approaches the "true" value of f(x), which is on the red line. That is to say, the blue line is a linear approximation of the red graph, centered at point $x=2$. Formally, we say $$f(t + \Delta t) = f(t) + f'(t) \Delta t + o(\Delta t)$$
But what if we wanted a better approximation than a linear one, say a quadratic approximation? As a consequence of the above definition, it is clear that $f = o(g)$ for some function $g$ if $$\lim \limits_{\Delta t \to 0} \frac{f(\Delta t)}{g(\Delta t)} = 0 $$
What we want to do, is find $a,b,c \in \mathbb R$ such that: $$f(t + \Delta t) = a + b \Delta t + c \Delta t^2 + o(\Delta t^2)$$ Please note that as a notational choice, we regard $\Delta t^2 = (\Delta t)^2$. Additionally, all these equations are approximations. Another way of expressing this idea is as follows:
Let $p(x)$ be our quadratic approximation. We know that this implies that $f(x) = p(x)$ for two derivatives. Now put $p(x) = c_2 x^2 + c_1 x + c_0$. We know that $p(0) = f(0), p'(0) = f'(0), p''(0) = f''(0)$. This yields $c_0 = f_0, c_1 = f'(0), c_2 = \frac 1 2 f''(0)$, which makes our quadratic polynomial $p(x) = f(0) + f'(0)x + \frac{f''(0)}{2}x^2$. Applying this idea to our established use of $\Delta t$ in the more general sense:
if $$f(t + \Delta t) \approx a + b \Delta t + c \Delta t^2$$ then clearly we see putting $\Delta t = 0$ yields $f(t) \approx a$. By our example of $p(x)$, we know the derivatives should match, which means $f'(t + \Delta t) \approx b + 2c \Delta t$, and again putting $\Delta t = 0$ shows us that $f'(t) \approx b$. Taking the second derivative shows us $f''(t + \Delta t) \approx 2c$, meaning $f''(t) = 2c$. Now, moving things around with algebra to get $a,b,c$ alone on one side, we see that $$ f( t + \Delta t) = f(t) + f'(t) \delta T + \frac{f''(t)}{2} \Delta t^2 + o(\Delta t ^2)$$
Remember, since we can always put $\Delta t = s - t$, we will always have a quadratic approximation centered at  $t$. The end goal here is to get a degree-$n$ approximation polynomial, known as a Taylor Polynomial. The essential observation we must make here is that, for any $x^n$, the $n$-th derivative will always be $n!$, which means our "approximation" value will always be $\frac{f^{n}(t)}{n!} \Delta t^n$. Putting this together, we define the n-th degree taylor polynomial as:
$$ f(t + \Delta t) = \frac{f(t)}{0!} + \frac{f'(t)}{1} \Delta t^1 + \frac{f''(t)}{2!} \Delta t^2 + \dots + \frac{f^{n}(t)}{n!} \Delta t^n + o(\Delta t^n)  $$ $$ \newline = \sum_{k=0}^{n} \frac{f^{k}(t)}{k!} \Delta t^k + o(\Delta t^n)$$
