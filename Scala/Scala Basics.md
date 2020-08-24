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

## Square root
```
def abs(x: Double) =  
  if (x>0) x else -x  
  
def isGoodEnough(guess: Double, x: Double): Boolean =  
  if (abs(x - guess*guess) / x < 0.00000000000001) true else false  
  
def improve(guess: Double, x: Double): Double =  
  (x/guess + guess)/2  
  
def sqrtIter(guess: Double, x: Double): Double =  
  if (isGoodEnough(guess, x)) guess else  
  sqrtIter(improve(guess, x), x)  
  
def sqrt(x: Double) = sqrtIter(1, x)  
  
sqrt(0.0004)
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2NTU1NTMxMywtMTM1ODI5NjMxMCwxOD
EzMTczMTYwLDkyMTUzNzg4NF19
-->