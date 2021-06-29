# Sequence and Numbers

## `:` operator

see `` ?`:` `` for official documentation.

```r
r$> 1:20                                                         
 [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20
r$> 15:1                                                         
 [1] 15 14 13 12 11 10  9  8  7  6  5  4  3  2  1
```

```r
r$> pi:10                                                        
[1] 3.141593 4.141593 5.141593 6.141593 7.141593 8.141593
[7] 9.141593
```

- if it starts and ends with the same type of number.
  - i.e. `pi:10` ends with `9.141593` but `10:pi`ends with `3` 
- 10 is not included because 9.141593 + 1 > 10

## `seq()`

```r
# default increment, i.e by = 1
r$> seq(1, 20)                                                   
 [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20

# custom increment
r$> seq(0, 10, by = 0.5)                                         
 [1]  0.0  0.5  1.0  1.5  2.0  2.5  3.0  3.5  4.0  4.5  5.0  5.5
[13]  6.0  6.5  7.0  7.5  8.0  8.5  9.0  9.5 10.0

# automatic increment
r$> seq(5, 10, length = 30)                                      
 [1]  5.000000  5.172414  5.344828  5.517241  5.689655  5.862069
 [7]  6.034483  6.206897  6.379310  6.551724  6.724138  6.896552
[13]  7.068966  7.241379  7.413793  7.586207  7.758621  7.931034
[19]  8.103448  8.275862  8.448276  8.620690  8.793103  8.965517
[25]  9.137931  9.310345  9.482759  9.655172  9.827586 10.000000
```

- `1:20 == seq(1, 20, by = 1)` 

```r
r$> my_seq <- seq(5, 10, length =30)                              
r$> length(my_seq)                                               
[1] 30
```

- `my_seq` is a vector with `length` 30.

```r
# generate a vector with the same length with another (N) from 1 to N
r$> length(my_seq)                                               
[1] 30
r$> 1:length(my_seq)                                             
 [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20
[21] 21 22 23 24 25 26 27 28 29 30
r$> seq(along.with = my_seq)                                     
 [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20
[21] 21 22 23 24 25 26 27 28 29 30
r$> seq_along(my_seq)                                            
 [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20
[21] 21 22 23 24 25 26 27 28 29 30
```
- `seq(along.with = my_seq) == seq_along(my_seq) == 1: length(my_seq) == 1:30`

## `rep()`

```r
# creating a vector that contains 40
r$> rep(0, times = 40)                                           
 [1] 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
[31] 0 0 0 0 0 0 0 0 0 0
r$> rep(c(0, 1, 2), times = 10)                                  
 [1] 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2
r$> rep(c(0, 1, 2), each = 10)                                   
 [1] 0 0 0 0 0 0 0 0 0 0 1 1 1 1 1 1 1 1 1 1 2 2 2 2 2 2 2 2 2 2
```