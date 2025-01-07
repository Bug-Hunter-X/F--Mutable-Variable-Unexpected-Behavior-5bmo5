# F# Mutable Variable Unexpected Behavior

This example demonstrates a common pitfall in F# when dealing with mutable variables.  The `add` function calculates the sum of `x` and `y` only once; changes to `x` and `y` afterward do not affect the value of `z`.

## Bug

The `bug.fs` file contains code that showcases this unexpected behavior.  The initial values of `x` and `y` are used to calculate `z`, but subsequent modifications to `x` and `y` do not update `z`.

## Solution

The `bugSolution.fs` file presents a corrected approach.  Instead of assigning the result of `add` directly to `z`, it recalculates `z` whenever `x` or `y` changes.  This ensures `z` reflects the latest values of `x` and `y`.