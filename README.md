# CSS Media Query `calc()` Percentage Issue

This repository demonstrates an uncommon error in CSS involving the usage of the `calc()` function with percentages within media queries.  The issue stems from attempting to calculate a value (100% - 100px) before the browser has the final viewport width.  The provided `bug.css` file showcases the erroneous implementation, while `bugSolution.css` presents a corrected approach.

## Problem Description

When using `calc(100% - 100px)` inside a media query's `max-width` condition, the browser might not accurately calculate the value, resulting in inconsistent or incorrect application of styles.  This is because `100%` refers to the viewport width, which is not yet fully determined at the point the media query is evaluated.

## Solution

To solve this, consider using viewport units like `vw` or a more straightforward approach without `calc()` if possible.  The `bugSolution.css` file presents a revised CSS code that addresses the issue.