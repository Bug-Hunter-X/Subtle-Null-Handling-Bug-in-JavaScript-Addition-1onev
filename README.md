# Subtle Null Handling Bug in JavaScript Addition

This repository demonstrates a subtle bug in a JavaScript function that handles addition with null values.  The function correctly returns null if both inputs are null, but it fails to correctly handle cases where only one input is null. This leads to unexpected results.  The solution provides a corrected version of the function that addresses this issue.

## Bug

The original `foo` function uses strict equality (`===`) to check for null values. This is a good practice; however, the function does not properly handle the scenario where one argument is null and the other is a number, resulting in an unexpected `null` return value.  This behavior might not be immediately obvious and could lead to difficult-to-debug problems in larger applications.

## Solution

The solution introduces a simple check to handle null values gracefully. If one value is null, it is treated as 0 during the addition. This ensures that the function produces the expected results in all cases. The solution improves the robustness and reliability of the function.