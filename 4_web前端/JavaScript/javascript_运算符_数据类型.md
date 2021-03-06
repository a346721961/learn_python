## 运算符

### 算术运算符

| 运算符 | 描述                 | 例子  | x运算结果 | y运算结果 |
| ------ | -------------------- | ----- | --------- | --------- |
| +      | 加法                 | x=y+2 | 7         | 5         |
| -      | 减法                 | x=y-2 | 3         | 5         |
| *      | 乘法                 | x=y*2 | 10        | 5         |
| /      | 除法                 | x=y/2 | 2.5       | 5         |
| %      | 取模（余数）         | x=y%2 | 1         | 5         |
| ++     | 自增（先赋值再自增） | x=++y | 6         | 6         |
| ++     | 自增（先自增再赋值） | x=y++ | 5         | 6         |
| --     | 自减（先赋值再自减） | x=--y | 4         | 4         |
| --     | 自减（先自减再赋值） | x=y-- | 5         | 4         |

```javascript
var x = 1;
alert(x++);  // 1  先打印，再加1  
alert(++x);  // 3  先加1，再打印  
alert(--x);  // 2  先减1，再打印  
alert(x--);  // 2  先打印，再减1  
```

### 一元加减法

```javascript
var a = "3";
b =+ a;
alert(b);  // 3
alert(typeof(b));  // number

var c = "3.2";
d =- c;  // 此处-号表示负号
alert(d);  // -3.2
alert(typeof(d));  // number

var m = "123a456";
n =+ m;
alert(n);  // NaN，字符串类型转化成数字类型失败
alert(typeof(n));  // number

var j = "a456";
k =+ j;
alert(k);  // NaN
alert(typeof(k));  // number
```

### 逻辑运算符

| 运算符 | 描述          | 例子（x = 6，y = 3）        |
| ------ | ------------- | --------------------------- |
| &&     | and（并且）   | (x < 10 && y > 1)为true     |
| \|\|   | or（或者）    | (x == 5 \|\| y == 5)为false |
| ！     | not（非，不） | !(x == y)为true             |

注意：

-   如果一个运算数是对象，另一个是Boolean值，则返回该对象；
-   如果两个运算数都是对象，则返回第二个对象；
-   如果某个运算数是null，返回null；
-   如果某个运算数是NaN，则返回NaN；
-   如果某个运算数是undefined，返回undefined。

### 比较运算符

| 运算符 | 描述                       | 比较（x = 5） | 返回值 |
| ------ | -------------------------- | ------------- | ------ |
| ==     | 等于（仅值相等即可）       | x == 8        | false  |
|        |                            | x == "5"      | true   |
| ===    | 绝对等于（值和类型均相等） | x === 5       | true   |
|        |                            | x === "5"     | false  |
| !=     | 不等于                     | x != 8        | false  |
| !==    | 绝对不相等                 | x !== "5"     | true   |
|        |                            | x !== 5       | false  |
| >      | 大于                       | x > 8         | false  |
| <      | 小于                       | x < 8         | true   |
| >=     | 大于或等于                 | x >= 8        | false  |
| <=     | 小于或等于                 | x <= 8        | true   |



## 基本数据类型

-   **Number** 数字型（包括整型、浮点型）
-   **Null** 空型
-   **String** 字符串型
-   **Boolean** 布尔型（true，false）
-   **Undefined** 未定义型

**注意：**

-   当字符串转换成数字失败时就是NaN；
-   NaN数据在表达式中结果一定为false，除了 **!=** ；
-   Undefined：如果声明了一个变量，但是没有赋值，则变量是Undefined类型。
-   Null：占一个**对象**的位置。

**其他使用：**

```javascript
var obj = null;  // 创建一个对象变量，只是现在还没对象进行赋值，所以用Null站位。

var obj = new Animal();  // 后面再把对象赋值给obj这个对象变量。
```

```javascript
parseInt(3.14)  // 把浮点型数字转换成整型
typeof("hello")  // 打印数据的数据类型
```

