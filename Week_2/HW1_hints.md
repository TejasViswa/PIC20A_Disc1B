# HW1 Hints

## Task 1
- Loop thru the array and get average.

## Task 2
- [Converting decimal to binary](https://www.cuemath.com/numbers/decimal-to-binary/) - See this if you are unsure how to convert decimal to binary
- Remember you only have ints here and you are finding only the positive binary conversion and adding a sign if required
- while loops are more convenient because the number of loops are not set
- use long for your input decimal number once you take in as an int (remember you should not change the method signature itself) - so that you can the handle the case for -2147483648 which when becomes positive ie: 2147483648 is too large for int to handle (limit of int is 2147483647)

## Task 3
- Remember arrays in Java are jagged (ie: they need not be rectangular) so make sure to check if all of the arrays have the same length, exit as soon as any one of them does not have the same length.
- For magic squares, the values range only from 1 to N^2 and exactly once. Exit if anything appears twice or something is beyond this range.
- You may use a boolean array whose indexes act as the values you are checking for in the magic square. ie: if you find 5 in the magic square then you are going to mark the 5th location in this boolean array as true (ie: used[4] - here used is the name of the boolean array and 4 actually refers to the 5th location because indexing in ana array is N-1 as it starts from 0).
- In total, you will first need two for loops to iterate through the array of arrays and a bunch of if statements within them to check for out of range and repeated occurence condition (if a value appears twice then used[value-1] (indexing hence value-1 instead of value) is goging to already be true instead of false) and only then are you going to amrk it to be true. Then another separate for loop outside these nested for loops to check if all the locations within the boolean array is marked true. This way you are sure that all the values from 1 to N^2 are there and appear exactly once.
- Everything should sum upto magic total (Remember you get N from the length of an individual array) and summing up rows is with 2 loops, inner loop for second index and outer loop for first index. And vice versa for column. For the two diagonals - think about the indexes of diagonals - how are they special?

## Task 4
- How can you optimize the prime number program?
- A few hints could be:
  - Do you need to search for all the numbers?
    - You know that some numbers cannot be prime - like even numbers (other than 2)
    - you don't have to search all the numbers until the candidate to see if its divisible - where do you think you should stop? (hint: think of factors and square roots)
    - [Sieve of Erasthosthenes](https://web.nmsu.edu/~pbaggett/Lessons/primeNumbers/primeNumbers.html)
    - Another really important thing - your task requires you to get all list of primes. To find if a number is prime or not, then the main criteria it needs to fulfill is that it shouldn't be divisible by the previous list of primes (which you already have). This probably enough to really boost your program execution speed.
 
