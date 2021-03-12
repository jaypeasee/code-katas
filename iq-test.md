# IQ Test

## Details:
* <b>Level:</b> 6
* [Code Wars Kata](https://www.codewars.com/kata/552c028c030765286c00007d/javascript)

## The Breif:
Among the given numbers finds one that is different in evenness, and return a position of this number. <b>Note:</b> index positions from lists start at 1 (not 0).

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



