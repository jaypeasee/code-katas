# Multiples of 3 or 5

## Details:
* <b>Level:</b> 6
* [Code Wars Kata](https://www.codewars.com/kata/514b92a657cdc65150000006/javascript)

## The Brief:
Create a function that returns the sum of all the multiples of 3 or 5 of the number passed in.

<b>Note:</b> If the number is a multiple of both 3 and 5, only count it once. Also, if a number is negative, return 0(for languages that do have them)

## My Solution:
```javascript
const addMultiples = (number) => {
  let sum = 0
  for (let i = 0; i < number; i++) {
    i % 3 === 0 || i % 5 === 0 ? sum += i : sum += 0
  }
  return sum
}

addMultiples(10)
```

