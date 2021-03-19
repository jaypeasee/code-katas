# Find the Max Min and Average

## Details:
This is a code challenge a friend sent me after an interview she had.

## The Brief:

Taking in a string, return an array of numbers where the first value is the biggest, the second value is the smallest, and the third value is the average.

## My Solution:
```javascript
const findMaxMinAvg = (string) => {
  let minMaxAvg = []
  const sortedNums = string.replaceAll(',', '').split('').sort((num1, num2) => {
    return num2 - num1
  })
  
  const sum = sortedNums.reduce((total, num) => {
    total += parseInt(num)
    return total
  }, 0)
  
  minMaxAvg.push(parseInt(sortedNums[0]))
  minMaxAvg.push(parseInt(sortedNums[sortedNums.length - 1]))
  minMaxAvg.push(Math.round(sum / sortedNums.length))
  return minMaxAvg
}
                                                      
findMaxMinAvg("7,1,5,3,2,4,8,6,10,9")
```

