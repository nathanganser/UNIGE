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
  
def sqrt(x: Double) = {  
  def isGoodEnough(guess: Double): Boolean =  
  if (abs(x - guess*guess) / x < 0.00000000000001) true else false  
  
 def improve(guess: Double): Double =  
  (x/guess + guess)/2  
  
  def sqrtIter(guess: Double): Double =  
  if (isGoodEnough(guess)) guess else  
  sqrtIter(improve(guess))  
  
  sqrtIter(1)  
}  
  
sqrt(0.0004)
```

## Greatest common denominator
```
def gcd(a: Int, b: Int): Int =  
  if (b ==0) a else gcd(b, a % b)
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM0MDI0MzgxNCwtNjE0MjAyMDQ2LC0xNj
U1NTUzMTMsLTEzNTgyOTYzMTAsMTgxMzE3MzE2MCw5MjE1Mzc4
ODRdfQ==
-->