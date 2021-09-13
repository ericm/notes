# Lecture 1
## Intro
- Labs week 2 onwards: Tuesday 3-4 WGB 21
- Required Book: Programming Haskell

## Functions
### Numeric
```hs
add_one :: Integer -> Integer
add_one x = x+1
add_one` x = (+) x 1 -- prefix
add_one`` x = (\x -> x+1) x
add_one``` = \x -> x + 1
```
- Params on left side of `=`.
### List
```hs
empty :: [Integer]
empty = []
add_to_front :: Integer -> [Integer] -> [Integer]
add_to_front i is = i :is
```
### Pattern Matching
```hs
is_empty :: [Integer] -> Bool
is_empty [] = True
is_empty ((:)i is) = False -- Pattern that matches non empty list.
__is_empty (i:is) = False
__is_empty _ = False -- least precedence wildcard.
get_head :: [Integer] -> Integer
get_head (i:_) = i -- Gets head of list.
```
### Integer precision 
```hs
n_ones :: Int -> [Int]
n_ones 0 = [] -- If n == 0, base case.
n_ones n = 1:n_ones (n-1) -- Recursion.
n_ones` n = replicate n 1 -- Standard lib function.

infi_ones :: [Integer]
ones = 1:ones
```