# GiaiBaiTapJS
Bai 0:
```
Array.prototype.myMap = function (callbackFn) {
    const arr = []
    for (let index = 0; index < this.length; index++) {
        arr.push(callbackFn(this[index], index, this))
    }
    return arr
}
```
```
Array.prototype.myFiler = function (callbackFn) {
    const arr = []
    for (let index = 0; index < this.length; index++) {
        if (callbackFn(this[index], index, this)) {
            arr.push(this[index])
        }

    }
    return arr
}
```
```

Array.prototype.myReduce = function (callBack, initValue) {
    let index = 1

    if (initValue) {
        index = 0
    }
    else {
        initValue = this[0]
    }
    for (; index < this.length; index++) {
        initValue = callBack(initValue, this[index],index, this)
    }
    return initValue
}
```

bài 1:
```
const answer = array1.filter(
    (item1) => array2.some((item2) => item2 === item1)

)
```
Bài 2:
```
firstArr.sort();
console.log([firstArr[firstArr.length - 1], firstArr[firstArr.length - 2]])
```
Bài 3:
```
const answer = arr.reduce((accValue, currentValue, index) => {
    if (arr.includes(sum - currentValue, index + 1)) {
        accValue.push([currentValue, sum - currentValue])
    }
    return accValue
}, [])
```
Bai 4
```
const newArr = new Set()
for (const item of firstArr) {

    newArr.add(item)
}

const result = []
for (const item of newArr) {
    result.push(item)
}
```
bài 5:
```
const arr = []
for (const arr1item of arr1) {
    for (const arr2item of arr2) {
        if (arr1item === arr2item) {
            if (!arr.includes(arr1item)) {
                arr.push(arr1item)
            }
            break;
        }
    }
}
```
bài 6:
```
const returnObj = arr.reduce((accValue, currentValue) => {
    if (currentValue in accValue) {
        accValue[currentValue] += 1;
    }
    else {
        accValue[currentValue] = 1
    }

    return accValue
}, {})
```
bài 7:
```
const returnObj = arr.reduce((accValue, currentValue) => {
    if (currentValue.make in accValue) {
        accValue[currentValue.make].push(currentValue)
    }
    else {
        accValue[currentValue.make] = [currentValue]
    }

    return accValue
}, {})
```
bài 8:
```
const newArr = order.cart.reduce((accValue, currentValue) => {

    return {
        total_money: accValue.total_money + currentValue.price * currentValue.amount,
        total_amount: accValue.total_amount + currentValue.amount
    }
}, { total_amount: 0, total_money: 0 })

```


