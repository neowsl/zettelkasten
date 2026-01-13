---
tags: math_207
---

## 2026-01-12

> An **equilibrium solution** to a DE is a constant function $y(x) = c$ that satisfies the DE. To find equilibrium solutions, solve for $f(x, y) = 0$.

> A first-order DE is called **separable** if it can be written as
> $$ (d y) / (d x) = f(x) g(y). $$

### Solving separable DE by separation of variables

1. Identify the DE in separable form

$$ (d y) / (d x) = f(x) g(y) $$

2. Separate the variables

$$ 1 / g(y) = f(x) d x $$

3. Integrate both sides

$$ integral 1 / g(y) d y = integral f(x) d x $$

Let $G(y)$ be the left-hand antiderivative, and $F(x)$ be the right-hand antiderivative:

$$ G(x) = F(x) + C $$

4. Substitute the initial condition $y(x_0) = y_0$ to solve for $C$
5. Write the solution explicitly (if possible)