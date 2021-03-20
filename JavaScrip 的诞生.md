# JavaScrip 的诞生

## JavaScript 的历史

1995 年，布兰登·艾克加入网景公司，网景目标是把 Scheme 语言嵌入到 Netscape Navigator 浏览器当中。后来由于和 Sun 公司合作，决定发明一种网页脚本语言和 Java 语言一同发布推进，布兰登仅仅花了十天就把原型设计出来 JavaScript 了。

JavaScript 推出后在浏览器大获成功，微软在不久后为 IE 3 浏览器推出了 JScript 。为了获得竞争优势，微软将 IE 浏览器打包进了 windows 系统，以便获取浏览器市场。

网景于 1996 年向 ECMA（欧洲计算机制造商协会）提交语言标准。1997 年，ECMA以JavaScript语言为基础制定了ECMAScript标准规范ECMA-262。

### 小结

tldr: JavaScript 的历史实在是太长了, 感兴趣的看官可以点击下面的文章细细品读.

一句话说, JavaScript 的历史是备胎逆袭成功的励志故事, 至于有么有娶到白富美, 不知道, 让子弹再飞会儿.

[JavaScript 的历史](https://www.wangdoc.com/javascript/basic/history.html#%E8%AF%9E%E7%94%9F)

## JavaScript 命名

1. Mocha摩卡=>LiveScript=>JavaScript
2. java既是编程语言，也是一种咖啡
3. 浏览器一开始同时支持java和JavaScript
4. 后来，JS胜了（浏览器方面)

## JavaScript 特点

### 1. 操控浏览器的能力

JavaScript 的发明目的，就是作为浏览器的内置脚本语言，为网页开发者提供操控浏览器的能力。它是目前唯一一种通用的浏览器脚本语言，所有浏览器都支持。它可以让网页呈现各种特殊效果，为用户提供良好的互动体验。

目前，全世界几乎所有网页都使用 JavaScript。如果不用，网站的易用性和使用效率将大打折扣，无法成为操作便利、对用户友好的网站。

对于一个互联网开发者来说，如果你想提供漂亮的网页、令用户满意的上网体验、各种基于浏览器的便捷功能、前后端之间紧密高效的联系，JavaScript 是必不可少的工具。

### 2. 广泛的使用领域

近年来，JavaScript 的使用范围，慢慢超越了浏览器，正在向通用的系统语言发展。

**（1）浏览器的平台化**

随着 HTML5 的出现，浏览器本身的功能越来越强，不再仅仅能浏览网页，而是越来越像一个平台，JavaScript 因此得以调用许多系统功能，比如操作本地文件、操作图片、调用摄像头和麦克风等等。这使得 JavaScript 可以完成许多以前无法想象的事情。

**（2）Node**

Node 项目使得 JavaScript 可以用于开发服务器端的大型项目，网站的前后端都用 JavaScript 开发已经成为了现实。有些嵌入式平台（Raspberry Pi）能够安装 Node，于是 JavaScript 就能为这些平台开发应用程序。

**（3）数据库操作**

JavaScript 甚至也可以用来操作数据库。NoSQL 数据库这个概念，本身就是在 JSON（JavaScript Object Notation）格式的基础上诞生的，大部分 NoSQL 数据库允许 JavaScript 直接操作。基于 SQL 语言的开源数据库 PostgreSQL 支持 JavaScript 作为操作语言，可以部分取代 SQL 查询语言。

**（4）移动平台开发**

JavaScript 也正在成为手机应用的开发语言。一般来说，安卓平台使用 Java 语言开发，iOS 平台使用 Objective-C 或 Swift 语言开发。许多人正在努力，让 JavaScript 成为各个平台的通用开发语言。

PhoneGap 项目就是将 JavaScript 和 HTML5 打包在一个容器之中，使得它能同时在 iOS 和安卓上运行。Facebook 公司的 React Native 项目则是将 JavaScript 写的组件，编译成原生组件，从而使它们具备优秀的性能。

Mozilla 基金会的手机操作系统 Firefox OS，更是直接将 JavaScript 作为操作系统的平台语言，但是很可惜这个项目没有成功。

**（5）内嵌脚本语言**

越来越多的应用程序，将 JavaScript 作为内嵌的脚本语言，比如 Adobe 公司的著名 PDF 阅读器 Acrobat、Linux 桌面环境 GNOME 3。

**（6）跨平台的桌面应用程序**

