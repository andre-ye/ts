---
layout: default
title: Lecture Notes
parent: MATH 125
grand_parent: Mathematics
nav_order: 1
---

# Lecture Notes

MATH 125
{: .fs-6 .fw-300 }

---

## Navigation

---


## Week 1 Monday - Antiderivatives and Syllabus

### Exams
- Two midterms; not that much time in between midterms.
- Standard calculator and 2-sided cheat sheet is allowed.
 
### Assignments
- Homework is due on Tuesdays at 11:00 PM.
- Quizes are between 9 AM and 11 AM on WebAssign based on the homework. These are 30 minutes. No makeups or quizzes are granted. Relatively short - designed to be completed in 20 to 30 minutes.
  - Material for Quizzes on Tuesday are the same as homework due that Tuesday.
- Worksheets are given during Thursday section with the TA. These are designed to give an opportunity to work on more complex problems. Graded on completion basis.

### Class Administrative
- Lectures will generally be recorded

### 4.9: The Antiderivative
- You are familiar with a derivative; the antiderivative is the 'opposite'

> **Definition**: A function $$F(x)$$ is an *antiderivative* of a function $f(x)$ is $$F'(x) = f(x)$$ for al $$x$$.

- Computing the antiderivative is much more difficult than taking the derivative
- Suppose $$f(x) = x^2$$. We have $$F(x) = \frac{x^3}{3}$$ as the antiderivative, since $$F'(x) = \frac{3x^2}{3} = x^2$$.
- Antiderivatives are not unique. We can always add a constant to $$F(x)$$ and it will still be a valid antiderivative. For this reason when finding antiderivatives we always use $$+C$$.
- See Table 2 in Section 4.9 for common antiderivatives. These come from the usual differentiation rules.
- Finding the antiderivative by inspection will only work in a minoirty of cases.
- If we have information about the antiderivative, like the value for an input, we can find the exact antiderivative instead of using a general rule.

---

## Week 1 Wednesday - Area and Riemann Sums
Last time, we found antiderivatives by inspection.

> **Example.** *A particle moves along a line such that its velocity at time $$t$$ is given by $$v(t) = 2\sin t + \frac{1}{1+t^2}$$. Find its position $$s(t)$$ at time $$t$$ if $$s(0)=5$$*. We know that $$s'(t) = v(t)$$; we need to compute the antiderivative of $$v(t)$$: $$s(t) = -2\cos t + \tan^{-1} t + C$$. We have that $$s(0)$$ with $$C=0$$ is $$-2$$. For $$s(0)=5$$, $$C=7$$.

How do we find the area of a region with curved sides? We will approximate it with rectangles. To improve the approximation, we make the rectangle smaller; as we take the limit of the rectangle side length towards zero, we obtain the true area.

**Example.** Find the area $$A$$ of the region below the parabola $$y=x^2$$ between $$x=0$$ and $$x=1. Divide into rectangles and calculate by right point: $$R_5 = \frac{1}{5}\left(\frac{1}{5}\right)^{2}+\frac{1}{5}\left(\frac{2}{5}\right)^{2}+\frac{1}{5}\left(\frac{3}{5}\right)^{2}+...$$. Since $$x^2$$ is increasing, $$A < R_5$$. 

We can also obtain an underestimate by calculating rectangles by the left point: $$L_5 = \frac{1}{5}\left(\frac{0}{5}\right)^{2}+\frac{1}{5}\left(\frac{1}{5}\right)^{2}+\frac{1}{5}\left(\frac{2}{5}\right)^{2}+...$$. We can obtain a good estimate with $$\frac{L_5 + R_5}{2}$$.

We can divide the function into $$n$$ rectangles:

$$R_n = \sum_{i = 1}^n \frac{1}{n} \cdot \left(\frac{i}{n}\right)^2$$

To find the exact area, we need to let the number of rectangles go to infinity:

$$\lim_{n\to\infty} \sum_{i = 1}^n \frac{1}{n} \cdot \left(\frac{i}{n}\right)^2$$

When taking the limit, we have $$A = \frac{1}{3} = \lim_{x\to\infty} R_n = \lim_{n\to\infty} L_n$$.

**Generalizing Riemann Sums**: given a function $$f(x)$$, the area under the curve from interval $$[a, b]$$ is...

$$R_n = \lim_{n\to \infty} \sum_{i = 1}^n f(x_i) \cdot \Delta x$$

...calculated using subintervals of $$\Delta x = \frac{b-a}{n}$$ and $$x_i = a + i \cdot \Delta x$$ for $$0 \le i \le n$$ ($$x_0 = a$$, $$x_n = b$$).

Alternatively, we can use $$x_i^*$$ to indicate any sampling method, like taking the middle, left, or right height. Regardless of the method utilized, as $$n\to\infty$$ all sampling methods converge to the same true area $$A$$.

$$A = \lim_{n\to \infty} \sum_{i = 1}^n f(x_i^*) \cdot \Delta x$$

---

## Week 1 Friday - 

---
