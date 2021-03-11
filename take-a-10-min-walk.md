# Take A Ten Minute Walk

## Details:
* <b>Level:</b> 6
* [Code Wars Kata](https://www.codewars.com/kata/54da539698b8a2ad76000228/javascript)

## The Brief:
You live in a city where all roads are laid out in a perfect grid. You arrived ten minutes too early to an appointment, so you decided to take a short walk. You have a Walk Generating App on your phone -- everytime you press the button it sends you an array of one-letter strings representing directions to walk (eg. ['n', 's', 'w', 'e']). You always walk only a single block for each letter (direction) and you know it takes you one minute to traverse one city block.

Create a function that will return true if the walk the app gives you will take you exactly ten minutes (you don't want to be early or late!) and will, of course, return you to your starting point. Return false otherwise.

<b>Note:</b> you will always receive a valid array containing a random assortment of direction letters ('n', 's', 'e', or 'w' only). It will never give you an empty array (that's not a walk, that's standing still!).

## My Solution:
```javascript
const checkValidWalk = (directions) => {
  const walkCoordinates = directions.reduce((totals, direction) => {
    !totals[direction] ? totals[direction] = 1 : totals[direction] +=1
    return totals
  }, {})
  if (directions.length === 10 && walkCoordinates.n === walkCoordinates.s 
      && (walkCoordinates.w === walkCoordinates.e || 
      walkCoordinates.w - walkCoordinates.e === 3 || 
      walkCoordinates.e - walkCoordinates.w === 3)) {
    return true
  }
  return false
}

checkValidWalk(['w', 'e', 'w', 'e', 'w', 'e', 'w', 'e', 'w', 'e', 'w', 'e'])
```



