# Find the Stray

## The Brief:
You are given an odd-length array of integers, in which all of them are the same, except for one single number. Complete the method which accepts such an array, and returns that single different number. The input array will always be valid! (odd-length >= 3)

## My Solution:
```javascript
const findStray = (numbers) => {
  const numOccurrances = numbers.reduce((numSums, num) => {
    !numSums[num] ? numSums[num] = 1 : numSums[num] += 1
    return numSums
  }, {})
  
  const strayNum = Object.keys(numOccurrances).find(num => {
    return numOccurrances[num] === 1
  })
  
  return parseInt(strayNum)
}

findStray([1, 1, 2])
```
