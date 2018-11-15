
### 浏览器 11111
#### 渲染内核
webkit app 开发 Safari 以前的chrome
chromeium/Blink 现在的 chrome浏览器/欧朋浏览器
Trident 早期IE浏览器内核
Edge内核，现在的IE浏览器内核
gecko 火狐浏览器内核

国内大部分浏览器 和手机浏览器都是用的webkit/Blink 内核
双核浏览器 就是一个webkit/Blink内核，一个IE浏览器的内核

#### JS内核
V8引擎 Google自己开发的JS内核

### 编程语言
css  层叠样式表
html 超文本标记语言
编程得有自己的思想，比如面向对象/面向过程
- 面向对象
- - java
- - php
- - c++
- - JavaScript
- 面向过程
- - c

### JS组成
> 1.ECMAScript
> 2.DOM （ Document Object Model ）文本对象模型
> 3.BOM （ Browser Object Model ）浏览器对象模型

### js引入
通过script 标签
- 内嵌式
- 外链式/引入式

### 变量
> 变量不是一个值，只是一个容器，存储我们的值，这个值是可以改变的，所以称之为变量 variable
[语法]
1.var 变量名 = 值;
2.function 函数名(){} //函数名也是变量名
3.let 变量名 = 值;
4.const 变量名 = 值;

#### 变量名的命名规则
1.驼峰命名 多个英文单词命名的变量，从第二个单词开始首字母需要大写
2.可用 a-z A-Z 0-9 _ $ 组成变量名 
3.关键字 保留字 不能用
4.强英文语义化（方便开发人员维护 规范 不会报错），
语义化 是给seo 搜索引擎看的
5.区分大小写

### 数据类型 5种
- 基本数据类型
- - String 字符串
- - Number 数字
- - Boolen 布尔值
- - Null 空对象指针--不占用内存
- - Undefined 空（ 为定义/未找到 ）

- 引用数据类型
- - Object 对象
- - - 普通对象（object）、数组[arr]、正则、时间对象
- - function 函数
引用类型的数据 都可以动态添加属性

`基本数据类型`
> 1.String（字符串） 用单引号或者双引号包裹零到多个字符
```javascript
var name = "lijunshuang";
var age = "18";
```
> 2.number（数字） 就是普通的数字和NaN
```javascript
var age = 18;
var ageNaN = 18 - "ljs"; //NaN   not a number   是number类型
```
> 3.Boolen (布尔值) true/false
```javascript
var true1 = true;
var false1 = false;
```
`引用数据类型`
> 1.普通对象 用 { } 大括号报起来的零到多个内容 {} 空对象
> 2.数组 用中括号[]包起来的零到多个内容  []空数组
> 数组 没有可见的属性吗 但是它有他的属性名 叫做 index 索引
> 数组索引从0开始，最大索引为数组长度 length-1

> 3.函数 function fn(){}

### 输出内容
> 1.console.log()  //日志输出，可以输出多项，以逗号隔开
> 2.console.dir() //详细日志输出， 输出DOM更详细
> 3.console.table() // 把json数据展示成一个表格
> 4.alert()  弹窗输出
> 5.document.write() // 向页面输出内容--不常用
...自己扩展

##数据类型详解

### Number详解

#### 将其他数据类型转换成 number类型
方法：Number()
```javascript
var str= "18";
var num = Number(str);
console.log(num,'>>>','18') // 输出 18 ">>>" "18"
```
#### 字符串转成number类型
> 1.如果字符串的字符是一个有效数字，转换后的结果就是这个有效数字
> 2.如果字符串的字符不是一个有效数字，结果是NaN
> 3.如果是空字符串
```javascript
var num = Number('18');//18
var num2 = Number('ljs'); // NaN
var num3 = Number('18ljs');// NaN
var num3 = Number('-12.5'); // -12.5
var num4 = Number('12.5'); // 12.5
var num5 = Number(''); // 0

var str1 = '18';
console.log(+str1);// 18
console.log(Number(str1)) // 18
var str2 = 'hello';
console.log(+str2);// NaN
console.log(Number(str2)) // NaN
```




