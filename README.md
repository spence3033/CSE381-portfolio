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

So 1

b. . Estimate how many times faster it will be to find gcd(31415, 14142) by
Euclid’s algorithm compared with the algorithm based on checking consecutive integers from min{m, n} down to gcd(m, n).

Euclid's algorithm = log_2 (14142) = 13.787698544

Normal = 14142

Times Faster = 14142/13.79 = 1025.53

1025 times faster


### 1.1 Problem 12:

Locker doors There are n lockers in a hallway, numbered sequentially from
1 to n. Initially, all the locker doors are closed. You make n passes by the
lockers, each time starting with locker #1. On the ith pass, i = 1, 2,...,n, you
toggle the door of every ith locker: if the door is closed, you open it; if it is
open, you close it. After the last pass, which locker doors are open and which
are closed? How many of them are open?

I remember the discussion of this one because it had a fasinating outcome. I hadn't done it before class because it didn't understand what was being asked.

So to begin: 
* one pass one you toggle lockers divisible by 1 (1,1,1,1,1)
* second pass you toggle lockers divisible by 2 (1,0,1,0,1)
* 3 (1,0,0,0,1)
* 4 (1,0,0,1,1)
* 5 (1,0,0,1,0)

The ending will be that all lockers that are perfect squares will be open. And all non perfect squares will be closed.

So 1,4,9,16,25,etc.

### 1.2 Problem 1

A peasant finds himself on a riverbank with a wolf, a goat,
and a head of cabbage. He needs to transport all three to the other side of the
river in his boat. However, the boat has room for only the peasant himself
and one other item (either the wolf, the goat, or the cabbage). In his absence,
the wolf would eat the goat, and the goat would eat the cabbage. Solve this
problem for the peasant or prove it has no solution. (Note: The peasant is a
vegetarian but does not like cabbage and hence can eat neither the goat nor
the cabbage to help him solve the problem. And it goes without saying that
the wolf is a protected species.)

Peasant should take the goat accross.
Then the Peasant should take the cabbage accross.
Then lastly take the wolf accross.

### 1.2 Problem 6:

Describe the algorithm used by your favorite ATM machine in dispensing
cash. (You may give your description in either English or pseudocode, whichever you find more convenient.)

I haven't ever used an atm machine. So I'm going to list of steps I  see from a video from getting cash from an atm.

* Step one: Check the atm machine says "Please insert your card. Do not remove."
* Step two: Insert your credit card and leave it there.
* Step three: Type in your PIN.
* Step four: Chosse a type of transaction
* Step five: check your balance to know if you can withdraw money
* Step six: Click the transaction amount
* Step seven: Select your receipt preference
* Step eight: take receipt, take your card, and take your withdrawn money.

### 1.4 Problem 2

If you have to solve the searching problem for a list of n numbers, how can you
take advantage of the fact that the list is known to be sorted? Give separate
answers for

a. lists represented as arrays.

If an array is sorted, the fastest way I know how to find a value is check halfway in the array and see if the value is larger or smaller than the value I'm looking for.

If it is to small, check halfway in the lower values and repeat the process of going halfway into the arrays that you know you value can be found. The same will go the value I'm looking for is larger than the item I saw.

There also is the possiblity the array does not have the value I'm looking for as well.

b. lists represented as linked lists.

For a linked list you don't know how to get halfway into the array because each next item in the list is only found where the previous value is.

So you would have to go through values one by one to find where the next value is linked to and skim through the values. So if you are looking say for 43 and the first value is 1 in the list. You will check each value after 1 in the list and keep checking to make sure each value is less than 43 and rising until you eventually find 43 or you go higher than 43 which means 43 doesn't exist in the list.



### 2.1 Problem 4ab

a. Glove selection: There are 22 gloves in a drawer: 5 pairs of red gloves, 4
pairs of yellow, and 2 pairs of green. You select the gloves in the dark and
can check them only after a selection has been made. What is the smallest
number of gloves you need to select to have at least one matching pair in
the best case? In the worst case?

10 red gloves, 8 yellow, 4 green.

The best case is two guesses will get you a matching pair of gloves.

The worst case will depend on the color you are going for and making sure you are pulling gloves out of the drawer and not putting them back. If you are going for red, you could take 14 guesses. If you are going for yellow, it could take 16 guesses. And for green, it could take 20 guesses.

