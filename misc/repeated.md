# Question

Uniformly draw a random real number $r$ between $0$ and $N$.
Repeat, drawing a number between $0$ and $r$.
You lose the game when you draw a number below 1.
On average, how many turns do you last in the game?

https://jasmcole.com/2016/10/01/a-probability-puzzle/

# Answer

Set up a recursive function.

$$f(x) = 1/x + 1/x \int_1^x (f(y) + 1) dy$$

Notice $f(x) = 1$ where $x < 1$.

Isolate the integral.

$$\int_1^x (f(y) + 1) dy = x(f(x) - 1/x)$$

Differentiate both sides.

$$d/dx \int_1^x (f(y) + 1) dy = d/dx (x(f(x) - 1/x))$$

$$\int_1^x f'(y) dy + d/dx(x-1) = (f(x) - 1/x) + x(f'(x) + 1/x^2)$$

$$f(x) + 1 = (f(x) - 1/x) + x(f'(x) + 1/x^2)$$

Simplifying terms.

$$1 = - 1/x + x(f'(x) + 1/x^2)$$

$$1 = xf'(x)$$

$$1/x = xf'(x)$$

Therefore 

$$f(x) = c + ln(x)$$

$$f(1) = 1 => c = 1$$

So

$$f(x) = ln(x) + 1$$
