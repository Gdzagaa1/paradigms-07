For detailed problem description and implementation details, see the assignment PDF.

# Where Am I?

A Scheme program that determines your location in 2D space using distance measurements to known stars.

## Problem

Given:
- A map of star locations
- Distance measurements to several stars (without knowing which star is which)

Find your location by analyzing circle intersections where each circle represents possible positions at a measured distance from a star.

## Files

- `where-am-i.scm` - Main implementation
- `scheme-examples.scm` - Helper functions and examples


## Testing

Run all tests (kawa):
```scheme
(load "where-am-i.scm")
(test-all)
```

Individual tests:
```scheme
(test-intersection-points)
(test-distance-product)
(test-rate-points)
(test-sort-points)
(test-clumped-points)
(test-average-point)
(test-best-estimate)
(test-where-am-i)
```

## How It Works

1. Generate all possible star-distance pairings
2. Find intersection points of circles for each pairing
3. Identify which intersections are clustered (correct guess)
4. Return the most likely location based on clustering analysis