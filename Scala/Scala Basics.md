## Functions
### Simple function
``` 
def square(x: Double) = x * x
```
### Function Inception
``` 
def sumOfSquare(x: Double, y: Double) = square(x) + square(y)
```
### If
``` 
def abs(x: Int) = if (x >= 0) x else -x
```
``` 
def and1(x: Boolean, y: Boolean) = if (x) if (y) true else false else false
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTQxMzk3MzM2Niw5MjE1Mzc4ODRdfQ==
-->