# Unexpected Null Return with Undefined Function Parameters

This repository demonstrates a common JavaScript error related to the loose comparison of null and undefined values when handling optional function parameters.  The `foo` function attempts to gracefully handle null values, but it fails to distinguish between null and undefined inputs.  The solution provides a more robust approach.

## Bug

The provided JavaScript code shows an example where the function `foo` returns null if either `a` or `b` is null. This behavior is intended but does not adequately account for the case where `a` or `b` is undefined. This leads to incorrect results in situations where a parameter is not passed.

## Solution

The corrected code uses strict equality (`===`) to explicitly check for both null and undefined, ensuring that the function behaves as expected in all cases.