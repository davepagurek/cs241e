# cs241e
A compiler to convert a subset of Scala into MIPS assembly.

Due to this being a project for a school course, the code is no longer available publicly. <a href="mailto:davepagurek@gmail.com">Send me an email</a> if you are not currently taking CS241e and want to see the source code.

## Features
Using tail recursion and closures, the following code works:
```scala
def main(a: Int, b: Int): Int = {
  lotsOfIncreasing(a, b)
}
def increaseBy(increment: Int): (Int)=>Int = {
  def procedure(a: Int): Int = { a + increment }
  procedure
}
def lotsOfIncreasing(x: Int, i: Int): Int = {
  if (i < 10) {
    increaseBy(i);
    lotsOfIncreasing(x, i+1)
  } else {
    x
  }
}
```
