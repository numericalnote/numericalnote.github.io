---
title: The Derivative and the Definite Integral
author: kush
date: 2024-01-12 10:59:00 -0500
categories: [Mathematics, Calculus]
tags: [derivative, integral, fundamental theorem of calculus]
render_with_liquid: false
math: true
---

The connection between the integral and derivative is not always apparent, however insight can be gained through deriving one of the most important results of single-variable calculus: the first fundamental theorem of calculus. The theorem states that:

$$ \int_{a}^{b} f(x)\,dx = F(b) - F(a) $$

Where $$F$$ represents a function with derivative f, such that

$$F' = f$$

This connection, however, between the rate of change of a function and the area under its curve, is not apparent. 

To compute $$\int_{a}^{b} f(x) dx$$ with $$f(x)$$ being continuous on $$[a,b]$$, let $$F$$ be a function who has the derivative of f, and let $$\mathcal{P}$$ be a partition such that:

$$a = x_o < x_1 \dots < x_n = b$$

Here, the partition represents the width of rectangles drawn under the curve, as in the following image:


The Mean Value Theorem (MVT) can be applied each slice of the partition, which allows for the following statement:

$$f(z_i) = \dfrac{F(x_{i+1}) - F(x_i)}{x_{i+1} - x_i}$$

To simplify this, we can multiply the denominator over on both sides, and have: 

$$f(z_i)(x_{i+1} - x_i) = F(x_{i+1}) - F(x_i)$$

This can then be summed over the entire partition, and we have:

$$\displaystyle\sum_{i=0}^{n-1} f(z_i)(x_{i+1} - x_i) = \displaystyle\sum_{i=0}^{n-1} F(x_{i+1}) - F(x_i)$$

The left hand side of this equation represents a Riemann Sum. In short, a Riemann Sum is a sum of rectangles under a curve, which approximates the area. Typically, a Riemann Sum uses an underestimation of the area under the curve by drawing a rectangle at the minimum value of $$f(x)$$ on an interval, and an overestimation by the maximum value. Then, with either of these height values, because of the rectangle area formula, we multiply this height value by $$x_{i+1} - x_i$$, and sum this over the partition to approximate area.
