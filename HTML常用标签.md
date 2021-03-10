# HTML常用标签

# a 标签

## a标签的属性

### 1. herf

```shell
yarn global add http-server 

# 像用户一样, 使用自己的网页
# 两个工具都可以
yarn global add parcel 

# 下载配置好之后, 运行下面这句, 会显示几个网址, 选其中一个打开即可
http-server . -c-1

# alias 之后, 可以简写 hs 
hs -c-1
```

**a** 链接的地址

取值:

 1. 网址:

    a. https://www.baidu.com

    b. http://www.baidu.com

    c. //www.baidu.com 推荐使用这一种写法, 放进浏览器会自动补全

	2. 路径:

    a. 绝对路径：/a/b/c, 开启 http-server 之后, 当前目录就是根目录, 

    b. 相对路径：a/b/c, 因为当前目录就是根目录, 所以 a 前面的 `/`有么有都是一样的

    ​					index.html和./index.html; 根目录有个index.html, 这样写就ok

	3. 伪协议:

    a. javascript:代码;  【需要写冒号和分号】

    ​		i. 应用场景：希望点击a标签之后页面不刷新也不返回到顶部，什么也不做：

    ​		ii. `<a href="javascript:;"></a>`

    ​		iii. 这就相当于执行一段没有意义的js代码, 里面只写一个分号即可

    b. mailto:邮箱

    ​		i. `<a href="mailto:123@qq.com"></a>`

    c. tel:手机号

    ​		i. `<a href="tel:123456789"></a>`

	4. id: href=#id名，可以跳转到id名为xxx的标签

    a. 如`<p id="xxxx"></p>, <a href="#xxx"></a>`就可以定位到这个p标签

    老师: href 加 #id名, 就可以跳转到 id 名为 xxx 的标签

小结: a 标签的 herf 总共有 9 种不同的取值

### 2. target

​		a. 决定是在本页面打开, 还是在新开一个页面打开链接

​		b. 取值:

​					i. 四个内置的名字:

- _blank 打开新页面
- _self 在当前页面打开
- _top 顶部页面打开
- _parent 在父级页面打开， 3和4适用于有Iframe内嵌窗口的情况

小结: target 的默认值是 `_self`, 具体使用的使用的时候再回看复习

# table标签

table 里面只能有以下三个标签

```html
<table>
        <thead></thead>
        <tbody></tbody>
        <tfoot></tfoot>
</table>
```

- <tr></tr>    table row 表格里面的**一行**
- <th></th>    表格的表头
- <td></td>    table data 表格的数据

## 栗子 1:

用 table 标签制作如下表格

|   英语    | 翻译 |
| :-------: | :--: |
|   hyper   | 超级 |
|  target   | 目标 |
| reference | 引用 |

```html
<table>
        <thead>
            <tr>
                <th>英语</th>
                <th>翻译</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>hyper</td>
                <td>超级</td>
            </tr>
            <tr>
                <td>target</td>
                <td>目标</td>
            </tr>
            <tr>
                <td>reference</td>
                <td>引用</td>
            </tr>
        </tbody>
        <tfoot></tfoot>
    </table>
```

## 栗子 2:

#### 两个表头怎么实现？

![两个表头怎么实现？](https://gitee.com/xiefengjun/images/raw/master/test/1591790799495-c3054088-01cf-4d44-8c54-411c201b1e1e.png)

这个栗子中, 这里有两个表头, 分别是名字这一行, 还有数学科目这一列

原理还是不变的

表头都用 `<th></th>`

数据都用 `<td></td>`

```html
<table>
        <thead>
            <tr>
                <th></th>
                <th>小红</th>
                <th>小明</th>
                <th>小颖</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <th>数学</th>
                <td>61</td>
                <td>91</td>
                <td>85</td>
            </tr>
            <tr>
                <th>语文</th>
                <td>61</td>
                <td>91</td>
                <td>85</td>
            </tr>
            <tr>
                <th>英语</th>
                <td>61</td>
                <td>91</td>
                <td>85</td>
            </tr>
        </tbody>
    </table>
```

## table的样式

table-layout:

- table-layout: auto; auto表示根据内容来计算宽度
- table-layout: fixed; fixed表示定宽，尽可能地让宽度平均

border-collapse 和 border-spacing用来调整表格Border的间隔

- border-collapse:    collapse    合并
- border-spacing:    border之间的距离, 需要设置为 0

一般会设置为：

```html
table {
            table-layout: auto;
            border-collapse: collapse;
            border-spacing: 0;
        }
```

设置前：

![image.png1](https://gitee.com/xiefengjun/images/raw/master/test/1591797588815-70511abb-6fa3-4670-9122-593c877b3afb-20210310120337329.png)

设置后：

![image.png2](https://gitee.com/xiefengjun/images/raw/master/test/1591797569440-e225c6fe-4bab-4288-aa80-0f45d5bf88f7-20210310120349103.png)

如果table-layout是fixed, 每一栏会是等宽(平均)，而如果是auto, 内容多的那一列会更宽一些

![image.png3](https://gitee.com/xiefengjun/images/raw/master/test/1591797635025-378330bb-6bb5-491b-ba66-1f120ac76e13-20210310120400463.png)

# img标签

## 作用：

发出GET请求，展示图片

## 属性

1. src: 图片地址
2. alt: 如果图裂了，无法加载，会显示这个alt属性的文字作为备用显示
3. width 如果只写宽度，高度会自适应
4. height 如果只写高度，宽度会自适应

方老师的要求, 一个合格的前端不能让图变形！所以就只写宽度或者高度！

## 事件

onload 加载成功

onerror 加载失败

## 响应式

手机屏幕显示自适应

关键就是“**max-width: 100%**;”

```css
  * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
  }

  img {
      max-width: 100%;
  }
```

这样图片就可以**自适应不同的屏幕大小**

# form标签

### 作用：

发get或者post请求，刷新页面



### 属性

action: 往哪里发请求

method: Get 或者 POST 控制用哪种方式请求

autocomplete 自动填充，值可以取"off"或者"on"

- `off`：在每一个用到的输入域里，用户必须显式的输入一个值，或者document 以它自己的方式提供自动补全；浏览器不会自动补全输入。
- `on`：浏览器能够根据用户之前在表单里输入的值自动补全, 会给出填这个表单的提示

target: 在当前页面提交，还是新开一个页面提交



### Input的submit和button的submit有什么区别？

Input标签里不能再有其他的标签

button标签里可以有其他的标签

比如里面加个 `span` `strong` 加图片`img`也可以

```html
 <form action="/xxx" method="GET" autocomplete="on">
        <input type="text" name="username" id="">
        <input type="submit" value="input提交">
        <button type="submit">
            <strong>button提交</strong>
        </button>
    </form>
```



## 其他感想

iframe

作用: 内嵌窗口, 也就是内嵌网页, 网页里面内嵌网页, 目前已经很少用了, 现在都是用 `Ajax`



​		



