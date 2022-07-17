Given five positive integers, find the minimum and maximum values that can be calculated by summing exactly four of the five integers. 
Then print the respective minimum and maximum values as a single line of two space-separated long integers.

https://www.hackerrank.com/challenges/one-week-preparation-kit-mini-max-sum/problem?h_l=interview&isFullScreen=true&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-one&h_r=next-challenge&h_v=zen

## Answer
```js
function miniMaxSum(arr) {
    arr = arr.sort().reverse()
    const minimum = arr.slice(0, 4)
    const max = arr.slice(-4)
    
    const addUp = (array)=>array.reduce((a,b)=> a + b)
    console.log(addUp(max), addUp(minimum))
}
```

## Highlights
- Array.sort sorts an array of integer from highest to lowest (not lowest to highest).
- Array.slice when given a negative integer without a second argument returns the (number of interger) 
last elements of the array. e.g slice(-3) returns the ast 2 elements.