Chromium OS、Windows 8 等操作系统直接支持 JavaScript 编写应用程序。Mozilla 的 Open Web Apps 项目、Google 的 [Chrome App 项目](https://developer.chrome.com/apps/about_apps)、GitHub 的 [Electron 项目](https://electron.atom.io/)、以及 [TideSDK 项目](http://tidesdk.multipart.net/docs/user-dev/generated/)，都可以用来编写运行于 Windows、Mac OS 和 Android 等多个桌面平台的程序，不依赖浏览器。

**（7）小结**

可以预期，JavaScript 最终将能让你只用一种语言，就开发出适应不同平台（包括桌面端、服务器端、手机端）的程序。早在2013年9月的[统计](http://adambard.com/blog/top-github-languages-for-2013-so-far/)之中，JavaScript 就是当年 GitHub 上使用量排名第一的语言。

著名程序员 Jeff Atwood 甚至提出了一条 [“Atwood 定律”](http://www.codinghorror.com/blog/2007/07/the-principle-of-least-power.html)：

> “所有可以用 JavaScript 编写的程序，最终都会出现 JavaScript 的版本。”(Any application that can be written in JavaScript will eventually be written in JavaScript.)

### 易学性

相比学习其他语言，学习 JavaScript 有一些有利条件。

**（1）学习环境无处不在**

只要有浏览器，就能运行 JavaScript 程序；只要有文本编辑器，就能编写 JavaScript 程序。这意味着，几乎所有电脑都原生提供 JavaScript 学习环境，不用另行安装复杂的 IDE（集成开发环境）和编译器。

**（2）简单性**

相比其他脚本语言（比如 Python 或 Ruby），JavaScript 的语法相对简单一些，本身的语法特性并不是特别多。而且，那些语法中的复杂部分，也不是必需要学会。你完全可以只用简单命令，完成大部分的操作。

**（3）与主流语言的相似性**

JavaScript 的语法很类似 C/C++ 和 Java，如果学过这些语言（事实上大多数学校都教），JavaScript 的入门会非常容易。

必须说明的是，虽然核心语法不难，但是 JavaScript 的复杂性体现在另外两个方面。

首先，它涉及大量的外部 API。JavaScript 要发挥作用，必须与其他组件配合，这些外部组件五花八门，数量极其庞大，几乎涉及网络应用的各个方面，掌握它们绝非易事。

其次，JavaScript 语言有一些设计缺陷。某些地方相当不合理，另一些地方则会出现怪异的运行结果。学习 JavaScript，很大一部分时间是用来搞清楚哪些地方有陷阱。Douglas Crockford 写过一本有名的书，名字就叫[《JavaScript: The Good Parts》](http://javascript.crockford.com/)，言下之意就是这门语言不好的地方很多，必须写一本书才能讲清楚。另外一些程序员则感到，为了更合理地编写 JavaScript 程序，就不能用 JavaScript 来写，而必须发明新的语言，比如 CoffeeScript、TypeScript、Dart 这些新语言的发明目的，多多少少都有这个因素。

尽管如此，目前看来，JavaScript 的地位还是无法动摇。加之，语言标准的快速进化，使得 JavaScript 功能日益增强，而语法缺陷和怪异之处得到了弥补。所以，JavaScript 还是值得学习，况且它的入门真的不难。

### 小结

**JavaScript, 学他! 学他!! 学他!!! 有饭吃**



## JavaScript 与 ECMAScript 的关系

1996年8月，微软模仿 JavaScript 开发了一种相近的语言，取名为JScript（JavaScript 是 Netscape 的注册商标，微软不能用），首先内置于IE 3.0。Netscape 公司面临丧失浏览器脚本语言的主导权的局面。

1996年11月，Netscape 公司决定将 JavaScript 提交给国际标准化组织 ECMA（European Computer Manufacturers Association），希望 JavaScript 能够成为国际标准，以此抵抗微软。ECMA 的39号技术委员会（Technical Committee 39）负责制定和审核这个标准，成员由业内的大公司派出的工程师组成，目前共25个人。该委员会定期开会，所有的邮件讨论和会议记录，都是公开的。

1997年7月，ECMA 组织发布262号标准文件（ECMA-262）的第一版，规定了浏览器脚本语言的标准，并将这种语言称为 ECMAScript。这个版本就是 ECMAScript 1.0 版。之所以不叫 JavaScript，一方面是由于商标的关系，Java 是 Sun 公司的商标，根据一份授权协议，只有 Netscape 公司可以合法地使用 JavaScript 这个名字，且 JavaScript 已经被 Netscape 公司注册为商标，另一方面也是想体现这门语言的制定者是 ECMA，不是 Netscape，这样有利于保证这门语言的开放性和中立性。因此，ECMAScript 和 JavaScript 的关系是，前者是后者的规格，后者是前者的一种实现。在日常场合，这两个词是可以互换的。

ECMAScript 只用来标准化 JavaScript 这种语言的基本语法结构，与部署环境相关的标准都由其他标准规定，比如 DOM 的标准就是由 W3C组织（World Wide Web Consortium）制定的。

ECMA-262 标准后来也被另一个国际标准化组织 ISO（International Organization for Standardization）批准，标准号是 ISO-16262。

### 小结

ECMAScript是纸上的标准，JS是浏览器的实现 纸上标准往往落后于浏览器，先实现，在写进标准

## JavaScript 的10 个设计缺陷

**∵ JavaScript的设计阶段过于仓促，没有先例，以及过早的标准化
 ∴ Javascript 的设计有缺陷**

### 1. 不适合开发大型程序

Javascript没有名称空间（namespace），很难模块化；没有如何将代码分布在多个文件的规范；允许同名函数的重复定义，后面的定义可以覆盖前面的定义，很不利于模块化加载。

### 2. 非常小的标准库

Javascript提供的标准函数库非常小，只能完成一些基本操作，很多功能都不具备。

### 3. null和undefined

null属于对象（object）的一种，意思是该对象为空；undefined则是一种数据类型，表示未定义。

```javascript
　　typeof null; // object
　　typeof undefined; // undefined
复制代码
```

两者非常容易混淆，但是含义完全不同。

```javascript
   var foo;
　　alert(foo == null); // true
　　alert(foo == undefined); // true
　　alert(foo === null); // false
　　alert(foo === undefined); // true
复制代码
```

在编程实践中，null几乎没用，根本不应该设计它。

### 4. 全局变量难以控制

Javascript的全局变量，在所有模块中都是可见的；任何一个函数内部都可以生成全局变量，这大大加剧了程序的复杂性。

```javascript
   a = 1;
　　(function(){
　　　　b=2;
　　　　alert(a);
　　})(); // 1
　　alert(b); //2
复制代码
```

### 5. 自动插入行尾分号

Javascript的所有语句，都必须以分号结尾。但是，如果你忘记加分号，解释器并不报错，而是为你自动加上分号。有时候，这会导致一些难以发现的错误。

比如，下面这个函数根本无法达到预期的结果，返回值不是一个对象，而是undefined。

```javascript
　　function(){
　　　　return
　　　　　　{
　　　　　　　　i=1
　　　　　　};
　　}
复制代码
```

原因是解释器自动在return语句后面加上了分号。

### 6. 加号运算符

+号作为运算符，有两个含义，可以表示数字与数字的和，也可以表示字符与字符的连接。
 如果一个操作项是字符，另一个操作项是数字，则数字自动转化为字符。
 这样的设计，不必要地加剧了运算的复杂性，完全可以另行设置一个字符连接的运算符。

### 7. NaN

NaN是一种数字，表示超出了解释器的极限。它有一些很奇怪的特性：

```javascript
　　NaN === NaN; //false
　　NaN !== NaN; //true
　　alert( 1 + NaN ); // NaN
复制代码
```

与其设计NaN，不如解释器直接报错，反而有利于简化程序。

### 8. 数组和对象的区分

由于Javascript的数组也属于对象（object），所以要区分一个对象到底是不是数组，相当麻烦。[Douglas Crockford](http://crockford.com/javascript/)的代码是这样的：

```javascript
　　if ( arr &&
　　　　typeof arr === 'object' &&
　　　　typeof arr.length === 'number' &&
　　　　!arr.propertyIsEnumerable('length')){

　　　　alert("arr is an array");
　　}
复制代码
```

### 9. == 和 ===

==用来判断两个值是否相等。当两个值类型不同时，会发生自动转换，得到的结果非常不符合直觉。 因此，推荐任何时候都使用"==="（精确判断）比较符

```javascript
　　"" == "0" // false

　　0 == "" // true

　　0 == "0" // true

　　false == "false" // false

　　false == "0" // true

　　false == undefined // false

　　false == null // false

　　null == undefined // true

　　" \t\r\n" == 0 // true
复制代码
```

### 10. 基本类型的包装对象

Javascript有三种基本数据类型：字符串、数字和布尔值。它们都有相应的建构函数，可以生成字符串对象、数字对象和布尔值对象。

```javascript
　　new Boolean(false);
  
　　new Number(1234);
  
　　new String("Hello World");
复制代码
```

与基本数据类型对应的对象类型，作用很小，造成的混淆却很大。

```javascript
　　alert( typeof 1234); // number

　　alert( typeof new Number(1234)); // object
```

## Refenences

[JavaScript 语言的历史--网道 JavaScript 教程](https://www.wangdoc.com/javascript/basic/history.html)

[JavaScript 历史--维基百科](https://zh.wikipedia.org/wiki/JavaScript#%E5%8E%86%E5%8F%B2)

[Javascript诞生记--阮一峰 (2011)](http://www.ruanyifeng.com/blog/2011/06/birth_of_javascript.html)

[Javascript的10个设计缺陷--阮一峰 (2011)](http://www.ruanyifeng.com/blog/2011/06/10_design_defects_in_javascript.html)















