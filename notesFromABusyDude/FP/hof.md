Higher-Order Function is a function that does at least one of the following:

- takes one or more functions as arguments,
- returns a function as its result.

### Example:
formatResult - hof
```scala
private def formatAbs(x: Int) =
    val msg = "The absolute value of %d is %d."
    msg.format(x, abs(x))

private def formatFactorial(n: Int) =
    val msg = "The factorial of %d is %d."
    msg.format(n, factorial(n))

def formatResult(name: String, n: Int, f: Int => Int) =
	val msg = "The %s of %d is %d."  
	msg.format(name, n, f(n))
```

Call func formatResult:
```scala
formatResult("absolute value", -42, abs)
val res0: String = "The absolute value of -42 is 42."

formatResult("factorial", 7, factorial)
val res1: String = "The factorial of 7 is 5040."
```
