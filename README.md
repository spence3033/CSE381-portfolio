# CSE381-portfolio

![reading assignments](https://github.com/spence3033/CSE381-portfolio/blob/c6fb37d5f66ddfada11c3ddcbcd6c0a64800d637/Screen%20Shot%202023-01-10%20at%204.41.59%20PM.png)

## Jan 5 class: Thursday
First day of Class!

## Jan 10 class: Tuesday

Learne about Euclid's Algorithm

![Euclid's algorithm](https://github.com/spence3033/CSE381-portfolio/blob/4b749ded8267a0190cf51d0cb02f44c9f707d89f/Euclids%20Algorithm.png)

## Jan 12 class: Thursday

Learning about units for measuring run time. There is actual run time, but there is also big-O notation.

Pusedo Code for playing the hilo game.
1. Know the range
2. pick the median of the range.
3. Was it Right?
4. If true, Stop! You won!
5. If no, 

a) Was it too high?
b) The range has been shortened from the bottom to the number just under the number chosen.
c) Now pick the median of the new range.
d) repeat back to step 3.

e) Was it too low?
f) The range has been shortened from the top to the number just above what was chosen.
g) Pick the median of the new range.
h) Repeat back to step 3.

### Jan 12 Preparation Reading

**The Design and Analysis of Algorithms: Section 2.2**

Asymptotic Notations and Basic Efficiency Classes

The efficiency analysis framework, computer scientists user three notations: $\mathcal{O}$ (big oh), $\Omega$ (big Omega), and $\Theta$ (big Theta)

Informal description: 

$\mathcal{O} (g(n))$ is all functions with a lower or same order of growth as $g(n)$.

$\Omega (g(n))$ is all functions with higher or same orderof growth.

$\Theta (g(n))$ all functions that have the same order of growth as $g(n)$.

**Using Limits for Comparing Orders of Growth**

A more convenient method for comparing growth is based on computing the limit of the ratio of the two functions in question.

I might want to ask about the mathamatical functions because the reading was confusing.

**Basic Efficiency Classes**

It may be a suprise that time efficiences fall into only a few classes.

There is the concern that larger classes outperform simpler classes, but few anomalies are known. But generally for even moderately sized inputs, this efficiency class setup will be correct.

## Jan 17 class: Tuesday

Binary Search

```
import random

def binarySearch(numlist, target):
    print(numlist)
    midpoint = len(numlist) // 2
    guess = numlist[midpoint]
    newnum = []

    if guess == target:
        print("You guessed it!")
        return guess

    elif guess < target:

        for i in range(midpoint + 1, len(numlist)):
            newnum.append(numlist[i])
        print(f"Too low, guess: {guess}")
    else:
        for i in range(0, midpoint):
            newnum.append(numlist[i])
    
        print(f"Too High, guess: {guess}")
    
    return binarySearch(newnum, target)

list = range(0, 99)
target = random.choice(list)

print(target)
print(binarySearch(list, target))
```

## Jan 19 problems:

![Alt text](https://github.com/spence3033/CSE381-portfolio/blob/05b41620e98b414e2ba4419ab201c308bc9b4be2/GC%20exercise%201.png)
![Alt text](https://github.com/spence3033/CSE381-portfolio/blob/d187f992157534d61f92ebc89584a565e12f07b0/GC%20exercise%202.png)
![Alt text](https://github.com/spence3033/CSE381-portfolio/blob/d187f992157534d61f92ebc89584a565e12f07b0/GC%20exercise%203.png)
![Alt text](https://github.com/spence3033/CSE381-portfolio/blob/d187f992157534d61f92ebc89584a565e12f07b0/GC%20exercise%204.png)

## Jan 24 class: Tuesday

### Grade Claim problems

### 1.1 Problem 6:

a. Find gcd(31415, 14142) by applying Euclid's algorithm. 

* 31415, 14142
* 14142, 3131
* 3131, 1618
* 1618, 1513
* 1513, 105
* 105, 43
* 43, 19
* 19, 5
* 5, 4
* 4, 1

So 1??


b. . Estimate how many times faster it will be to find gcd(31415, 14142) by
Euclid’s algorithm compared with the algorithm based on checking consecutive integers from min{m, n} down to gcd(m, n).



### 1.1 Problem 12:

Locker doors There are n lockers in a hallway, numbered sequentially from
1 to n. Initially, all the locker doors are closed. You make n passes by the
lockers, each time starting with locker #1. On the ith pass, i = 1, 2,...,n, you
toggle the door of every ith locker: if the door is closed, you open it; if it is
open, you close it. After the last pass, which locker doors are open and which
are closed? How many of them are open?

 ### 1.2 Problem 6:

Describe the algorithm used by your favorite ATM machine in dispensing
cash. (You may give your description in either English or pseudocode, whichever you find more convenient.)

### 1.4 Problem 2

If you have to solve the searching problem for a list of n numbers, how can you
take advantage of the fact that the list is known to be sorted? Give separate
answers for
a. lists represented as arrays.
b. lists represented as linked lists.

### 2.1 Problem 4ab

a. Glove selection There are 22 gloves in a drawer: 5 pairs of red gloves, 4
pairs of yellow, and 2 pairs of green. You select the gloves in the dark and
can check them only after a selection has been made. What is the smallest
number of gloves you need to select to have at least one matching pair in
the best case? In the worst case?
b. Missing socks Imagine that after washing 5 distinct pairs of socks, you
discover that two socks are missing. Of course, you would like to have
the largest number of complete pairs remaining. Thus, you are left with
4 complete pairs in the best-case scenario and with 3 complete pairs in
the worst case. Assuming that the probability of disappearance for each
of the 10 socks is the same, find the probability of the best-case scenario;
the probability of the worst-case scenario; the number of pairs you should
expect in the average case

### 2.1 Problem 9a-f

For each of the following pairs of functions, indicate whether the first function
of each of the following pairs has a lower, same, or higher order of growth (to
within a constant multiple) than the second function.
a. n(n + 1) and 2000n2 b. 100n2 and 0.01n3
c. log2 n and ln n d. log2
2 n and log2 n2
e. 2n−1 and 2n f. (n − 1)! and n!

### 2.2 Problem 1

. Use the most appropriate notation among O, , and  to indicate the time
efficiency class of sequential search (see Section 2.1)
a. in the worst case.
b. in the best case.
c. in the average case.

### 2.2 Problem 2a-d
