# 算法

## 冒泡排序

## 选择排序

## 插入排序

## 数组去重

- 利用ES6的Array.from()或者扩展运算符 以及 Set
``` JavaScript
  Array.from(new Set(arr))
```
``` JavaScript
  [...new Set(arr)]
```

- 遍历数组，建立新数组，利用indexOf判断是否存在于新数组中
``` JavaScript
  function unique(arr) {
    let newArr = []
    for (let i in arr) {
      if (newArr.indexOf(arr[i]) === -1) {
        newArr.push(arr[i])
      }
    }
    return newArr
  }
```

- 遍历数组，利用Object对象的key值保存数组值，key值唯一
``` JavaScript
  function unique(arr) {
    let newArr = []
    let obj = {}
    for (let i in arr) {
      let item = arr[i]
      if (obj[item] !== 1) {
        obj[item] = 1
        newArr.push(item)
      }
    }
    return newArr
  }
```

- 先排序，然后遍历排序后的数组并push到新数组，判断最后一个元素是否相同
``` JavaScript
  function unique(arr) {
    let newArr = []
    arr.sort()
    for (let i in arr) {
      let item = arr[i]
      if (newArr[newArr.length - 1] !== item) {
        newArr.push(item)
      }
    }
    return newArr
  }
```
