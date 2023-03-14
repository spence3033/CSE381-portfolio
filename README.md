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

### Grade Claim 1 problems

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

### 1.2 Problem 1

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


### Grade Claim 2 problems

### Selection Sort

```
import random

#setup
size = 10
unsortedNums = random.sample(range(1, 1000), size)

#print(unsortedNums)

#algorithm
def selectionSort(nums):
    for i in range(len(nums) - 1):
        smallest = i
        print(nums)
        for j in range(i, len(nums)):
            if nums[j] < nums[smallest]:
                smallest = j
        nums[i], nums[smallest] = nums[smallest], nums[i]
    return(nums)

#testing the algorithm
sortedNums = selectionSort(unsortedNums)
print(sortedNums)
```

### Insertion Sort

```
import random

#setup
size = 10
unsortedNums = random.sample(range(1, 1000), size)
print(unsortedNums)

#algorithm
def InsertionSort(nums):
    sortedArray = []
    unsortedArray = nums

    for x in unsortedArray:

        if len(sortedArray) == 0:
            sortedArray.append(x)
        else:
            sortedArray = InsertIntoSorted(sortedArray, x)

        print(sortedArray)

    return sortedArray

def InsertIntoSorted(sortedArray, num):
    for i in range(len(sortedArray)):
        if num < sortedArray[i]:
            sortedArray.insert(i, num)
            return sortedArray
        elif i + 1 == len(sortedArray):
            sortedArray.append(num)
            return sortedArray


#testing the algorithm
sortedNums = InsertionSort(unsortedNums)
print(sortedNums)
```

### Topological Sort

This is a graph problem so I figure puesdo code works best for this.

Topological Sorting: Breadth first-search

* Step 1: Look for any nodes that have no arrows leading to them. 
* Step 2: If none are found, the graph cannot be topologically sorted.
* Step 3: If some are found, add them one by one to the stack, the order doesn't matter.
* Step 4: If you run out of nodes, you are finished and the stack is your sorted graph.
* Step 5: Repeat back to step 1.
    

### 3.1 Problem 3

For each of the algorithms in Problems 4, 5, and 6 of Exercises 2.3, tell whether
or not the algorithm is based on the brute-force approach.

Problem 4: 
S = S + i^2
As i goes to n?
I'm not sure this is brute force or not. I can see that it's a recursive problem. So it could go on n times for a certain amount of numbers, and there may be a way to find an algorithm that doesn't require the recursiveness.

Problem 5:
I think we are iterating through an array for the min and max values, then getting the difference of them.
I think it would be O(n).
This one is brute force because you have to go through the entire array with no shortcuts.

Problem 6:
I think we are iterating through at array that is n * n. And I think we are going through all the values one by one.

So it should be O(n^2)
This one is brute force. becuase we are going through an array that is n*n and there are no shortcuts.

### 3.1 Problem 7

A stack of fake coins There are n stacks of n identical-looking coins. All of
the coins in one of these stacks are counterfeit, while all the coins in the other
stacks are genuine. Every genuine coin weighs 10 grams; every fake weighs
11 grams. You have an analytical scale that can determine the exact weight of
any number of coins.

a. Devise a brute-force algorithm to identify the stack with the fake coins and
determine its worst-case efficiency class.

The brute force is check every coin to be counterfeit. So O(n^2).

b. What is the minimum number of weighings needed to identify the stack
with the fake coins?

The minimum (I'm not sure if this is about being lucky in finding the right stack or having a algorithm that has the least searches),
So you could find the stack on the first try. So 1 guess. But if it's about the worst senerio with the best algorithm, then it is O(n) becuase you only need to check one coin from each stack.

### 3.1 Problem 8

Sort the list E, X, A, M, P , L, E in alphabetical order by selection sort.

* E, X, A, M, P, L, E
* A, E, X, M, P, L, E
* A, E, X, M, P, L, E
* A, E, E, X, M, P, L
* A, E, E, L, X, M, P 
* A, E, E, L, M, X, P 
* A, E, E, L, M, P, X
* A, E, E, L, M, P, X

### 3.1 Problem 9

Is selection sort stable? (The definition of a stable sorting algorithm was given
in Section 1.3.)

Yes. I think it is stable because selection sort will not mix up the order of items that are of the same value. Selection sort will choose the first item that was smallest. So if we ordered by number and we had items:

(1, A) (1, C) (2, A) (1, B)

I was incorrect: Selection sort is unstable because we are throwing values backwards, this could mess up the order.

For example: AEEEAEEE

The first E will switch with A and end up not being the first E in the end.

Selection sort would leave the 1's in the same order.
So...

(1, A) (1, C) (1, B) (2, A)

### 4.1 Problem 1

Ferrying soldiers - A detachment of n soldiers must cross a wide and deep
river with no bridge in sight. They notice two 12-year-old boys playing in a
rowboat by the shore. The boat is so tiny, however, that it can only hold two
boys or one soldier. How can the soldiers get across the river and leave the
boys in joint possession of the boat? How many times need the boat pass from
shore to shore?

n, 2 boys playing in a rowboat. The boat holdes 2 boys or 1 soldier. 
How to leave the boys in joint possession of the boat? 
and how many times to go from shore to shore?

1. I assume they mean there needs to be a boy on one side of the river and one on the other. So both boys need to go to one side, then one comes back. So two passes initially.
2. Then a soldier goes to the other shore. Then the boy with the soldiers goes back to the other boy, both go accross and one comes back so theres one boy on each side. 4 passes.
3. Then repeat step 2.

4 * n + 2.


### 4.2 Problem 1

Apply the DFS-based algorithm to solve the topological sorting problem for
the following digraphs:

Topological sorting is only possible if it is a directed acyclic graph (DAG). Essentially there is a direction that they can be sorted from what I can understand. There are two efficient algorithms that verify if a digraph is a DAG and produces an odering of vertices that solves the topological sorting problem.

1st algorithm DFS traversal: application of depth-first search: Follow some lines and note when the order of the vertices become dead-dens (pip off the traversal stack) Reversing the order yields a solution assuming no back edge has been encountered. If a back edge has been encountered the digraph is not a DAG.

2nd algorithm: 

First Diagraph: D, A, C, B, G, E, F

Second Diagraph: F, No dead end found, So it's not a DAG (directed acyclic graph).

## Grade Claim 3

### Russion Peasant
```
# two positive integers
x = 30
y = 30

def russianPeas(x, y, total):
    print(x, y)
    if (x == 1):
        total += y
        return total
    elif (x % 2 == 1):
        total += y
        x -= 1
        x = x / 2
        y = y * 2
    else:
        x = x / 2
        y = y * 2
    returnValue = russianPeas(x, y, total)
    return returnValue

answer = russianPeas(x, y, 0)
print(answer)

```

### MergeSort

### Quicksort

### PuIP Problem Reduction

### Problem 5.1: 1(a,b,c,d)

### Problem 5.1: 2(a,b,c)

### Problem 5.2: 5(a,b)
