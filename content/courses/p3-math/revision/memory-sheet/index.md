---
title: "Memory Sheet"
date: 2020-02-08T08:34:21+05:30
draft: false
---

## Algebra

### Modulus

There are 2 kinds of problems typically asked in the Modulus topic.

**Equality problems**

Where the problem involves an equality with a modulus, either on one side or both sides of the equation, simply resolve the modulus by using the \\( \pm \\) sign. For e.g., to solve,

{{< katex >}}
\begin{array}{rcl}
|2x + 1| & = & |x + 5| \\
\therefore 2x + 1 & = & \pm (x + 5) \\
\therefore 2x + 1 = x + 5 & OR & 2x + 1 = -(x + 5) \\
\end{array}
{{< /katex >}}

**Inequality problems**

Where the problem involves an inequality with a modulus, either on one side or both sides of the equation, resolve the modulus by squaring both sides and finding the critical points. For e.g., to solve,

{{< katex >}}
\begin{array}{rcl}
|2x + 1| & < & |x + 5| \\
\therefore (2x + 1)^2 & = & (x + 5)^2 \\
\end{array}
{{< /katex >}}

Solve the quadratic equation to find 2 critical points, in this case, -4 and 2. Evaluate the original inequality in between the two critical points, if it is satisfied, then the solution is \\( -4 < x < 2 \\), else the solution is \\( x < -4 \text{ and } x > 2 \\). In this case, test for e.g. for \\(x = 0\\), the inequality is satisfied, hence the solution is \\( -4 < x < 2 \\).

### Polynomial division

There are 2 kinds of facts to use in polynomial problems:

1. If suppose \\( (x - 2) \\) divides a polynomial \\( p(x) \\), then \\( p(2) = 0 \\).
2. If it is known that the reminder upon dividing the polynomial by say \\( (2x - 3) \\) is say \\(5\\), then \\( p(\frac{3}{2}) = 5 \\).

Usually the polynomial will be given with unknown coefficients, and some facts such as above, use the facts to find the unknown coefficients. Then may also need to do long division to find the other factor(s).

### Logarithms and Exponentials

Remember the basic rules for logarithms and exponentials of course:

{{< columns >}}

{{< katex >}}
\begin{array}{rcl}
\log_a xy & = & \log_a x + \log_a y \\ \\
\log_a \frac{x}{y} & = & \log_a x - \log_a y \\ \\
\log_a x^n & = & n\log_a x \\ \\
\log_a 1 & = & 0 \\
\end{array}
{{< /katex >}}

<---> 

{{< katex >}}
\begin{array}{rcl}
a^{(m + n)} & = & a^m\cdot a^n \\ \\
a^{(m - n)} & = & \displaystyle \frac{a^m}{a^n} \\ \\
(a^m)^n & = & a^{m\cdot n} \\ \\
a^0 & = & 1 \\
\end{array}
{{< /katex >}}

{{< /columns >}}

A few different kinds of problems may come up:

- If the equation to be solved has only a single exponent value, say \\( 5^x\\), then bring all the \\(5^x\\) terms to one side, all the constants to the other side, and then take logarithms to solve.
- If the equation to be solved has exponents of different kinds, like say \\( e^x\\), \\(e^{2x}\\), then it may typically need a substitution of the form \\( Y = e^x \\) to get a quadratic equation in \\( Y\\). Before that, make sure that any same exponent terms on both sides of the equation can be cancelled out. For e.g. from the equation \\( e^x + e^{2x} = e^{3x} \\), we can cancel \\( e^x \\) from both sides of the equation to get \\( 1 + e^x = e^{2x} \\).

- If the equation to be solved has \\( \log \\) or \\( \ln \\) in the equation, bring the equation to the form where \\( \log_b X = \log_b Y \\), then equate \\( X = Y \\) to solve.

Remember that in log and exponential equations \\( e\\) is just the same as any other base \\( 10 \\) or \\(5 \\) or any other number.

### Binomial Expansion

All problems need simple application of the binomial expansion formula:

{{< katex >}}
(1 + x)^n = 1 + n\cdot x + \frac{n(n - 1)}{2!} x^2 + \frac{n(n - 1)(n - 2)}{3!} x^3 + \cdots
{{< /katex >}}

The formula holds good for all values of \\( x\\) if \\(n\\) is a natural number. But if \\( n \cancel\in \N \\), then the formula holds true only if \\( |x| < 1 \\).

If the question is posed as \\( ( a + x)^n \\), then simplify it to the form \\( a^n\cdot (1 + \displaystyle \frac{x}{a})^n \\) and then use the binomial expansion.

### Partial Fractions

