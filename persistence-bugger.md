# Persistence Bugger

## Details:
* <b>Level:</b> 6
* [Code Wars Kata](https://www.codewars.com/kata/55bf01e5a717a0d57e0000ec/javascript)

## The Brief:
Write a function that takes in a positive parameter num and returns its multiplicative persistence, which is the number of times you must multiply the digits in num until you reach a single digit.

## My Solution:
```javascript
const calculateRounds = (num, rounds = 0) => {
  if (num > 9) {
    const numsMultiplied = num.toString().split('').reduce((outcome, num) => {
      outcome = outcome * num
      return outcome
    }, 1)
    return calculateRounds(numsMultiplied, rounds + 1)
  } else {
    return rounds
  }
}

calculateRounds(39)
```


