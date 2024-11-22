
## Day 1 - Second Largest Element

### Problem statement :

Given an array arr, return the second largest distinct element from an array. If the second largest element doesn't exist then return -1.

Sample Test Cases :
Input:  12 35 1 10 34 1
Output: 34

Input:  10 5 10
Output: 5

Input:  10 10 10 
Output: -1

***


### Approach 1:

#### Using Sorting - 
12 35 1 10 34 1 35
#### Sort all the elements -
1 1 10 12 34 35 35
- Don't need that to be sorted, that is some extra work that we are putting, that should be avoided.

#### Return the unique second last element.
34

#### Complexity analysis:
T.C. -> O(nlogn) 

S.C. -> O(1)
- Sorting algorithm nlogn & traval nth time n.
- not using any extra space here.

<br>

### Approach 2:

#### In two Iterations - 
- in first iteration, we can find out the maximum.

#### Find max value in 1st iteration -
- 'll find out Is the maximum value.

#### Find max value (less than the previous) in 2nd iteration - 
- biggest value less than 35.

#### Complexity analysis:
T.C. -> O(2n) ~ O(n)

S.C. -> O(1)

<br> 

### Approach 3:  
- Better approach to it in which we can do all of this work in just one single iteration.

### In One Iteration - 
-  sample that we are doing.

### Look for max and keep track of the previous updated value and Second max value -
- using max & sec variable using

#### Complexity analysis:
T.C. -> O(n)

S.C. -> O(1)



```python

# Approach 3 : one single iteration use in code.

def print2largest(self, arr):
    n = len(arr)
    if n < 2:
        return -1
        
    first = second = float('-inf')
    for num in arr:
        if num > first:
            second = first
            first = num
        elif num > second and num != first:
            second = num
            
    if second == float('-inf'):
        return -1
    else:
        return second

```






