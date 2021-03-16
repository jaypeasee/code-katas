# Palindromic Numbers

## Details:
This was a code challenge at Turing during mod 4.

## The Brief:
Identify the first 25 numbers who's reverse plus their own adds up to a palindrome and the number is greater than 1000.

## My Solution:
```javascript
const getPalindromicNums = (numToEval, palindromicNums) => {
  const sum = numToEval + getReversedNum(numToEval)
  const reversedSum = getReversedNum(sum)
  if (reversedSum === sum && sum > 1000) {
   palindromicNums.push(numToEval)
  }
  if (palindromicNums.length === 25) {
    return palindromicNums
  } else {
    return getPalindromicNums(numToEval + 1, palindromicNums)
  }
}

const getReversedNum = (number) => {
  return parseInt(number.toString().split('').reverse().join(''))
}

getPalindromicNums(209, [])
```