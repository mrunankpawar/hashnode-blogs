# Mastering the basics of Numpy: Unlock the power of arrays and matrices

### What is Numpy?

Numpy is like a toolbox for people who like to work with numbers, especially lots and lots of numbers. Imagine you have a big box of legos, but instead of building blocks, each lego represents a number. Numpy helps you organize and play with these lego numbers smartly and efficiently. You can use it to stack legos into neat rows and columns, and perform mathematical operations with them.

### List vs Numpy in Python

![](https://miro.medium.com/max/612/0*f7EjQfSfGzT5evMz.jpeg align="center")

**Numpy is better than Python Lists in the following ways:**

* Time efficient
    
* Space efficient
    
* Convenient
    
* Utilizes contiguous memory
    
* Matrix operations
    

### Let's get our hands dirty!

You can copy-paste these code snippets into [Jupyter notebook](https://jupyter.org) and play around with these amazing numbers in Numpy. Also make sure you have Numpy installed, if not you can install it using this [guide](https://numpy.org/install/) or if you use pip then you can install numpy using `pip install numpy` .

##### ⏳ Load numpy

```python
import numpy as np
```

##### ⚡️ The Basics

`np.array()` helps you to create an array.

```python
# Print a 1-D array 
a = np.array([1,2,3], dtype="int16") 
print(a)

# OUTPUT
# [1 2 3]
```

`dtype` allows you to specify the data type.

```python
# Print a 2-D array
b = np.array([[1.0, 3.0, 6.0], [4.0,5.0,4.0]])
print(b)

# OUTPUT
# [[1. 3. 6.]
#  [4. 5. 4.]]
```

`ndim` provides you with the dimensions of your array.

```python
# Get dimension
a.ndim

# OUTPUT
# 1
```

`shape` helps you to understand the shape of an array in terms of (rows, columns).

```python
# Get shape
b.shape

# OUTPUT
# (2, 3)
```

`size` provides you with the total number of elements in an array.

```python
# Get size
a.size

# OUTPUT
# 3
```

`itemsize` gives you the size of each element in an array.  
eg. As we have `dtype=int16` for array a, we should get `itemsize` of 2.

```python
# Get itemsize
a.itemsize

# OUTPUT
# 2
```

Now, what if you want to get the total size of all elements in an array? Let's get some MATHS done!

We can multiply the `itemsize` of element by a total `size` of an array.

```python
# Get total size
a.size * a.itemsize

# OUTPUT
# 6
```

##### 🧩 Accessing/ Changing specific elements, rows, columns, etc.

```python
a = np.array([[1,2,3,4,5,6,7], [8,9,10,11,12,13,14]])
print(a)

# OUTPUT
# [[ 1  2  3  4  5  6  7]
#  [ 8  9 10 11 12 13 14]]
```

So is there any way that I can access element 13?  
Yes, there is!

*Note: Always keep in mind that indexing always starts from 0.*

```python
# Get specific element [row, column]
a[1, 5]

# OUTPUT
# 13
```

We can also access entire rows by using `:` in place of the column and vice-versa.

```python
# Get specific row
a[0, :]

# OUTPUT
# array([1, 2, 3, 4, 5, 6, 7])
```

```python
# Get specific column
a[:, 5]

# OUTPUT
# array([ 6, 13])
```

Let's deep dive into some advanced types we can access the elements.  
Here, we are looking into 1st row (index 0) and in that, we want to consider the columns that start from 0 - 5 with a step size of 2.

```python
# Getting into more details (start:stop:step-size)
a[0, 0:5:2]

# OUTPUT
# array([1, 3, 5])
```

Now, that we have a clear idea of accessing the elements, let's see if we can change the values of these elements.  
To answer that, it's a big YES.

```python
# Changing a particular element
a[1, 5] = 20

# OUTPUT
# [[ 1  2  3  4  5  6  7]
#  [ 8  9 10 11 12 20 14]]
```

In the above code snippet, we accessed the element at row 1 and column 5 and changed its value to 20.

Now, let's get a bit fancier and update both values in both rows in column 2.

```python
a[:, 2] = [5, 10]
print(a)

# OUTPUT
# [[ 1  2  5  4  5  6  7]
#  [ 8  9 10 11 12 20 14]]
```

***That's all for now. Let's*** [***connect***](https://www.linkedin.com/in/mrunankpawar/) ***and stay tuned for more such content.***