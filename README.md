# Missing Number

**LeetCode Problem:** 268
**Language:** Python

## Problem

Given an array `nums` containing `n` distinct numbers from the range:

```text
0 to n
```

one number is missing from the array.

The task is to find and return the missing number.

## Example

Input:

```text id="1t9q5c"
nums = [3, 0, 1]
```

The complete range should be:

```text id="x8m2ka"
0, 1, 2, 3
```

The number `2` is missing.

Output:

```text id="c6r4yb"
2
```

Another example:

```text id="v0n7hs"
nums = [0, 1]
```

The complete range is:

```text id="q5k2we"
0, 1, 2
```

So the missing number is:

```text id="3j8p1d"
2
```

## Approach

This solution uses the **XOR** operation.

The important XOR properties are:

```text id="s3f7qm"
a ^ a = 0
a ^ 0 = a
```

We start with `n` because the range goes from `0` to `n`.

Then we XOR:

* Every index
* Every value in the array
* The value `n`

All numbers that appear in both groups cancel each other.

The only number left is the missing number.

## Example

Suppose:

```text id="x5m8pa"
nums = [3, 0, 1]
```

The numbers from `0` to `3` are:

```text id="h2v9kd"
0, 1, 2, 3
```

The array contains:

```text id="n4c6rx"
3, 0, 1
```

After applying XOR, the duplicate values cancel:

```text id="w7q1mz"
0 ^ 1 ^ 2 ^ 3
^
3 ^ 0 ^ 1
```

Only `2` remains.

## Complexity

* **Time:** O(n)
* **Space:** O(1)

The array is traversed only once, and no additional data structure is required.

## Key Learning

This problem helped me practice:

* XOR operation
* Bit manipulation
* Array traversal
* Finding missing values
* Using mathematical properties for optimization

## Conclusion

The solution uses XOR to find the missing number without sorting the array or using extra space. Since duplicate values cancel each other, the only remaining value is the missing number.

**Author: T. Nandhini**
