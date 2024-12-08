# Kotlin MutableMap values.removeIf() Unexpected Behavior

This repository demonstrates a subtle difference in behavior between `MutableList.removeIf()` and `MutableMap.values.removeIf()` in Kotlin.  The `values` property of a `MutableMap` returns a view, not a modifiable copy.  Therefore, using `removeIf()` on the view doesn't affect the original map.

The `bug.kt` file shows the unexpected behavior, while `bugSolution.kt` offers a corrected approach.

## How to reproduce

1. Clone this repository.
2. Open the `bug.kt` file.
3. Run the code using a Kotlin compiler.
4. Observe that the `MutableMap` is not modified as expected by `values.removeIf()`.

## Solution

Refer to `bugSolution.kt` for the corrected way to remove elements from a `MutableMap` based on a condition.