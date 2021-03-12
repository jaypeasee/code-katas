# IQ Test

## Details:
* <b>Level:</b> 6
* [Code Wars Kata](https://www.codewars.com/kata/552c028c030765286c00007d/javascript)

## The Breif:

Bob is preparing to pass IQ test. The most frequent task in this test is to find out which one of the given numbers differs from the others. Bob observed that one number usually differs from the others in evenness. Help Bob — to check his answers, he needs a program that among the given numbers finds one that is different in evenness, and return a position of this number.

<b>Note:</b> Keep in mind that your task is to help Bob solve a real IQ test, which means indexes of the elements start from 1 (not 0)

## My Solution:
```javascript
const findUniquePosition = (numbers) => {
  let uniqueNum
  const numsPattern = numbers.split(' ')
  const numTypes = numsPattern.reduce((totals, num) => {
    parseInt(num) % 2 === 0 ? totals.evens.push(num) : totals.odds.push(num)
    return totals
  }, {odds: [], evens: []})
  uniqueNum = numTypes.odds.length === 1 ? numTypes.odds[0] : numTypes.evens[0]
  for (let i = 0; i < numsPattern.length; i++) {
    if (numsPattern[i] === uniqueNum) {
      return i + 1
    }
  }
}

findUniquePosition("5 3 2")
```



