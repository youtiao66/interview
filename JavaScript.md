## 数据类型

### 6种原始类型（`primitive`）

- `Boolean`
- `Null`
- `Undefined`
- `Number`
- `String`
- `Symbol`

### 对象（`Object`）

## `typeof`

| 类型 | 结果 |
| --- | --- |
| `Boolean` | `"boolean"` |
| **`Null`** | **`"object"`** |
| `Undefined` | `"undefined"` |
| `Number` | `"number"` |
| `String` | `"string"` |
| `Symbol` | `"symbol"` |
| `Function` | `"function"` |
| 其他任何对象 | `"object"` |

``` js
  typeof null === "object"
  typeof function() {} === "function"
  typeof [] === "object"
```

``` js
  Object.prototype.toString.call(xx) === "[object Type]"
```
