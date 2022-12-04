# Move Zeroes

## Problem Statement


> Given an integer array nums, move all 0's to the end of it while maintaining the relative order of the non-zero elements.

> Note that you must do this in-place without making a copy of the array.


Source: https://leetcode.com/problems/move-zeroes/description/

## Solution


### 1. State the problem clearly. Identify the input & output formats.


**Problem**

> Given an integer array nums, move all 0's to the end of it while maintaining the relative order of the non-zero elements.

> Note that you must do this in-place without making a copy of the array.

<br/>


**Input**

1. nums = [0,1,0,3,12]


**Output**

1. [1,3,12,0,0]


<br/>

Based on the above, we can now create a signature of our function:


```python
def move_zeroes(nums):
    pass
```

### 2. Come up with some example inputs & outputs. Try to cover all edge cases.


1. All zeroes.
2. All non-zeroes.
3. first element is zero.
4. first element is non-zero.


```python
tests = []
```


```python
tests.append({
    'input': {
        'nums' : [0,0,0]
    },
    'output': [0,0,0]
})
```


```python
tests.append({
    'input': {
        'nums' : [1,1,1]
    },
    'output': [1,1,1]
})
```


```python
tests.append({
    'input': {
        'nums' : [0,1,0,3,12]
    },
    'output': [1,3,12,0,0]
})
```


```python
tests.append({
    'input': {
        'nums' : [10,1,0,3,12]
    },
    'output': [10,1,3,12,0]
})
```

### 3. Come up with a correct solution for the problem. State it in plain English.


> **Brute Force** <br>
> extra space

###  4. Implement the solution and test it using example inputs. Fix bugs, if any.


```python
def move_zeroes(nums):
    
    # Result list
    res = []
    
    # Counter for zeroes
    c = 0
    
    # Set a loop for append non-zeroes
    for num in nums:
        if num:
            res.append(num)
        else:
            c += 1

    # Set a loop for append zeroes
    for _ in range(c):
        res.append(0)
    
    # Copy result to nums list
    nums = res[:]
    
    # Return nums list
    return nums
```


```python
for i in range(len(tests)):
    
    print(move_zeroes(tests[i]['input']['nums'])==tests[i]['output'])
```

    True
    True
    True
    True
    

### 5. Analyze the algorithm's complexity and identify inefficiencies, if any.

> Time complexity : **O(N)** <br>
> Space complexity : **O(N)**

### 6. Apply the right technique to overcome the inefficiency. Repeat steps 3 to 6.

> **Two Pointer**

### 7. Come up with a correct solution for the problem. State it in plain English.


> one pointer for iterating the list and another pointer that just works on the non-zero elements of the list.

### 8. Implement the solution and test it using example inputs. Fix bugs, if any.


```python
def moveZeroes(nums):
    
    # Find zero element's index
    slow = 0
    
    # Find non-zero and swap with zero
    for fast in range(len(nums)):
        
        # If None-zero than swap 
        if nums[fast] != 0:
            
            # swap
            nums[slow], nums[fast] = nums[fast], nums[slow]
            
            # Increment slow
            # For zero element's index
            slow += 1
    
```


```python
for i in range(len(tests)):
    print(move_zeroes(tests[i]['input']['nums'])==tests[i]['output'])
```

    True
    True
    True
    True
    

### 9. Analyze the algorithm's complexity and identify inefficiencies, if any.

> Time complexity : **O(N)** <br>
> Space complexity : **O(1)**
