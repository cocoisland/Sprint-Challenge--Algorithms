Add your answers to the Algorithms exercises here.

a: O(n). One while loop with large number n^3.

b: O(n^4) . Four for loop.

c: O(2^n) . Recursive looping

Exercise II:
Understanding:
n-story building = length of array
let array zero is ground floor, then ground floor to _f_ floor would contain zero broken eggs.

The plan:
Build an array of length nth story building, containing zero broken eggs to number of broken eggs.
for floor in  range (nth story building):
  if floor[n] contains broken eggs:
    return n

Complexity : O(n) - one for loop