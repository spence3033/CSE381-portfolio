# CSE381-portfolio

![reading assignments](https://github.com/spence3033/CSE381-portfolio/blob/c6fb37d5f66ddfada11c3ddcbcd6c0a64800d637/Screen%20Shot%202023-01-10%20at%204.41.59%20PM.png)

## Jan 5 class: Thursday
First day of Class!

## Jan 10 class: Tuesday

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

Grade Claim problems

Complete 4 exercises for asymptotic notation practice. Found in assigned problems tab in teams.

1. 
2.
3.
4.

1.1 Problem 6:

1.1 Problem 12:

1.2 Problem 6:

1.4 Problem 2

2.1 Problem 41b

2.1 Problem 9a-f

2.2 Problem 1

2.2 Problem 2a-d
