# Fibonacci Numbers
> Neil Atreya

## PROBLEM 1.1.

0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610, 987, 1597

Therefore, the answer is $\boxed{1597}$

## PROBLEM 1.3.

Looking at the fibonacci numbers:

0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, ...

The even numbers are:

$F_0=0, F_3=2, F_6=8, F_9=34, F_{12}=144, ...$

Therefore, by observation: 

That is why $\boxed{F_{n+3}}$ is the function to get the next even number, if $F_n$ is an even number.


Why this happens is because:  
\- every even + odd number equals an odd number  
\- every even + even number is another even number  
\- every odd + odd number is another even number  

When you're going in order for this:  
1\. 0 + 1: even + odd = odd.  
2\. 1 + 1: odd + odd = even.  
3\. 1 + 2: odd + even = odd.  

That's why every third number of n is the function to get the next even number

## PROBLEM 1.4.

Looking at the fibonacci numbers:

0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, ...

The multiples of 3 are:

$F_4=3, F_8=21, F_{12}=144, ...$

Therefore, by observation: 

If $F_n$ is a multiple of 3, then $F_{n+4}$ is the function to get the next multiple of 3.

Why?:

$F_{n+4} = F_{n+3} + F_{n+2}$

$F_{n+3} = F_{n+2} + F_{n+1}$

$F_{n+2} = F_{n+1} + F_n$

$F_{n+4} = F_{n+2} + F_{n+1} + F_{n+1} + F_n$

$F_{n+4} = F_{n+1} + F_n + F_{n+1} + F_{n+1} + F_n$

$F_{n+4} = 3(F_{n+1}) + 2(F_n)$

$F_n = 3k$, since $F_n$ is a multiple of 3.

$F_{n+4} = 3(F_{n+1}) + 6k$

$F_{n+4} = 3(F_{n+1} + 2k)$

This shows $F_{n+4}$ is a multiple of 3.

That is why $\boxed{F_{n+4}}$ is the function to get the next multiple of 3, if $F_n$ is a multiple of 3.



## PROBLEM 1.5.

```
fib_prev = 0
fib_curr = 1

print(fib_prev)
print(fib_curr)

for i in range (2, 100):
    fib_next = fib_prev + fib_curr
    print (fib_next)
    fib_prev = fib_curr
    fib_curr = fib_next
```
This code prints the first 100 Fibonacci numbers.  In problems 1.3 and 1.4, the rule is that $F_{n + 3}$ is the function for every next even number. And $F_{n + 4}$ is the function for every next multiple of 3. 

TODO

That means that for every number m, there is always going to be an infinite umber of multiples  of m's in the Fibonacci sequence.

## PROBLEM 1.9.

Compute fibonacci ratios:

$$
\frac{F_{n+1}}{F_n}
$$ 

For $1 \le n \le 10$:

$$
1, 2, \frac{3}{2}, \frac{5}{3}, \frac{8}{5}, \frac{13}{8}, \frac{21}{13}, \frac{34}{21}, \frac{55}{34}, \frac{89}{55}
$$

Approximately:
$$
1, 2, 1.5, 1.667, 1.6, 1.625, 1.615, 1.619, 1.618, 1.618
$$

So yes, they seem to approach the **golden ratio** $\boxed{1.618...}$

---

Compute Lucas ratios:

$$
\frac{L_{n+1}}{L_n}
$$ 

For $1 \le n \le 10$:

$$
\frac{3}{1}, \frac{4}{3}, \frac{7}{4}, \frac{11}{7}, \frac{18}{11}, \frac{29}{18}, \frac{47}{29}, \frac{76}{47}, \frac{123}{76}, \frac{199}{123}
$$

Approximately:
$$
3, 1.333, 1.75, 1.571, 1.636, 1.611, 1.621, 1.617, 1.618, 1.618
$$

So yes, they seem to approach the **golden ratio** $\boxed{1.618...}$



## PROBLEM 1.10.

To solve $G_n = F_1 + F_2 + F_3 +···+ F_n$ You first have to start with 

$$
F_1 = \cancel{F_3} - F_2
\\
F_2 = \cancel{F_4} - \cancel{F_3} 
\\
F_3 = \cancel{F_5} - \cancel{F_4}
\\
...
\\
F_{n-1} = \cancel{F_{n+1}} - \cancel{F_n} 
\\
F_n = F_{n+2} - \cancel{F_{n+1}}
$$

Everything except two terms cancel out!

$$
G_n= F_{n+2}-F_2
\\
G_n= F_{n+2}-1
$$   

Thus $\boxed{G_n= F_{n+2}-1}$ is the answer.

---

To solve $M_n = L_1 + L_2 + L_3 +···+ L_n$ You first have to start with 

$$
L_1 = \cancel{L_3} - L_2
\\
L_2 = \cancel{L_4} - \cancel{L_3} 
\\
L_3 = \cancel{L_5} - \cancel{L_4}
\\
...
\\
L_{n-1} = \cancel{L_{n+1}} - \cancel{L_n} 
\\
L_n = L_{n+2} - \cancel{L_{n+1}}
$$

Everything except two terms cancel out!

$$
M_n= L_{n+2}-L_2
\\
M_n= L_{n+2}-3
$$
 
Thus, $\boxed{M_n= L_{n+2}-3}$ is the answer.

## PROBLEM 1.11.

To solve $H_n = F_1 + F_3 + F_5 +···+ F_{2n-3} + F_{2n-1}$ You first have to start with 

$$
F_1 = \cancel{F_2} - F_0
\\
F_3 = \cancel{F_4} - \cancel{F_2} 
\\
F_5 = \cancel{F_6} - \cancel{F_4}
\\
...
\\
F_{2n-3} = \cancel{F_{2n-2}} - \cancel{F_{2n-4}} 
\\
F_{2n-1} = F_{2n} - \cancel{F_{2n-2}}
$$

Everything except two terms cancel out!

$$
H_n= F_{2n}-F_0
\\
H_n= F_{2n}-0 = F_{2n}
$$   

Thus, $\boxed{H_n= F_{2n}}$ is the answer.

## PROBLEM 1.12.

Computing by example:

$n=1: 1^2 = 1$

$n=2: 1^2 + 1^2 = 2$

$n=3: 1^2 + 1^2 + 2^2 = 6$

$n=4: 1^2 + 1^2 + 2^2 + 3^2 = 15$

$n=5: 1^2 + 1^2 + 2^2 + 3^2 + 5^2 = 40$

So the sums are, 1, 2, 6, 15, 40, ...

By observation and trial, products of two successive Fibonacci numbers are:

$F_1F_2 = 1 \cdot 1 = 1$

$F_2F_3 = 1 \cdot 2 = 2$

$F_3F_4 = 2 \cdot 3 = 6$

$F_4F_5 = 3 \cdot 5 = 15$

$F_5F_5 = 5 \cdot 8 = 40$

Based on this pattern:

$\boxed{F_1^2 + F_2^2 + ... + F_n^2 = F_nF_{n+1}}$

## PROBLEM 1.13.

Computing by example:

$n=2: F_1F_3 - F_2^2 = (1)(2)-1^2 = 1$

$n=3: F_2F_4 - F_3^2 = (1)(3)-2^2 = -1$

$n=4: F_3F_5 - F_4^2 = (2)(5)-3^2 = 1$

$n=5: F_4F_6 - F_5^2 = (3)(8)-5^2 = -1$

So it altenates: 1, -1, 1, -1, ...

Based on this pattern:

$\boxed{F_{n-1}F_{n+1} - F_n^2 = (-1)^n}$

