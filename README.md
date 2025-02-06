# F# Mutable Variable Swap Bug

This repository demonstrates a common error in F# when working with mutable variables and function parameters.  The `swap` function attempts to exchange the values of two mutable variables, but due to pass-by-reference semantics, the original values remain unchanged within the caller's scope.  The solution illustrates how to use tuples for correct value swapping.

## How to reproduce the bug

1. Clone the repository.
2. Open `bug.fs` and run the code.
3. Observe that the output is not as expected; values are not swapped correctly.

## Solution

The solution is presented in `bugSolution.fs` and involves using a tuple to return the swapped values, avoiding the pass-by-reference issue.