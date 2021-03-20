# Fun With Anagrams

## Details:
This was a take-home code challenge on HackerRank that I received for a job interview.

## The Brief:
Create a function that takes in an array of strings and returns an array of strings where there are no consecutive anagrams. If there are anagrams, keep the first one. Return the array in the closest order to the input.

For example:
`['code', 'doce', 'ecod', 'framer', 'frame'] => [ 'code', 'framer', 'frame' ]`

## My Solution:
```javascript
const funWithAnagrams = (words) => {
  let updatedWords = [words[0]]
  for (let i = 1; i < words.length; i++) {
    if (updatedWords[updatedWords.length -1].split('').sort().join('') !==
        words[i].split('').sort().join('')) {
      updatedWords.push(words[i])
    }
  }
    return updatedWords
}

funWithAnagrams(['code', 'doce', 'ecod', 'framer', 'frame'])
```

