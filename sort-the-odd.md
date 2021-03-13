# Sort The Odd

## Details:
* <b>Level:</b> 6
* [Code Wars Kata](https://www.codewars.com/kata/578aa45ee9fd15ff4600090d/javascript)

## The Brief:
You will be given an array of numbers. You have to sort the odd numbers in ascending order while leaving the even numbers at their original positions.

## My Solution:


```javascript
const sortOdds = (nums) => {
  let rearrangedNums = []
  const sortedOdds = nums.reduce((odds, num) => {
    if (num % 2 === 0) {
      rearrangedNums.push(num)
    } else {
      rearrangedNums.push('odd')
      odds.push(num)
    }
    return odds
  }, []).sort((num1, num2) => num1 - num2)
  return rearrangedNums.map(num => {
    sortedOdds.forEach(odd => {
      if (num === "odd") {
        num = odd
        sortedOdds.shift()
      }
    })
    return num
  })
}

sortOdds([5, 3, 2, 8, 1, 4])
```