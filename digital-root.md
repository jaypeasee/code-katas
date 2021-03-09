# Digital Root

## The Brief:
Digital root is the recursive sum of all the digits in a number.

Given n, take the sum of the digits of n. If that value has more than one digit, continue reducing in this way until a single-digit number is produced. The input will be a non-negative integer.

## My Solution:
```javascript
function digital_root(n) {
  if (n > 9) {
    const total = n.toString().split('').reduce((sum, num) => {
      sum += parseInt(num)
      return sum
    }, 0)
    return digital_root(total)
  } else {
    return n
  }
}

digital_root(16)
```



