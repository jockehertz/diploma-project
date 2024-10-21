# Calculus

**MAT03c: Mathematics 3c**

*Joakim Hertzberg*

# The Infinituple and Infinitesimal

An *infinituple* ($\infty$) is a number which is so big that it can not be represented numerically.

An *infinitesimal* is the opposite - a number which is infinitely small, but **not 0**. It can be represented in two ways:

$$
\frac{1}{\infty}
$$

$$
0.00 \cdots 1
$$

# The Derivative

## Definition

A derivative is the **instantaneous rate of change** of a function. It may be denoted as:

$$
\dot{y} = f'(x) 
$$

**OR**

$$
\dot{y} = \frac{dy}{dx}f(x)
$$

### The first equation

The rate of change which defines the derivative can is that between one point $(x)$, and one point which is only infinitesimally bigger than that, such that:

$$
\begin{cases} x+h \\ h= \frac{1}{\infty} \end{cases}
$$

The **first equation for the definition of the derivative** can then be found as follows:

$$
\frac{dy}{dx}f(x)=\lim_{h \rightarrow 0}\left(\frac{f(x+h)-f(x)}{h}\right)
$$

### The Second Equation

Another approach is to define two points, and have one approach the other.

$$
\frac{dy}{dx}f(x)=\lim_{a\rightarrow x} \left( \frac{f(a)-f(x)}{a-x}\right)
$$

Note that both these equations are constructed such that the numerator gives $\Delta y$, and the denominator gives $\Delta x$. However, when dealing with infinitesimals, the $\Delta$ is replaced by a $d$. This is why we denote a derivative with $\frac{dy}{dx}$.

## Differentiation

Differentiation is derivation, but with respect to only one variable. For most use cases it's the same, but it's denoted as follows:

$$
\frac{d}{dx}f(x)
$$

Above is the function $f(x)$ differentiated **with respect to $x$.**

*"With respect to" can be abbreviated to "WRT"*

## Derivation Rules

It is *possible* to derive with the definitions of derivatives, it is however cumbersome and requires a lot of algebracrobatics. Patterns have been found in the ways that different functions turn out when dervied, and hence we have derived

### The Power Rule

The power rule applies for - as the name states - **power functions**.

**<u>Definition</u>**

$$
\begin{cases}f(x) = kx^n \\\frac{d}{dx}f(x) = knx^{n-1} \end{cases}
$$

**<u>Example</u>**

Differentiate $f(x)$ with respect to $x$.

$f(x) = 3x^2$

$$
\because \frac{d}{dx} kx^n = knx^{n-1} \\ \frac{d}{dx}3x^2 = 3 \times 2 x^{2-1} = 6x
$$

### The exponential derivative

The exponential derivative is defined for **exponential functions**, and is defined such that:

$$
\frac{d}{dx} ka^{nx} = nka^{nx} \ ln(a)
$$

**NOTE:**

In polynomials where $a=e$, the expression $ln(a)$ is not present, as $ln(e) = 1$ by definition.

**<u>Example</u>**

Differentiate $f(x)$ WRT $x$.

$f(x) = 3(2^x)$ 

$$
\because \frac{d}{dx}ka^{nx} = kna^{nx} \ \ln{a} \\ \frac{d}{dx} 3(2^x) = 3(2^x) \ \ln{2}
$$

**LOOK OUT**

If the power is negative, the expression switches sign each time it is differentiated, since the power gets multiplied with the entire expression.

### The Logarithmic Derivative

The logarithmic derivative is srelated to the exponential derivative:

$$
\frac{d}{dx}\log_{a}x = \frac{1}{x \ln{a}}
$$

**<u>Example</u>**

Find $\frac{d}{dx} \log_2{x}$.

$$
\because \frac{d}{dx} \log_a{x} = \frac{1}{x \ln{a}}
$$

$$
\frac{d}{dx}\log_2{x}=\frac{1}{x \ln{2} }
$$

# The Integral

The integral has not quite the same intuitive definition as the derivative, but it can sometimes be represented as the area under a graph.

## Primitive Functions

A primitive function is a function which has the function in question as a derivative. That is - it's an *antiderivative*. A primitive function is denoted with a capital letter, as such for $f(x)$:

$$
F(x)
$$

A primitive function is then defined such that:

$$
\frac{d}{dx}F(x) = f(x)
$$

### The Constant of Integration

Ponder what happens to a constant as a function is differentiated - it dissappears! This mechanism means that a primitive function has some undefined constant, which was lost in derivation to the origin function. Said constant is represented with $C$.

**<u>Proof</u>**

Consider a function $F(x)$ which contains only one constant polynomial, it may then be represented as a component function, $\psi(x)$, plus that constant $C$.

$$
F(x)=\psi(x)+C
$$

$$
\because a^0=1, C = Cx^0 \\
F(x)=\psi(x)+Cx^0 \\
f(x) = \psi'(x) + \frac{d}{dx}(Cx^0) \\
f(x) = \psi'(x) + 0(Cx^{-1}) \\
f(x) = \psi'(x) + 0 \\
\therefore C=0  \quad \square
$$

## Definite Integrals

A definite integral is the area between two bounds of a function, it is found using following equation:

$$
A = \int_a^b f(x) = F(b) - F(a)
$$

When calculating definite integrals, $C$ may be ignored, as it cancels out.

**<u>Proof</u>**

$$
\begin{cases}
\int_a^bf(x)=F(b)-F(a) \\
F(x)=\psi(x)+C
\end{cases} \\

$$

$$
F(b)-F(a) = (\psi(b) + C) - (\psi(a)+C) \\
\int_a^b f(x) = \psi(b) + \cancel{C} - \psi(a) - \cancel{C} \\
\int_a^b f(x) = \psi(b) - \psi(a) \quad \square
$$



