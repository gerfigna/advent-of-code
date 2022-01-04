# advent-of-code

day one:

https://adventofcode.com/2021/day/1/input
```
const intValues = $('pre').textContent.split("\n").map(x => parseInt(x)).filter(x => !isNaN(x));

values.reduce((previousValue, currentValue, currentIndex, array) => {
    return previousValue += currentIndex > 0 && array[currentIndex-1] < currentValue ? 1 : 0;
}, 0);

```

day two:

https://adventofcode.com/2021/day/1/input
```
const intValues = $('pre').textContent.split("\n").map(x => parseInt(x)).filter(x => !isNaN(x));

const slides = intValues.map((element, index, array) => {
    if(index < array.length - 2){
        return parseInt(element) + parseInt(array[index+1]) + parseInt(array[index+2]);
    }
    return 0;
}).filter(x => x > 0)

const result = slides.reduce((previousValue, currentValue, currentIndex, array) => {
    return previousValue += currentIndex > 0 && array[currentIndex-1] < currentValue ? 1 : 0;
}, 0);

```
