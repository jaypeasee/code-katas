# Find the Stray
You are given an odd-length array of integers, in which all of them are the same, except for one single number. Complete the method which accepts such an array, and returns that single different number. The input array will always be valid! (odd-length >= 3)

```javascript
const stray = (numbers) => {
  const numOccurrances = numbers.reduce((numDetails, num) => {
    !numDetails[num] ? numDetails[num] = 1 : numDetails[num] += 1
    return numDetails
  }, {})
  
  const numberKey = Object.keys(numOccurrances).find(numKey => {
    return numOccurrances[numKey] === 1
  })
  
  return parseInt(numberKey)
}

stray([1, 1, 2])
```
