# CSS calc() Inconsistency with Percentage Variables

This repository demonstrates a subtle bug related to the use of percentage values within CSS variables and the `calc()` function.  The issue lies in the unexpected behavior when subtracting a percentage variable from a percentage value within `calc()`. 

## Bug Description
The code within `bug.css` shows a situation where a CSS variable `--my-width` is set to `50%`.  When used in a `calc()` function to calculate the width of a container (subtracting `--my-width` from `100%`), the result is inconsistent across browsers and doesn't always produce the expected 50% width for the container.

## Solution
The `bugSolution.css` file offers a solution to this issue by explicitly defining the context of percentage values. This is achieved by using fixed values instead of percentages for the calculation within `calc()`, ensuring a consistent result across browsers.   This avoids unexpected results by directly specifying the subtraction amount in pixels instead of percentages, thereby resolving the inconsistency that is observed when using percentages directly within the `calc()` function's subtraction operation.