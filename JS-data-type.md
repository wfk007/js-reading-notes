# 数据类型

## 五种基本数据类型+Object

- Undefined
- Null
- Boolean
- Number
- String
- **Object**

## typeof 操作符

- Undefined->undefined
- **Null->object**
- Boolean->boolean
- Number->number
- String->string
- Object->object
- Function->fucntion

## Undefined 类型


- Undefined 类型只有一个值，在使用 var 声明变量，但未对其加以初始化时，这个变量值就是 undefined
- **在对未初始化的变量执行 typeof 操作会返回undefined，对未声明的变量执行 typeof 操作同样返回undefined**

## Null 类型


- Null类型是第二个只有一个值的类型，表示一个对象的空指针。

```js
var car = null;
alert(typeof car); // "object"
alert(null == undefined); //true
```

## Boolean 类型

- 该类型只有两个值：true,false(且区分大小写)。true不一定等于1，false不一定等于0

其他类型转换成Boolean：Boolean()

- String：任何非空字符串->true；""->false
- Number：任何非 0 数字（包括无限大）->true；0和NaN->false
- Object：任何对象->true；null->false


## Number 类型


- 任何涉及 NaN 的操作都会返回 NaN。NaN 与任何值都不相等，包括自身

非数值转换成数值：

- Number()

  - Boolean 的 true 和 false 将分别被转换成1,0
  - 数字值，简单的传入和返回
  - null，返回 0
  - undefined，返回 NaN
  - 字符串：字符串为空，返回 0、只包含数字，返回十进制数、包含十六进制格式，转换成十进制数、**包含除上述外的字符，返回NaN**
  - 对象：调用对象的 valueOf() 方法，然后依照前面的规则转换返回的值。如果转换的结果是 NaN，则调用对象的 toString() 方法，然后再次依照前面的规则转换返回的字符串值

- parseInt()：在转换字符串时，更多的是看其是否符合数值模式。它会忽略字符串前面的空格，直至找到第一个非空格字符。**如果第一个字符不是数字字符或者负号， parseInt() 就会返回 NaN**（""会返回 NaN，而Number() 则会返回 0）

- parseFloat()：同 parseInt()

## String 类型


- ECMASCcript 中的字符串不可变

其他值转换成 String

- 使用几乎每个值都有的 toString() 方法。但 null 和 undefined 没有这个方法
- 使用转型函数 String()
  - 如果该值有 toString() 方法，则调用该方法，返回结果
  - null 返回 null
  - undefined 返回 undefined

## Object 类型


Object 的每个实例都具有下列属性和方法：

- constructor：保存用于创建当前对象的函数
- hasOwnProperty(propertyName)：用于检查给定的属性在当前对象实例中（而不是在实例的原型中）是否存在，propertyName 必须以字符串形式给出
- isPrototypeOf(object1)：检查对象是否在 object1 对象的原型链中(**与 instanceof 区分**)
- propertyIsEnumerable(propertyName)：检查给定属性是否能够使用 for-in 语句
- toLocaleString()
- toString()
- valueOf()



