# Unexpected Behavior of calc() within translate3d() in CSS

This repository demonstrates an uncommon issue encountered when using the `calc()` function within the `transform: translate3d()` property in CSS. The problem arises due to the way `calc()` is interpreted and processed in conjunction with `translate3d()`.

## Bug Description
The `calc()` function, when directly embedded within `translate3d()`, might not be parsed correctly, resulting in unexpected transformations or no transformation at all. This is not a typical CSS issue and might easily be overlooked during development.

## Bug Reproduction
The file `bug.css` contains a simple CSS rule that demonstrates this issue.  Observe the unexpected result of applying the transform. 

## Solution
The `bugSolution.css` file demonstrates the solution to this problem. To solve this,  use intermediate variables to create a separate calculation step. Then, use the calculated variable as the argument for the translate3d() function.