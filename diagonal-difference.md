Given a square matrix, calculate the absolute difference between the sums of its diagonals

https://www.hackerrank.com/challenges/one-week-preparation-kit-diagonal-difference/problem?h_l=interview&isFullScreen=true&playlist_slugs%5B%5D%5B%5D=preparation-kits&playlist_slugs%5B%5D%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D%5B%5D=one-week-day-two&h_r=next-challenge&h_v=zen

## Answer
```js
function diagonalDifference(arr) {
    let reductor = arr.length - 1
   const leftToRight = arr.reduce(
        (acc, presentArr, index)=> acc + presentArr[index],
        0
    )
    const rightToLeft = arr.reduceRight(
        (acc, presentArr, index )=> {
            return acc + presentArr[reductor - index]
        },
        0
    )
    return Math.abs(leftToRight - rightToLeft)
}
```

## Highlights
- Math.abs returns the absolute value of a number. The absolute value of -12 is 12, 10 is 10 etc. It simply returns the number leaving the symbol.
[learn more about Math.abs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/abs)
- to get the reverse index value of reduceRight is to return `index - (lengthOfArr - 1)`
