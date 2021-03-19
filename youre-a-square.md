# You're A Square!

## Details:
* <b>Level:</b> 7
* [Code Wars Kata](https://www.codewars.com/kata/54c27a33fb7da0db0100040e/javascript)

## The Brief:
In mathematics, a square number or perfect square is an integer that is the square of an integer; in other words, it is the product of some integer with itself. Given an integral number, determine if it's a square number. 

## My Solution:
```javascript
const checkSquared = (numToEval) => {
  for (let i = 0; i < numToEval + 1; i++) {
    if (i * i === numToEval) {
      return true
    }
  }
  return false
}

checkSquared(25)
```



