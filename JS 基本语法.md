

# JS 基本语法

## 表达式与语句

### 表达式

`1 + 2`是表达式

1+2表达式的值是3

add(1,2)表达式的值是函数的返回值

### 语句

`var a = 1`是一个语句

问:

```javascript
console.log(3)
```

上面这句话中,

什么是值?

什么是返回值?

什么是打印出来的东西?

答;

值是 `Undefined`, 因为返回值是`Undefined`, `3`是打印出来的东西

#### 细节

> 只要一个地方不能加回车, 那就是`return` 后面

## JS大小写敏感

记住就行了, 不要写错了

`object` 和 `Object` 是不同的

## 标识符

#### 啥是标识符?

一般就是给变量取名字用的字符

标识符是指变量的合法命名。规则如下：

- 第一个字符，可以是任意Unicode字母（包括英文字母、希腊字母、中文）、下划线(_)、$符号，

- - 不可以是数字开头

- 第二个字符及后面的字符，除了 Unicode 字母、美元符号和下划线，还可以用数字0-9

![image-20210323232850186](https://gitee.com/xiefengjun/images/raw/master/test/image-20210323232850186.png)

看栗子, 第一个 `$88`可以, 第二个不可以

报错信息看一哈, 英语小课堂

> Uncaught SyntaxError: Invalid or unexpected token
>
> 没有捕获的    语法错误: 无效的          意外的  字符串

原因:

说一哈原因, 数字只能放到第二位开始, 绝大多数编程语言都是这样设计的, 因为编译器的原因

## 注释

```javascript
// 这个注释只能单行

// 和

/*这里面写注释*/
// 没了, 就这两个
```

#### 小结

多写好的注释, 那么什么是好的注释呢?

1. 描述为什么这样做, 为啥把代码写成这样, 是业务需要还是啥情况
2. 后面有个藏的很深的坑, 嗯, 我得在这儿注释一下
3. 遇到了什么问题, 如何解决的, 同时也可以提醒自己, 不然你翻看自己一个月前写的代码, 你不注释, 你会体会到痛苦



## if语句

> 流程控制

if(表达式){}

{}在只有一个语句时可以省略，**注意是一个语句而不是一行！**

```javascript
const a = 1;
if (a === 2)
    console.log('打印a'); console.log('打印b')
```

这里只会输出`打印b`

### 三元操作符

也叫, 问号冒号表达式, **很常用**

```javascript
const x = 10;

const color = x > 10 ? "red" : "blue";
//                      true    false
console.log(color);	
```

输出;

`blue`

讲一下, 在 `if`后面一个语句, `else`后面一个语句的时候使用, 简化`if...else...`

#### 栗子来了

一个函数, 返回一个数字的绝对值

```javascript
function abs(n){
  return n > 0 ? n : -n
}
```

## &&短路逻辑

```javascript
if (window.f1) {
    console.log('f1存在')
}
```

```javascript
window.f1 && console.log('f1存在')		
```

问: 控制台会输出啥? 自己去试一试呗

这两句语句等价

```javascript
a&&b
等价于
if (a) {
  b
}
```

A&&B： 如果A是真，就看B的值；如果A是假，就看A的值，就不会管B，短路

A&&B&&C&&D ： 取第一个假值 或者 B

## ||短路逻辑

```javascript
a||b
等价于
if(!a) {
  b
}
```

常见的应用场景就是给a设定默认值

```javascript
a = a || 100
如果a存在就a=a, 如果a不存在, a=100
等价于
if (a) {
 a = a
} else {
 a = 100
}
```

A || B || C || D : 取第一个真值或 D

#### 小结

条件语句

- `if...else...`

- `switch`

- `A?B:C`

- `A&&B`

- `fn&&fn()`

- `A||B`

- `A=A||B`

  



## 循环 Loop

> 流程控制

### while循环

```javascript
let a = 0.1;
while (a !== 1) {
    console.log(a)
    a = a + 0.1
}
```

由于浮点数的计算时不精确的，所以以上代码会死循环

### For循环

for, 其实是 while 的语法糖

```javascript
for (var i = 0; i < 5; i++) {
    console.log(i)
}
请问这里打印出的i是多少？
console.log(i)
```

答案是5， 因为当i == 4, i = i + 1 = 5, 然后退出循环

```javascript
for (let i = 0; i < 5; i++) {
    console.log(i)
}
请问这里打印出的i是多少？
console.log(i)
```

i是undefined. 因为Let声明的变量不会变量提升

或者说, var 的作用域是全局的



setTimeout就是过一段时间执行

```javascript
for (var i = 0; i < 5; i++) {
    setTimeout(()=>{
        console.log(i)
    }, 0)
}
```

会打印出5次5

我们已经知道for (var i = 0; i < 5; i++) {}执行完毕后，i的值是5

而setTimeout就是过一段时间执行， 而for循环是当前任务，所以这段代码意思就是说**等到for循环执行完毕**了，再打印5次i，所以就会打印5个5

同步执行, 与, 异步执行

```javascript
for (let i = 0; i < 5; i++) {
    setTimeout(()=>{
        console.log(i)
    }, 0)
}
```

当把var 换成 let, 就会打印出 0, 1, 2, 3, 4

for 循环在 `let `的时候有单独的逻辑

## break 和 continue

break是跳出离它最近的一个for循环

> 在多层循环中, `break`只能终止最里面包裹它的那个循环

continue是跳出本次循环，下次继续

```javascript
for (var i = 0; i < 10; i++) {
    for (var j = 0; j < 5; j++) {
        if (i===5) {
            break;
        }
    }
    console.log(i)
}
```

会打印出0,1,2,3,4,5,6,7,8,9

因为break只会跳出和他最近的一个for循环

## label

```javascript
{
    a:1;
}
```

以上的代码是：有一个代码块，代码块里有一个label, a: 1 表示这个标签是a, a的值是1

以上代码不是一个对象！



```javascript
foo: {
    console.log(1)
    break foo;
    console.log('本行不会输出')
}
console.log(2)
```

foo 表示 label的标识符是 foo, break foo 表示退出当前的Label, 所以代码会输出1， 2

## Refenences

推荐书籍

[入门篇](https://wangdoc.com/javascript/basic/grammar.html)

[你不知道的JavaScript（上卷）](https://book.douban.com/subject/26351021/)

先看上卷, 适合进阶