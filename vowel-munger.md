# Vowel Munger

## Details:
This was a code challenge I received in an interview.

## Brief:
Write a function that accepts a single string parameter and replaces all the vowels [a,e,i,o,u] with their respective positions within that string. Consider the string 1-indexed, IE, the first position in the string is position 1

## My Solution
```javascript
const vowelMunger = (phrase) => {
  const vowels = ['a','e','i','o','u']
  let updatedLetters = []
  let letters = phrase.split('')
  for (let i = 0; i < letters.length; i++) {
    if (vowels.includes(letters[i].toLowerCase())) {
      updatedLetters.push([i + 1].toString())
    } else {
      updatedLetters.push(letters[i])
    }
  }
  return updatedLetters.join('')
}

vowelMunger('ChOcolate is very vEry tasty.')
```

