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
      let ele = arr[i]
      if (obj[ele] !== 1) {
        obj[ele] = 1
        newArr.push(ele)
      }
    }
    return newArr
  }
```