The key thing to remember in partial fraction expansions is that if the degree of the numerator is \\( \geq \\) than the degree of the denomiator, then first a round of division needs to be done to get the degree of the numerator \\( < \\) than the degree of the denominator. This can be done either using long division, or sometimes with a small tweak to the numerator. The latter applies in this case for e.g. 
$$ \displaystyle \frac{x^2 - 3}{x^2 - 5x} = \frac {x^2 - 5x + 5x - 3}{x^2 - 5x} = 1 + \frac {5x - 3}{x(x - 5)} $$

The rule to use for partial fraction should of course be remembered, an example is below:
$$ \displaystyle \frac{1}{x(x-5)^2(x^2 + 10)} \equiv \displaystyle \frac{A}{x} + \frac{B}{x - 5} + \frac{C}{(x - 5)^2} + \frac{Dx + E}{x^2 + 10} $$

Remember to carefully go through the calculations to find the constants \\(A\\), \\(B\\), etc. And once found, substitute back and rationalize the denominator on the RHS to check that the numerator matches the numerator in the LHS.

Partial fraction problems are usually accompanied by binomial expression problems, or with integration problems.

## Trigonometry

Trigonometry problems come in a variety of different kinds.

### Proving identities

These kinds of problems need application of basic trigonometric identities such as 

{{< columns >}}

{{< katex >}}
\begin{array}{rcl}
\tan \theta & = & \displaystyle \frac{\sin \theta}{\cos \theta} \\ \\
\sec \theta & = & \displaystyle \frac{1}{\cos \theta} \\ \\
\cosec \theta & = & \displaystyle \frac{1}{\sin \theta} \\ \\
\end{array}
{{< /katex >}}

<--->

{{< katex >}}
\begin{array}{rcl}
\cot \theta & = & \displaystyle \frac{\cos \theta}{\sin \theta} \\ \\
\sec^2 \theta & = & 1 + \tan^2 \theta \\ \\
\cosec^2 \theta & = & 1 + \cot^2 \theta \\ \\
\end{array}
{{< /katex >}}

{{< /columns >}}

They may also need application for compound angle formulae or double angle formulae. 

### Solving for theta 

Similar to the problems in exponentials, simple problems will have a simple linear equation of the form \\( \sin \theta = 0.123 \\) from which \\( \theta \\) values can be found. More involved problems may need solving a quadratic to get to a solution such as \\( \tan \theta = 1.23 \text{ OR } \tan \theta = 23.4 \\).

In each of these cases, the value of \\( \theta \\) needs to be found in the range provided in the question. The best way to do this is by drawing a rough graph of the function to identify the values that \\( \theta \\) may be allowed to take. Note also that the value of \\( \theta \\) in the problems can be found in degrees or in radians as required by simply switching over the setting in the calculator.

### Compound Angles

The compound angle formulae need to be remembered of course, but it is sufficient to remember 2-3 of them and even derive the rest if needed.

{{< columns >}}

{{< katex >}}
\begin{array}{rcl}
\sin (\alpha + \beta) & = & \sin \alpha \cdot \cos \beta + \cos \alpha \cdot \sin \beta \\ \\
\cos (\alpha + \beta) & = & \cos \alpha \cdot \cos \beta - \sin \alpha \cdot \sin \beta \\ \\
\tan (\alpha + \beta) & = & \displaystyle \frac{\tan \alpha + \tan \beta}{1 - \tan \alpha \cdot \tan \beta} \\ \\
\end{array}
{{< /katex >}}

<--->

{{< katex >}}
\begin{array}{rcl}
\sin (\alpha - \beta) & = & \sin \alpha \cdot \cos \beta - \cos \alpha \cdot \sin \beta \\ \\
\cos (\alpha - \beta) & = & \cos \alpha \cdot \cos \beta + \sin \alpha \cdot \sin \beta \\ \\
\tan (\alpha - \beta) & = & \displaystyle \frac{\tan \alpha - \tan \beta}{1 + \tan \alpha \cdot \tan \beta} \\ \\
\end{array}
{{< /katex >}}

{{< /columns >}}

### Multiple  Angles

The multiple angle formulae are simply derived from the compound angle formulae, but the formula for \\( \cos 2\theta \\) is particulary interesting and often comes handy in a number of problems.

{{< columns >}}

{{< katex >}}
\begin{array}{rcl}
\sin (2\theta) & = & 2\sin \theta \cdot \cos \theta \\ \\
\tan (2\theta) & = & \displaystyle \frac{2\tan \theta}{1 - \tan^2 \theta} \\ \\
\end{array}
{{< /katex >}}

<--->

{{< katex >}}
\begin{array}{rcl}
\cos (2\theta) & = & \cos^2 \theta - \sin^2 \theta \\
& = & 2\cos^2 \theta - 1 \\
& = & 1 - 2\sin^2 \theta \\
\end{array}
{{< /katex >}}

