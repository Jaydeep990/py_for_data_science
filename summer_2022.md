## Q.1
### (a) List Advantages of Python. 
- Presence of third-party modules 
- Extensive support libraries(NumPy for numerical calculations, Pandas for data analytics, etc.) 
- Open source and large active community base 
- Versatile, Easy to read, learn and write
- User-friendly data structures 
- High-level language 
- Dynamically typed language(No need to mention data type based on the value assigned, it takes data type) 
- Object-Oriented and Procedural  Programming language
- Portable and Interactive
- Ideal for prototypes – provide more functionality with less coding
- Highly Efficient(Python’s clean object-oriented design provides enhanced process control, and the language is equipped with excellent text processing and integration capabilities, as well as its own unit testing framework, which makes it more efficient.)
- Internet of Things(IoT) Opportunities
- Interpreted Language
- Portable across Operating systems 
### (b) Differentiate Numpy and Pandas.
|                                           PANDAS                                          |                                        NUMPY                                        |   |
|:----------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|---|
| When we have to work on Tabular data, we prefer the pandas module.                       | When we have to work on Numerical data, we prefer the numpy module.                 |   |
| The powerful tools of pandas are Data frame and Series.                                  | Whereas the powerful tool of numpy is Arrays.                                       |   |
| Pandas consume more memory.                                                              | Numpy is memory efficient.                                                          |   |
| Pandas has a better performance when a number of rows is 500K or more.                   | Numpy has a better performance when number of rows is 50K or less.                  |   |
| Indexing of the pandas series is very slow as compared to numpy arrays.                  | Indexing of numpy Arrays is very fast.                                              |   |
| Pandas offer a have2d table object called DataFrame.                                     | Numpy is capable of providing multi-dimensional arrays.                             |   |
| It was developed by Wes McKinney and was released in 2008.                               | It was developed by Travis Oliphant and was released in 2005.                       |   |
| It is used in a lot of organizations like Kaidee, Trivago, Abeja Inc. , and a lot more.  | It is being used in organizations like Walmart Tokopedia, Instacart, and many more. |   |
| It has a higher industry application.                                                    | It has a lower industry application.                                                |   |
### (c) Explain Exploratory Data Analysis (EDA).
- https://www.geeksforgeeks.org/what-is-exploratory-data-analysis/
## Q.2
### (a) Explain String Slicing in python with Example.
- Python slicing is about obtaining a sub-string from the given string by slicing it respectively from start to end. 
- Python slicing can be done Using array slicing  [ : : ] method
- string slicing in Python with example:
```
arr[start:stop]         # items start through stop-1
arr[start:]             # items start through the rest of the array
arr[:stop]              # items from the beginning through stop-1
arr[:]                  # a copy of the whole array
arr[start:stop:step]    # start through not past stop, by step
```
### (b) List and Explain different programming styles in python.
- There are four main Python coding styles: imperative, functional, object-oriented, and procedural.
- `1.Functional`:
  - Every statement is treated as a mathematical equation and any forms of state or mutable data are avoided. 
  - The main advantage of this approach is that it lends itself well to parallel processing because there is no state to consider.
  - Many developers prefer this coding style for recursion and for lambda calculus.
- `2.Imperative`:
  - Computation is performed as a direct change to program state.
  - This style is especially useful when manipulating data structures and produces elegant yet simple code. 
  - Python fully implements this paradigm.
- `3.Object-oriented`:
  - Relies on data fields that are treated as objects and manipulated only through prescribed methods.
  - Python doesn’t fully support this paradigm because it can’t implement features such as data hiding (encapsulation), which many believe is a primary requirement of the object-oriented programming paradigm.
  - This coding style also favors code reuse.
- `4.Procedural`:
  - Tasks are treated as step-by-step iterations where common tasks are placed in functions that are called as needed. 
  - This coding style favors iteration, sequencing, selection, and modularization.
  - Python excels in implementing this particular paradigm.
## (c) Write a program to check whether the given number is prime or not.
```python
# To take input from the user
num = int(input("Enter a number: "))

# define a flag variable
flag = False

# prime numbers are greater than 1
if num > 1:
    # check for factors
    for i in range(2, num):
        if (num % i) == 0:
            # if factor is found, set flag to True
            flag = True
            # break out of loop
            break

# check if flag is True
if flag:
    print(num, "is not a prime number")
else:
    print(num, "is a prime number")
```
### (c) Write a program to print Fibonacci series up to number given by user.
```python
# Program to display the Fibonacci sequence up to n-th term

nterms = int(input("How many terms? "))

# first two terms
n1, n2 = 0, 1
count = 0

# check if the number of terms is valid
if nterms <= 0:
   print("Please enter a positive integer")
# if there is only one term, return n1
elif nterms == 1:
   print("Fibonacci sequence upto",nterms,":")
   print(n1)
# generate fibonacci sequence
else:
   print("Fibonacci sequence:")
   while count < nterms:
       print(n1)
       nth = n1 + n2
       # update values
       n1 = n2
       n2 = nth
       count += 1
```
## Q.3
### (a) Differentiate rand and randn function in Numpy.
|                                                 rand function in numpy                                                 |                                                 randn function in numpy                                                |
|:----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------:|
| random.randn(d0, d1, ..., dn)                                                                                          | random.rand(d0, d1, ..., dn)                                                                                           |
| Parameters                                                                                                             | Parameters                                                                                                             |
| d0, d1, …, dn : int, optional                                                                                          | d0, d1, …, dn : int, optional                                                                                          |
| The dimensions of the returned array, must be non-negative. If no argument is given a single Python float is returned. | The dimensions of the returned array, must be non-negative. If no argument is given a single Python float is returned. |
| Return a sample (or samples) from the “standard normal” distribution.                                                  | Return a random sample from a uniform distribution over [0, 1).                                                        |
| np.random.rand(3)                                                                                                      | np.random.randn(3)                                                                                                     |
| [ 0.04604743 -1.12499395 -0.42282234]                                                                                  | [0.63016653 0.77964169 0.92521163]                                                                                     |
### (b) Explain DataFrame in Pandas with example.
- A Data frame is a two-dimensional data structure.
- i.e., data is aligned in a tabular fashion in rows and columns.
- Features of DataFrame
  - Potentially columns are of different types
  - Size – Mutable
  - Labeled axes (rows and columns)
  - Can Perform Arithmetic operations on rows and columns
 - Structure
  ![image](https://media.geeksforgeeks.org/wp-content/uploads/finallpandas.png)
 - Create DataFrame
  - A pandas DataFrame can be created using various inputs like −
    - Lists
    - dict
    - Series
    - Numpy ndarrays
    - Another DataFrame
 - Creating DataFrame from dict of lists: 
  ```python
    import pandas as pd

  # intialise data of lists.
  data = {'Name':['Tom', 'nick', 'krish', 'jack'],
          'Age':[20, 21, 19, 18]}

  # Create DataFrame
  df = pd.DataFrame(data)

  # Print the output.
  print(df)
  ```
  ```python
      Output:
        Name  Age
    0    Tom   20
    1   nick   21
    2  krish   19
    3   jack   18
  ```
### (c) Write a program to print following patterns.
```
1)
*
* *
* * *
* * * *
2)
$ $ $ $
$ $ $
$ $
$
3)
# # # # #
 # # #
   #
 # # #
# # # # #
```
```python
1.
for i in range(4):
    for j in range(4):
        if i>=j:
            print('*',end=" ")
    print()
2.
for i in range(4):
    for j in range(4):
        if i<=j:
            print('*',end=" ")
    print()
```

