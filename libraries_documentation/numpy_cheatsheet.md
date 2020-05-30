## Numpy
Or called the **Numeric Python** is a library used for performing calculations on arrays.
```python
import numpy as np
arr = np.array([1,2,3,4,5)]
print(type(arr)) # <class 'numpy.ndarray'>
```
Numpy arrays are different from python lists. A np array is created using ```np.array()``` function which takes python list as 
an arguement. The values in the list should be of same data type. Otherwise, numpy will implicitly typecast it to maintain
homogeneity.
```python
a = np.array([1,2,'one'])
print(a) # array(['1', '2', 'one'], dtype='<U11')
b = np.array([1,2,True,3, False,'h'])
print(b) # array([1, 2, 1, 3, 0])
c= np.array([1,2,True,3, False,'h'])
print(c) # array(['1', '2', 'True', '3', 'False', 'h'], dtype='<U11')
```
Filtering data is a one step process here.
```python
a = np.array([1,2,7,2,9,7,5,4,3,2])
b = a>3
print(b) # [False False  True False  True  True  True  True False False]
c = a[a>3]))
print(c, type(c)) # [7 9 7 5 4]  <class 'numpy.ndarray'>
```
Operations to be performed on each element of list value does not require looping.
```python
a= np.array([1,2,3,4,5])
b = a**2
print(b) # [1,2,3,16,25]
c = a+10
print(c) # [11,12,13,14,15]
```
It also supports formation of multi-dimensional arrays. Homogeneity is maintained here as well.
Accessing elements and slicing in np array is same as in python lists, i.e. through square brackets.
```
a=np.array([[1,2],[3,4],[5,6]])
print(a.shape) # (3, 2)
print(a[:,1]) # array([2, 4, 6])
print(a[1,1]) # 4
print(a[2]) # array([5, 6])
```
**.shape** return the dimensions of the array in tuple, where the first element is row and second is column.
Statistics can also be performed using np. Few functions in use are as follows:
```python
a =np.array([12, 34, 23, 92, 76, 54, 76, 83, 91])
print(np.mean(a)) # 60.111111111111114
print(np.median(a)) # 76.0
print(np.std(a)) # 28.695506595378866
b =np.array([32, 45, 63, 78, 91, 67, 87, 20, 52])
print(np.corrcoef(a)) # array([[1., 0.32346095], [0.32346095, 1.]])
```
```.mean() .median() .std() .corrcoef()``` are used to find mean, median, standard deviationand correlation coefficient respectively.