{{< /columns >}}

### Reverse of compound angles

In this kind of problem that comes up often in exams, we are posed with an expression of the form say \\( 2\cdot \sin \theta + 3\cdot \cos \theta \\) and the goal is to convert it to the for \\( R\cdot \sin (\theta + \alpha) \\)

{{< columns >}}

{{< katex >}}
\begin{array}{rcl}
a\sin (\theta) + b\cos (\theta) & = & R\cdot \sin (\theta + \alpha) \\ \\
a\sin (\theta) - b\cos (\theta) & = & R\cdot \sin (\theta + \alpha) \\ \\
a\cos (\theta) + b\sin (\theta) & = & R\cdot \cos (\theta - \alpha) \\ \\
a\cos (\theta) - b\sin (\theta) & = & R\cdot \cos (\theta + \alpha) \\ \\
\end{array}
{{< /katex >}}

<--->

{{< katex >}}
\begin{array}{rcl}
R & = & \sqrt{a^2 + b^2} \\ \\
\cos \alpha & = & \displaystyle \frac{a}{R} \\ \\
\sin \alpha & = & \displaystyle \frac{b}{R}
\end{array}
{{< /katex >}}

{{< /columns >}}

### Circular Measure

{{< columns >}}
For an arc of radius \\( r\\) and \\( \theta \\) in radians,  
the length of the arc \\( = r\cdot \theta \\)  
and the area of the sector \\( = \displaystyle \frac{r^2\cdot \theta}{2} \\)
<--->
And for the entire circle, \\( \theta = 2\cdot \pi \\), hence  
circumference of the circle \\( = 2\cdot \pi \cdot r\\)  
area of the circle \\( = \pi \cdot r^2 \\)
{{< /columns >}}

## Differentiation

### Step by Step approach

Given an involved function of x, in order to find the derivative of the function, the following step by step approach can be followed:

{{< table "normal-table" >}}
| 1. | First, check if sum / difference rule can be applied. | If \\( y = u \pm v\\), <br/>then, \\( \displaystyle \frac{dy}{dx} = \displaystyle \frac{du}{dx} \pm \frac{dv}{dx} \\) |
| :-- | :-- | :-- |
| 2. | Next, check if product / quotient rule can be applied. | If \\( y = u \cdot v\\), <br/>then, \\( \displaystyle \frac{dy}{dx} = \displaystyle u\cdot \frac{dv}{dx} + v\cdot \frac{du}{dx} \\)<br/><br/>If \\( y = \displaystyle \frac{u}{v}\\), <br/>then, \\( \displaystyle \frac{dy}{dx} = \displaystyle \frac{v\cdot \displaystyle \frac{du}{dx} - u\cdot \frac{dv}{dx}}{v^2} \\) |
| 3. | Next, check if chain rule can be applied. | \\( \displaystyle \frac{dy}{dx} = \displaystyle \frac{dy}{du} \cdot \frac{du}{dx} \\)<br/><br/> |
| 4. | Finally, you should have a function whose derivative is well known. | \\( \displaystyle \frac{d}{dx} (kx^n) = knx^{n-1} \\)<br/><br/> \\( \displaystyle \frac{d}{dx} (\ln x) = \frac{1}{x} \\)<br/><br/> \\( \displaystyle \frac{d}{dx} (e^{kx}) = ke^{kx} \\)<br/><br/> \\( \displaystyle \frac{d}{dx} (\sin kx) = k\cdot \cos kx \\)<br/><br/> \\( \displaystyle \frac{d}{dx} (k\cdot \tan x) = k\cdot \sec^2 kx \\)<br/><br/> |
{{< /table >}}

### Parametric differentiation

When \\(y\\) is not given as a function of \\(x\\), but as a function of a different variable such as \\(t\\) and \\(x\\) is also a function of \\(t\\), then to find the derivative of \\(y\\) wrt \\(x\\):
$$ \displaystyle \frac{dy}{dx} = \displaystyle \frac{dy}{dt} / \frac{dx}{dt} $$

### Implicit differentiation

When \\(y\\) is not given as an explicit function of \\(x\\), but \\( y\\) and \\( x\\) are related together by an equation where it is not simply to rewrite it in the form \\( y = f(x) \\), then to find the derivative of \\(y\\) wrt \\(x\\), simply differentiate the equation, then get all the \\( \displaystyle \frac{dy}{dx} \\) terms together to the LHS.

Note while differentiating,
{{< katex >}}
\begin{array}{rcl}
\displaystyle \frac{d}{dx} (x^3) & = & 3\cdot x^2 \\ \\
\text{And } \displaystyle \frac{d}{dy} (y^3) & = & 3\cdot y^2 \\ \\
\text{BUT crucially } \displaystyle \frac{d}{dx} (y^3) & = & 3\cdot y^2\cdot \displaystyle \frac{dy}{dx} \\ \\
\end{array}
{{< /katex >}}

