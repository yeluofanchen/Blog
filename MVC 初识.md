# MVC 初识

## MVC三个对象

Model-View-Controller (**MVC**)

m, 主要负责数据相关的存储, 比如数据的增删改查, 也包括数据模型的初始化和解析数据相关的操作

v, 主要是视图方面的更新, 渲染, 

c, 控制器, 负责 m 和 v 之外的部分

```javascript
// TODO: 数据相关放到 m
const m = {
  data: {},
  create () {},
  delete () {},
  update () {},
  get () {}
}

// TODO: 视图相关放到 v
const v = {
  el: null,
  html: ``,
  init (container) {},
  render (n) {}
}

// TODO: 其他相关放到 c
const c = {
  init (container) {},
  events: {},
  autoBindEvents () {}
}
```

## EventBus

eventBus 是一个对象, 可以用于 上面三个对象 m, v, c 之间的通信

```javascript
// eventBus 有许多 API, 其中 on 方法用于添加事件监听, trigger 方法用于触发事件
const eventBus = $({})
eventBus.trigger('m:updated')
eventBus.on('m:updated', () => {
      v.render(m.data.n)
    })
```

## 表驱动编程

> 表驱动法就是一种编程模式(scheme)——从表里面查找信息而不使用逻辑语句(if 和case)。 事实上，凡是能通过逻辑语句来选择的事物，都可以通过查表来选择。 对简单的情况而言，使用逻辑语句更为容易和直白。 但随着逻辑链的越来越复杂，查表法也就愈发显得更具吸引力。

关键词: 干掉重复和冗余, 为了简洁

```javascript
// jQuery 风格写法
$('#el1').on('事件A', fn1)
$('#el2').on('事件B', fn2)
$('#el3').on('事件C', fn3)
$('#el4').on('事件D', fn4)
$('#el5').on('事件E', fn5)
```

抽取关键信息, '#el', '事件', fn, 将这三个组成一个对象

```javascript
const events = {
    '#el1 事件A': 'fn1',
    '#el2 事件B': 'fn2',
    '#el3 事件C': 'fn3',
    '#el4 事件D': 'fn4',
    '#el5 事件E': 'fn5'
}

const eventFunctions = { //事件处理函数
    fn1(){}
    fn2(){}
    fn3(){}
    fn4(){}
    fn5(){}
}
```

然后创建一个函数，给这些元素绑定相应的事件：

```javascript
function autoBindEvents(){
    for(let key in events){
        const spaceIndex = key.indexOf(' ')
        const element = key.slice(0, spaceIndex)  //得到各个'#el'
        const event = key.slice(spaceIndex + 1) //得到各个'事件'
        const fn = eventFunctions[events[key]] //得到各个fn
        $(element).on(event, fn) //绑定事件
    }
}
```

## 我对于模块化的理解

随着前端的发展, 开发的应用越来庞大, 代码量日趋复杂. 模块化可以把各个功能独立开发, 比如进一步组件化, 通过父子组件的方式进行前端开发, 提高复用性, 对代码进行解耦, 各个模块相互独立, 有各自的 data, view, methods, 等等, 可以使程序的结构更加清晰, 方便维护.

 



