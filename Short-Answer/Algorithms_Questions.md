# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```
#  O(n). One while loop with large number.

```
b)  sum = 0
    for i in range(n):  # O(n)
      i += 1
      for j in range(i + 1, n): # O(n)
        j += 1
        for k in range(j + 1, n): #O(n)
          k += 1
          for l in range(k + 1, 10 + k): #O(1)
            l += 1
            sum += 1
```
# O(n^3) . Four for loop.
```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1) #O(n)
```
# O(2^n) . => bunnyEars(bunnies -1) + bunnyEars(bunnies -2) Recursive looping
# O(n) => bunnyEars(bunnies-1) like a single loop backward

## Exercise II

Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.

****************************
Understanding:
n-story building = length of array
let array zero is ground floor, then ground floor to _f_ floor would contain zero broken eggs.

The plan:
Build an array of length nth story building, containing zero broken eggs to number of broken eggs.
for floor in  range (nth story building):
  if floor[n] contains broken eggs:
    return n

Complexity : O(n) - one for loop