## Integration 

### Integration by Substitution

Watch out for any part of the integral where substituting that part as \\(u\\) would help simplify the rest of the integral, esp the \\( dx\\) part of the integral. An obvious example is below:

To integrate \\( \displaystyle \int x\cdot \cos x^2 dx \\), simply substitute \\( u = x^2 \\), and that helps simplify the integral cosce \\( du = x\cdot dx \\), and the integral can be solved ucosg \\( \displaystyle \frac{1}{2} \int \cos u \, du \\).

### Integration by Partial Fraction

Check if the integral can be simplified using partial fractions, so that sum rule can be easily applied and each separate part of the integral can be easily calculated. An example is below:

To integrate \\( \displaystyle \int \frac{1}{x\cdot (x - 5)} dx \\), first simplify the integral using partial fractions and then integrate each part separately.

{{< katex >}}
\begin{array}{rcl}
\displaystyle \int \frac{1}{x\cdot (x - 5)} dx & = & \displaystyle \frac{1}{-5}\int (\frac{1}{x} - \frac{1}{x-5}) dx \\ \\
& = & \displaystyle \frac{1}{-5}\int \frac{1}{x} dx - \frac{1}{-5}\int \frac{1}{x - 5} dx \\ \\
& = & \displaystyle \frac{1}{-5}\ln|x|- \frac{1}{-5}\ln |x - 5| + c\\ \\
& = & \displaystyle \frac{1}{5}\ln |\frac{x - 5}{x}| + c \\ \\
\end{array}
{{< /katex >}}

### Integration by Parts

If the integral cannot be soolved using substitution, or by partial fractions, and it is not a well known integral to start with, then the option left is to use integration by parts.

1. The first step is to choose \\(f\\) and \\(g\\) carefully using ILATE rule. Whichever comes first becomes \\(f\\) and the other becomes \\(g\\).  
2. Next find \\( \displaystyle \int g dx \\)  
3. Then find \\( \displaystyle \frac{df}{dx} \\)  
4. Finally, find \\( \displaystyle \int \frac{df}{dx}\cdot (\int g dx ) dx \\)

And apply the overall formula for integration by parts:
$$ \displaystyle \int (f\cdot g)\, dx = f\cdot \displaystyle \int g\, dx - \displaystyle \int \frac{df}{dx}\cdot (\int g\, dx )\, dx $$

### Known Integrals

\\( \displaystyle \int{kx^n}{dx}  = \frac{kx^{n+1}}{n+1} + c \\)<br/><br/> 
\\( \displaystyle \int{e^{ax+b}}{dx}  = \frac{1}{a} e^{ax+b} + c \\)<br/><br/> 
\\( \displaystyle \int{\frac{1}{ax+b}}{dx} = \frac{1}{a} \ln |ax + b| + c \\)<br/><br/> 
\\( \displaystyle \int{\cos (ax+ b)}{dx} = \frac{1}{a} \sin (ax + b) + c\\)<br/><br/> 
\\( \displaystyle \int{\sin (ax+ b)}{dx} = \frac{-1}{a} \cos (ax + b) + c\\)<br/><br/> 
\\( \displaystyle \int{\sec^2 (ax+ b)}{dx} = \frac{1}{a} \tan (ax + b) + c\\)<br/><br/> 

### Differential Equations

Solving differential equations where the variables are separable is very simple, just get all the variables in say \\( y\\) to one side, including \\(dy\\) in the numerator together with all other functions in \\(y\\), and similarly get all the variables in \\(x\\) to the other side. Then simply integrate both sides, using any of the methods above.

Substitute boundary conditions given to find the values of any constants. 

## Numerical Techniques

### Numerical Integration

The question would usually mention a number of intervals to consider. Suppose three intervals, then divide the limits of the integral into three parts, and find the value of the function at the start \\( y_0\\), in the middle \\( y_1\\) and \\(y_2\\) and at the end \\(y_3\\). Then use the formula:

Area = \\(\frac{1}{2}\\) x strip width x [ends + twice middles ]

### Numerical Solution

First rewrite the equation \\(f(x) = 0\\) in the form \\(x = F(x) \\).

The use the iteration \\( x_{n+1} = F( x_n) \\). This converges to the root a provided \\( -1 < F(a) < 1 \\).

1. So, choose \\(x_0\\) near \\(a\\), substitute into \\( F(x) \\) to find \\( x_1\\).  
1. Next, substitute \\(x_1\\) into \\( F(x) \\) to find \\( x_2\\).   
2. Stop when the value of \\(x\\) from two successive interations are very close to each other, or have achieved the desired number of significant digits of accuracy intended.