If you keep putting the gloves back in you could go on forever because you always have a chance of selecting the right or wrong gloves continually.


b. Missing socks: Imagine that after washing 5 distinct pairs of socks, you
discover that two socks are missing. Of course, you would like to have
the largest number of complete pairs remaining. Thus, you are left with
4 complete pairs in the best-case scenario and with 3 complete pairs in
the worst case. Assuming that the probability of disappearance for each
of the 10 socks is the same, find the probability of the best-case scenario;
the probability of the worst-case scenario; the number of pairs you should
expect in the average case

5 paires - 2 socks missing

Best-case scenario 1/9 (11.11%) chance of both socks being a matching pair. The reason is it doesn't matter what first sock was selected. But there are 9 socks left, and you wish only 1 specific sock was selected which was the matching sock to the first sock missing.

Worst-case scenario 8/9 (88.88%) chace of missing one sock from one pair and another sock from another pair.



### 2.1 Problem 9a-f

For each of the following pairs of functions, indicate whether the first function
of each of the following pairs has a lower, same, or higher order of growth (to
within a constant multiple) than the second function.

a. n(n + 1) and 2000n2 
* first function will always be less than the second function
* but they do have the same big-O growth. So I guess they actually do have the same order of growth

b. 100n2 and 0.01n3
* first function has a smaller order of growth to the second function

c. log2 n and ln n 
* according to big-O. These are the same.
* But log2 n is slightly growing faster.

d. log2 2 n and log2 n2
* the first function has a higher growth rate than the second function 
* log(n)^2 is higher because log(n^2) simplifies to 2 * log(n) which is only log(n) in big-O notation. 

e. 2n−1 and 2n 
* The first funciton has a lower growth rate than the second function

f. (n − 1)! and n!
* The first funciton has a lower growth rate than the second function

### 2.2 Problem 1

. Use the most appropriate notation among O, , and  to indicate the time
efficiency class of sequential search (see Section 2.1)

a. in the worst case.
O(n)

b. in the best case.
Big Theta(1)

c. in the average case.

Possibly: Big Omega(1) - O(n)

Or Big Theta(n/2). 

I'm not entirely sure.

### 2.2 Problem 2a-d

a. n(n + 1)/2 ∈ O(n3) 

This is true. The growth is within the bounds set.

b. n(n + 1)/2 ∈ O(n2)

I suppose false? The growth is the same, but the function is technically is over the bounds set.

c. n(n + 1)/2 ∈ Big Theta(n3) 

This is false.

d. n(n + 1)/2 ∈ Big Omega(n)

This is true.

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

```
import random

#setup
size = 7
unsortedArray = random.sample(range(1, 100), size)

def mergeSort(arr):

    print(arr)

    if(len(arr) != 1):
        num = len(arr) // 2
        firstArr = arr[:num]
        secondArr = arr[num:]

        firstSortedArr = mergeSort(firstArr)
        secondSortedArr = mergeSort(secondArr)

        i = 0
        j = 0

        combinedSortedArr = []
        
        print(f"sorting: {firstSortedArr} :: {secondSortedArr}")

        while(i < len(firstSortedArr) or j < len(secondSortedArr)):
            # This is just in case the while loop didn't quite
            if(i == len(firstSortedArr) and j == len(secondSortedArr)):
                print("This should NOT HAPPEN")
                break
            elif(i >= len(firstSortedArr) and j < len(secondSortedArr)):
                print(f"first array finished: add {secondSortedArr[j]}")
                combinedSortedArr.append(secondSortedArr[j])
                j += 1
            elif(j >= len(secondSortedArr) and i < len(firstSortedArr)):
                print(f"Second array finished: add {firstSortedArr[i]}")
                combinedSortedArr.append(firstSortedArr[i])
                i += 1

            elif(firstSortedArr[i] < secondSortedArr[j]):
                print(f"Add {firstSortedArr[i]}")
                combinedSortedArr.append(firstSortedArr[i])
                i += 1
            else:
                print(f"Add {secondSortedArr[j]}")
                combinedSortedArr.append(secondSortedArr[j])
                j += 1
            
        print(combinedSortedArr)

        return combinedSortedArr

    else:
        return arr
    

sortedArray = mergeSort(unsortedArray)
print(sortedArray)
```

