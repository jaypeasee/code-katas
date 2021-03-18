# Move Vowels

## Details:
* <b>Level:</b> 7
* [Code Wars Kara](https://www.codewars.com/kata/56bf3287b5106eb10f000899/javascript)

## The Brief:
Given a string as input, move all of its vowels to the end of the string, in the same order as they were before. Vowels are (in this kata): a, e, i, o, u

## My Solution:
```javascript
const moveVowel = (string) => {
  let separatedVowels = []
  const separatedConsanants = string.split('').filter(char => {
    const vowels = ['a','e','i','o','u']
    vowels.includes(char.toLowerCase()) ? separatedVowels.push(char) : null
    return !vowels.includes(char.toLowerCase())
  })
  return [...separatedConsanants, ...separatedVowels].join('')
}

moveVowel("Apple")
```



