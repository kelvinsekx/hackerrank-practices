# hackerrank-practices 
## Grinding Day 02
This repo is an open solution to share my 100 days of hackerrank problem tackle.
It does not only show my solutions, it also states hints and highlights of what I learnt while solving or what may need extra exposure.


### Latest solution was 5:52am WAT (solution to converting to military time)
```js
function timeConversion(s) {
  if(s.slice(-2) === 'AM'){
    return `0${parseInt(s.slice(0, 2)) - 12}` + s.slice(2, 8)
  }else{
     return `${(parseInt(s.slice(0, 2)) !== 12) ? 
     parseInt(s.slice(0, 2)) + 12 : 12 }` + s.slice(2, 8) 
  }
}
```
