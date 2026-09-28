# Logic Gates and Qubits

## Problem 29.1

| x | y | XOR | (x + y) | (x + y) mod 2 |
| - | - | :-: | :-----: | :-----------: |
| 0 | 0 |  0  |    0    |       0       |
| 0 | 1 |  1  |    1    |       1       |
| 1 | 0 |  1  |    1    |       1       |
| 1 | 1 |  0  |    2    |       0       |

This shows that XOR is the same as equivalent (x + y) modulo 2.

## Problem 29.2

| x | y | AND | XOR | NAND | xNOR |
| - | - | :-: | :-: | :--: | :--: |
| 0 | 0 |  0  |  0  |  1   |  1   |
| 0 | 1 |  0  |  1  |  1   |  0   |
| 1 | 0 |  0  |  1  |  1   |  0   |
| 1 | 1 |  1  |  0  |  0   |  1   |

## Problem 29.3

| Shirt | Shoes | Service |
| :---: | :---: | :-----: |
|   0   |   0   |    0    |
|   0   |   1   |    0    |
|   1   |   0   |    0    |
|   1   |   1   |    1    |

<img src="image.png" width="300" />

## Problem 29.4

| x | x | AND(x, x) | OR(x, x) | XOR(x, x) |
| - | - | :-------: | :------: | :-------: |
| 0 | 0 |     0     |     0    |     0     |
| 1 | 1 |     1     |     1    |     0     |

AND(x, x) = x

OR(x, x) = x

XOR(x, x) = 0

## Problem 29.9

**Stage 1:**

XOR(0, 1) = 1

OR(1, 1) = 1

NAND(1, 0) = 1

**Stage 2:**

AND(1, 1) = 1

xNOR(1, 1) = 1

**Stage 3:**

NOR(1, 1) = 0

**Output = 0**

## Problem 29.8

| x | x | y | NOT(x) | NAND(x, x) |
| - | - | - | :----: | :--------: |
| 0 | 0 | 0 |   1    |     1      |
| 0 | 0 | 1 |   1    |     1      |
| 1 | 1 | 0 |   0    |     0      |
| 1 | 1 | 1 |   0    |     0      |

**NOT(x) = NAND(x, x)**

| x | y | AND(x, y) | A = NAND(x, y) | B = NAND(x, y) | NAND(A, B) |
| - | - | :-------: | :------------: | :------------: | :--------: |
| 0 | 0 |     0     |        1       |        1       |      0     |
| 0 | 1 |     0     |        1       |        1       |      0     |
| 1 | 0 |     0     |        1       |        1       |      0     |
| 1 | 1 |     1     |        0       |        0       |      1     |

**AND(x, y) = NAND(NAND(x, y), NAND(x, y))**
