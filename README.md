# Pattern recognition
This is the midterm project for the [Parallel Computing](https://www.unifi.it/index.php?module=ofform2&mode=1&cmd=3&AA=2022&afId=628836) course at [University of Florence](https://www.unifi.it/).
The goal is to implement a sequential and a parallel version of a pattern recognition program.

## Project description
Given a time series we want to find a match within a longer time series.
The metric to evaluate the match will be the [SAD](https://en.wikipedia.org/wiki/Sum_of_absolute_differences).
### Observations
A **time series** is a series of data points indexed in time order. 

We have to of them:
1. The series that we want to analyze
2. The reference series

In the reference series we don't need the time component, as long as it is ordered.

What we have to do is for a given "long" time series, slide on it a fixed "smaller" one and evaluate a match at every step.

#### Example:
Given the "long" time series: [2,4,5,7,1,6,7,9,1,3], slide of it the fixed "smaller" one [1,2,3].
We have to evaluate the match with SAD for:
1. [2,4,5] with [1,2,3]
2. [4,5,7] with [1,2,3]
3. [5,7,1] with [1,2,3]
4. [7,1,6] with [1,2,3]
5. ...
6. [9,1,3] with [1,2,3]
   
The **smallest** evaluation gives us the best subsequence that matches the reference series.

## Abstract steps to implement the project:
- Write a sequential version of the program
- Check that the sequential code works correctly
- Refactor the code to parallelize the application
- Check that the parallel/vectorized version gives the same results as the sequential one

Every step will be decomposed and described in the [GitHub issues](https://github.com/cMancio00/Pattern-recognition/issues).



