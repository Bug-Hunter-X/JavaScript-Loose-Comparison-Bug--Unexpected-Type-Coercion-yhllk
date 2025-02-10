# JavaScript Loose Comparison Bug

This repository demonstrates a subtle bug in JavaScript related to loose comparison (==) and type coercion. The code appears to function correctly for the given test cases, but it fails when considering edge cases or different data types.

## Bug Description

The `foo` function intends to categorize numbers based on whether they are null, negative, or positive.  However, due to JavaScript's loose comparison, it handles inputs in an unexpected manner. The problem surfaces when unexpected values are passed.  For instance, using loose comparison, a value of 0 will be incorrectly categorized as positive.

## Bug Solution

The solution involves replacing the loose comparison (==) with strict comparison (!==).  Strict comparison does not allow type coercion, thus ensuring that only truly null values are handled correctly.

## How to Reproduce

1. Clone this repository.
2. Open `bug.js` and examine the initial code.
3. Run the JavaScript code. Note the unexpected output for the value 0.
4. View `bugSolution.js` to see the fix. Re-run the code to observe the corrected behavior.