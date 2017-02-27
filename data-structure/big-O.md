# Algorithms and big O

## What is an algorithm
* A set of steps to solve a certain problem
* They have a goal and terminate at some point in time
* Take an input and produce an output
* Generally are very reusable for different problems

## Types of algorithms
* Brute force
* Divide and conquer
* Search

## Analysis of algorithms
* In CS the analysis of algorithms is the determination of the amount of resources necessary to execute them. Most algorithms are designed to work with inputs

## BIG O
* given a certain input how will the runtime change based upon the size of the input

## What is big O
* Allows programers to discuss the complexity of an algorithm and understand how fast the runtime will grow given its input in the worst case.
* How long will it take when the input is 100 or 1000 or 1000000.

## BIG O at a glance
* constant time
* linear
* Quadratic or Polynomial

```js
function print50Nums() {
  for (var i = 0; i < 50; i++) {
    console.log(i);
  }
}
```

* The run time is always the same
* Constant
* O(50) or O(1)

```js
function sum(numbers) {
  var total = 0;
  for (var i = 0; i < numbers.length; i++) {
    total += numbers[i];
  }
  return total;
}
```
* The runtime is not always the same
* Each time the input grows the time increases in the same way
* Linear
* O(n)

```js
function sumMatrix(matrix) {
  var total = 0;
  for (var i = 0; i < matrix.length; i++) {
    for (var j = 0; j < matrix[i].length; j++) {
      total += matrix[i][j]
    }
  }
  return total;
}
```
* The runtime is not always the same
* It's n times n
* Quadratic
* O(n^2)

## When it comes into play
* access time
* search time
