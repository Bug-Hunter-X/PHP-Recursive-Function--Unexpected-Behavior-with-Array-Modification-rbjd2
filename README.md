# PHP Recursive Function Bug

This repository demonstrates a subtle bug in PHP related to how recursive functions handle array modifications.  The provided code shows a recursive function `processData` intended to process nested arrays. However, the function does not correctly modify the original array; only a copy is changed.

## Bug Description

The recursive function `processData` processes nested arrays, making changes within.  However, due to the way PHP handles array passing by reference, the original array remains unmodified.  This is counter-intuitive and can lead to bugs when you expect the original array to be changed.

## Solution

The solution involves using a technique to modify the original array by reference. This can be done by passing the array element using `&` as demonstrated in the `bugSolution.php` file.

## How to Reproduce

1. Clone this repository.
2. Run `bug.php`. Observe the output. The original array is not modified.
3. Run `bugSolution.php`. Observe the output. The original array is correctly modified.
