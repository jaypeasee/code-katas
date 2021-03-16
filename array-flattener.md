# Array Flattener

## Details:
This was a code challenge assigned at Turing in Mod 4.

## Brief:
Create a function with the input of an array, will always return a non nested array. Some inputs may have arrays within arrays. You must do this without any built in methods, such as `.flat().` It must also be solved using recursion.

## My Solution:
```javascript
const flattenTheArray = (arrayToEval) => {
  let nestedCount = 0
  const updatedArray = arrayToEval.reduce((updateProgress, element) => {
    if (typeof element === 'object') {
      element.forEach(arrayElement => {
        updateProgress.push(arrayElement)
        nestedCount += 1
      })
    } else {
      updateProgress.push(element)
    }
    return updateProgress
  }, [])
  return nestedCount ? flattenTheArray(updatedArray) : updatedArray
}

flattenTheArray([ 0, 1, 2, [ 3, 4 ], [[4, 5, 6], []] ])
```

