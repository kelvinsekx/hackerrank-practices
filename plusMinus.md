[[Given an array of integers, calculate the ratios of its elements that are positive, negative, and zero. 
Print the decimal value of each fraction on a new line with `6` places after the decimal.

Note: This challenge introduces precision problems. 
The test cases are scaled to six decimal places, though answers with absolute error of up to  are acceptable.
Example
There are  elements, two positive, two negative and one zero. Their ratios are ,  and . Results are printed as:](https://www.hackerrank.com/challenges/one-week-preparation-kit-plus-minus/problem?h_l=interview&isFullScreen=true&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-one)](https://www.hackerrank.com/challenges/one-week-preparation-kit-plus-minus/problem?h_l=interview&isFullScreen=true&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-one)


## Answer
```js
function plusMinus(arr) {
  let positive = [], negative = [], zero = [], newArr = [...arr];
  for(let x = 0; x < newArr.length; x++){
      if(newArr[x] > 0){
          positive.push(newArr[x])
      }else if (newArr[x] === 0){
          zero.push(newArr[x])
      }else{
          negative.push(newArr[x])
      }
  }
  console.log((positive.length/arr.length).toFixed(6))
  console.log((negative.length/arr.length).toFixed(6))
  console.log((zero.length/arr.length).toFixed(6))
}
```

### Highlights
- learnt toFixed is used for getting number of decimal roundoffs. E.g (3).toFixed(2) would return 3.00