### Quicksort

```
import random

#setup
size = 7
unsortedArray = random.sample(range(1, 100), size)

def QuickSort(arr, low_index, high_index):

    print(arr, low_index, high_index)

    if (low_index < high_index):
        pivot_location = Partition(arr, low_index, high_index)
        QuickSort(arr, low_index, pivot_location)
        QuickSort(arr, pivot_location + 1, high_index)

def Partition(arr, low_index, high_index):
    pivot = arr[low_index]
    leftwall = low_index

    # print(f'pivot number: {pivot}')
    # print(f'leftwall index: {leftwall}')

    for i in range(low_index + 1, high_index + 1):
        # print(f'Array index: {arr}')
        if (arr[i] < pivot):
            arr[i], arr[leftwall] = arr[leftwall], arr[i]
            leftwall = leftwall + 1
        
    
    pivot, arr[leftwall] = arr[leftwall], pivot

    return(leftwall)
    

sortedArray = QuickSort(unsortedArray, 0, len(unsortedArray) - 1)
print(sortedArray)
```

### PuIP Problem Reduction
```
# import library
import pulp as p

# create a LP min problem
lp_prob = p.LpProblem('Problem', p.LpMinimize)
# create problem variables
x = p.LpVariable("x", lowBound = 0)
y = p.LpVariable("y", lowBound = 0)
# objective function
lp_prob += 3 * x + 5 * y
# constraints
lp_prob += 2 * x + 3 * y >= 12
lp_prob += -x + y <= 3
lp_prob += x >= 4
lp_prob += y <= 3
# display the problem
print(lp_prob)
# solver
status = lp_prob.solve()
# solution status
print(p.LpStatus[status])
# print solution
print(p.value(x), p.value(y), p.value(lp_prob.objective))
print("Answer should be 6, 0, 18")
```

### Problem 5.1: 1(a,b,c,d)

#### a. Write pseudocode for a divide-and-conquer algorithm for finding the position of the largest element in an array of n numbers.

It depends on in the array is sorted.
* Step 1: If array is sorted check one side
* Step 2: Check the other side and see which one is the biggest number.
* Step 3: Whichever is bigger, you'll know if the front or back is the position of the largest element

* Step 4: If array is unsorted, you will have to brute force and check every number and record the position of the largest found number.

#### b. What will be your algorithm’s output for arrays with several elements of the largest value?

The output would still be one position of one of the elements that are the largest value.

#### c. Set up and solve a recurrence relation for the number of key comparisons made by your algorithm.

It could be 2 or n. It depends on if the array is sorted or not.

#### d. How does this algorithm compare with the brute-force algorithm for this problem?

* for recurrence my algorithm: (2, n) 
* for brute-force: (n)

So it's only better in one case.

### Problem 5.1: 2(a,b,c)

#### a. Write pseudocode for a divide-and-conquer algorithm for finding values of both the largest and smallest elements in an array of n numbers.

Once again it depends on if the array is sorted.

If it's sorted
* Step 1: check the front of the array and save the value as the smallest.
* Step 2: check the back, if it's smaller than the front, save the back as the smallest number, and the front as the biggest.

If it's unsorted, all you can do is brute force it.
* Check every value for being smaller or bigger than the last saved number.

If you don't know
* Resort to doing brute force.

So either 2 checks or n*2

#### b. Set up and solve (for n = 2k) a recurrence relation for the number of key comparisons made by your algorithm.

My algorithm with n = 2k will be 2 or 4k comparisions. 

#### c. How does this this algorithm compare with the brute-force algorithm for this problem?

Brute force is automatically 4k comparisions.
My algorithm is 4k for an unsorted array, or 2 for a sorted array.

### Problem 5.2: 5(a,b)

For the version of quicksort given in this section:

#### a. Are arrays made up of all equal elements the worst-case input, the bestcase input, or neither?

This is the best case senario because you would discover every pivot is in the correct position.

#### b. Are strictly decreasing arrays the worst-case input, the best-case input, or neither?

This would be the worst case senario because you would have to switch the item-from-left and the item-from-right recusively the most times than in any other senario.


