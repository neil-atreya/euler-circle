# Fibonacci Numbers

## PROBLEM 1.1.

0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610, 987, 1597

> Therefore, the answer is **1597** 

## PROBLEM 1.2.

TODO

## PROBLEM 1.3.

If $F_n$ is even, then $F_{n + 3}$ is the function to get the next even number.

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

If $F_n$ is a multiple of 3, then $F_{n+4}$ is the function to get the next multiple of 3.

Why?:

$F_{n+4} = F_{n+3} + F_{n+2}$

$F_{n+3} = F_{n+2} + F_{n+1}$

$F_{n+2} = F_{n+1} + F_n$

$F_{n+4} = F_{n+2} + F_{n+1} + F_{n+1} + F_n$

$F_{n+4} = F_{n+1} + F_n + F_{n+1} + F_{n+1} + F_n$

$F_{n+4} = 3(F_{n+1}) + 2(F_n)$

$F_n = 3k$

$F_{n+4} = 3(F_{n+1}) + 6k$

$F_{n+4} = 3(F_{n+1} + 2k)$

That is why $F_{n+4}$ is the function to get the next multiple of 3.







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

