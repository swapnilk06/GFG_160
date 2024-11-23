
## Day 1 - Second Largest Element

### Problem statement :

Given an array arr, return the second largest distinct element from an array. If the second largest element doesn't exist then return -1.

Sample Test Cases :
Input:  12 35 1 10 34 1  <br>
Output: 34<br>

Input:  10 5 10<br>
Output: 5<br>

Input:  10 10 10 <br>
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



## Day 2 - Move all Zeros to End

### Problem statement :

Given an array of integers arr[], the task is to move all the zeros to the end of the array while maintaining the relative order of all non-zero elements. 
(Changes should be done in place)

Sample Test Cases :
Input arr[] = {1, 2, 0, 4, 3, 0, 5, 0}
Output arr[] = {1, 2, 4, 3, 5,0, 0, 0}
Explanation: There are three 0's that are moved to the end.

Input arr[] = {10, 20, 30}
Output arr[] = {10, 20, 30}
Explanation: No change in array as there are no 0s.

Input arr[] = {0, 0}
Output arr[] = {0, 0}
Explanation: No change in array as there are no 0s.

***


### Approach 1:










