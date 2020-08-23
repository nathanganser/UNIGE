## Functions
### Simple function
``` 
def square(x: Double) = x * x
```
### Function Inception
``` 
def sumOfSquare(x: Double, y: Double) = square(x) + square(y)
```
### If example
``` 
def abs(x: Int) = if (x >= 0) x else -x
```
## && in Scala
if you replace `y: Boolean` by `y: => Boolean` it will become a `call by name` parameter and only evaluated when called (and not when created)
``` 
def and(x: Boolean, y: Boolean) = if (x) y else false
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzNTgyOTYzMTAsMTgxMzE3MzE2MCw5Mj
E1Mzc4ODRdfQ==
-->