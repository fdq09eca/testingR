# Basic Building Block

This is a note for learning R by using `swirl`

## syntax

| syntax |       meaning       |
| :----: | :-----------------: |
|  `<-`  | assignment operator |

## vector, `c()`

```r
r$> z <- c(1.1, 9, 3.14)
r$> z                                                       
[1] 1.10 9.00 3.14
r$> z*2 + 100                                               
[1] 102.20 118.00 106.28
```

- if two vectors have same length, arithmetic operation is element by element.

```r
r$> x <- c(4, 6, 8)
r$> y <- c(2, 3, 4)
r$> z <- x / y
r$> z
[1] 2 2 2
```

```r
r$> c(1, 2, 3, 4) + c(0, 10)                                
[1]  1 12  3 14
```

- If the vectors are of different lengths, R 'recycles' the shorter vector until it is the same length as the longer vector.
- It is the reason why `z * 2` has been done to every element of `z`. therefore, technically, `z * c(2, 2, 2) == z * 2`

```r
r$> c(1, 2, 3, 4) + c(0, 10, 0)                                
```

- It still applies the "recycle" rule but there will be warning[^warning].

[^warning]: It should not happen, usually.

## arithmetic operator

- `+-*/^`, `^` means power of. e.g. `2^3 = 8`
- `sqrt(x)` is square root of `x`
- `abs(x)` is the absolute value of `x`