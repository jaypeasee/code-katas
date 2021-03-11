# Digital Root

## Details:
* Level: 6
* [Code Wars Kata](https://www.codewars.com/kata/541c8630095125aba6000c00)

## The Brief:
Digital root is the recursive sum of all the digits in a number.

Given n, take the sum of the digits of n. If that value has more than one digit, continue reducing in this way until a single-digit number is produced. The input will be a non-negative integer.

## My Solution:
```javascript
function getDigitalRoot(number) {
  if (number > 9) {
    const total = number.toString().split('').reduce((sum, digit) => {
      sum += parseInt(digit)
      return sum
    }, 0)
    return getDigitalRoot(total)
  } else {
    return number
  }
}

getDigitalRoot(16)
```



