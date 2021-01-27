# 数据类型
1. 数字number
2. 字符串string
3. 布尔bool
4. 符号symbol
5. 空undefined
6. 空null
7. 对象object

## 数字number
由64位浮点数组成。+0和-0不一样
*无穷大*infinity/+infinity/-infinity。无法表示的数字用NaN表示


### 范围（忽略符号位）
1. 指数拉满、有效数字拉满，得到最大二进制数字
2. Number.MAX_VALUE: 1.7976931348623157e+308
3. 指数负方向拉满、有效数字最小1，得到最小值
4. Number.MIN_VALUE: 5e-324
### 精度（有效数字）
1. 最多只能到52+1个二进制位表示有效数字
2. 2^53 对应的十进制是 9 后面 15 个零
3. 所以15位有效数字都能精确表示
4. 16位有效数字如果小于 90 开头，也能精确表示
5. 9110000000000001 就存不下来


## 字符串string  
### 单引号
'你好'
### 双引号
"你好"
### 反引号
`你好`
### 注意
引号不属于字符串的一部分，就像书名号不属于书名的一部分一样
### 错误写法
'it's ok' 
JS 引擎会认为 'it' 就结束了，后面的看不懂
### 正确写法
1. 'it\'s ok'  // 这就是转义
2. "it's ok"
3. `it's ok`

### 转义用另一种写法表示你想要的东西
1. \' 表示 '
2. \" 表示 "
3. \n 表示换行
4. \r 表示回车
5. \t 表示 tab 制表符
6. \\ 表示 \
7. \uFFFF 表示对应的 Unicode 字符
8. \xFF 表示前 256 个 Unicode 字符


## 布尔 boolean
if 语句常常需要判断真假
if( value ) { ... } else { ... }
### 五个 falsy 值
1. undefined 
2. null 
3. 0 
4. NaN 
5. ''**是空字符串，没有空格**

## undefined 和 null
1. 细节一:如果一个变量声明了，但没有赋值，那么默认值就是 undefined，而不是 null
2. 细节二:如果一个函数，没有写 return，那么默认 return undefined，而不是 null
3. 细节三:前端程序员习惯上，把非对象的空值写为 undefined，把对象的空值写为 null
但仅仅是习惯上而已

## 变量声明
1. var a = 1 var 是过时的、不好用的方式
2. let a = 1 let 是新的，更合理的方式
3. const a = 1是声明时必须赋值，且不能再改的方式
### let
1. 遵循块作用域，即使用范围不能超出 { }
2. 不能重复申明
3. 可以赋值，也可以不赋值
4. 必须先声明再使用，否则报错
5. 全局声明的 let 变量，不会变成 window 的属性
6. for 循环配合 let 有奇效

### const
1. 跟 let 几乎一样
2. 只有一条不一样：声明时就要赋值，赋值后不能改

### name 和 'name' 的区别
1. name 是变量
值可变，可能是 'name'，也可能是 'hello'
2. 'name' 是字符串常量
常量就是不变量
'name' 只能是 'name'，不能是其他值
### 类型转换
* number => string
String(n)
n + ''
* string => number
Number(s)
parseInt(s) / parseFloat(s)
s - 0
* x => bool
Boolean(x)
!!x
* x => string
String(x)
x.toString()








