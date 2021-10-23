## js基本数据类型如何判断
- number、stirng、boolean、bigint、symbol、undefined、null

## HTML中居中的方式
- text-align:center方式，水平居中块级元素中的行内元素，如inline，inline-block
- margin:0 auto方式，这种对齐方式要求内部元素是块级元素，并且不能脱离文档流（如设置position:absolute）,否则无效。
- display:table-cell，配合width，text-align:center,vertical-align:middle让大小不固定元素垂直居中,这个方式将要对其的元素设置成为一个td，float、absolute等属性都会影响它的实现，不响应margin属性;
垂直居中，行内元素的垂直居中把height和line-height的值设置成一样的即可。
- 使用css3的translate水平垂直居中元素 ，设置top：50%，left：50%，然后使用transform来向左向上偏移半个内元素的宽和高。
- 使用css3计算的方式居中元素calc，例如：left: calc(50% - 元素固定宽度);
- 使用弹性盒(display：flex)，display:flex;justify-content:center;align-items:center;

## 如何把行内元素转成块级元素， 有多少种方式？
- 使用display:block
- 使用float
- 使用position（absolute和fixed）

## display:none 与 visibility：hidden 的区别

## 什么是伪类 和 伪元素，有哪些，区别是什么？

## box-sizing是什么，各个参数含义

## JS中map和filter区别，是否会改变原数组？

## JS中改变原数组的方法
- push、pop、shift、unshift、splice、reverse、sort

## 判断一个变量是数组有几种方式？
- instanceof ，原型判断，写法：变量 instanceof Array
- __proto__，原型判断，写法：变量.__proto__ === Array.prototype
- constructor，原型判断，写法：变量.constructor === Array
- Object.prototype.toString，通过object类型的副属性class去判断的其中函数的class是Function，结果是[object Function]， 普通的对象是Object，结果是- - [object Object]，写法：Object.prototype.toString.call(变量) === '[object Array]'
- Array.isArray，es6新增的方法，写法：Array.isArray(变量)
## 你知道哪些HTTP状态码？


## 事件代理、事件冒泡、事件捕获是什么？
- 事件代理：又称之为事件委托，是JavaScript中常用绑定事件的常用技巧。“事件代理”是把原本需要绑定在子元素的响应事件（click、keydown......）委托给父元素，让父元素担当事件监听的职务。事件代理的原理是DOM元素的事件冒泡。

## 什么是跨域？如何处理？


## axios 原理
- axios 是一个基于 promise 的 HTTP 库，可以用在浏览器和 node.js 中。axios可以用在浏览器和 node.js 中是因为，它会自动判断当前环境是什么，如果是浏览器，就会基于XMLHttpRequests实现axios。如果是node.js环境，就会基于node内置核心模块http实现axios。

## 述路由原理
- 路由分为后端路由和前端路由。
- 前端路由：URL到函数的映射。路由的映射函数通常是进行一些DOM的显示隐藏操作。当访问不同路径时，就会显示不同的页面组件。
- 前端路由主要有两种实现方案：hash、history API
## 如何理解html语义化
- 优点：seo、方便阅读、不用看css

## 变量提升

## let与var与函数声明得区别

## 作用域链
- 概念
## 原型链
- 概念
- __proto__与prototype得区别
- test.__proto__ =Test.prototye
- Test.prototype.__proto__ = Object.prototype
- Test.prototype.construtor = Test
- test.__proto___ = Function.prototype
- Function.prototype = Function.__proto__
- Object.__proto__ = null 

## 什么是BFC

## 响应式布局方案
- %、rem、em、@media、vw

## flex:1
- flex-grow：1
- flex-shrink：1
- flex-basis：0%
## 如何实现居中
- flex
- margin
- position

## bootstrap栅格原理
- %、@media
## flex布局和传统布局的性能对比

## %相对于谁

## css会阻塞页面渲染吗
- 不会
- HTML解析文件，生成DOM Tree，解析CSS文件生成CSSOM Tree,将Dom Tree和CSSOM Tree结合，生成Render Tree(渲染树),根据Render Tree渲染绘制，将像素渲染到屏幕上。

## Symbol
- new Symbol 报错
- Symbol应用
- Symbol.iterator
```js
let o = {}
o[Symbol.iterator] = function(){
  let i = 0 
  return {
    next:function(){
      return {
        value:i++,
        done:i>10
      }
    }
  }
}
```

## this指向
- 箭头函数
- 非严格调用
- 直接调用
- 对象调用
- apply、call、bind

## JS垃圾回收与V8垃圾回收

## 闭包
- 

## reduce实现

## compose实现

## apply、bind、call区别实现

## new实现

## 继承

## class继承与原型继承区别

## 宏任务 微任务

## js的event loop与node的event loop区别

## setTImeout与requestAnmationframe区别

## try{}catch{}、onerror、addEventListener('error')、unhandlerrejection

## 迭代器
- 迭代器模式
- string、array、map、set、dom都实现了迭代器【键值是Symbol.iterator】实现的函数
- 方法：for-of、数组解析、 扩展运算符、 Array.from、 set、map

```js
let test = 'hello world'
console.log(test[Symbol.iterator])
for(let item of test){
  console.log(Item)
}
```



## promise异常

## promise 异步实现

## promise穿透实现

## promise then链式调用实现

## promise静态方法实现

## 为什么给对象添加的方法能用在基本类型上？
- .运算符提供了装箱操作，他会根据基础数据类型，创建一个临时的对象，使得我们可以在基础数据类型上调用对于的对象方法



## 前端工程化

## 模块化
- commonjs、cmd、amd、import 区别

## 响应式框架基本原理

## 模板编译原理

## 订阅、发布模式

## mvvm

## 虚拟dom

## 柯里化
```js
function curry(fn){
  return function main(...args){
    if(fn.length<args){
      return fn.apply(this,args)
    }else{
      return funcion(...child){
        return main.apply(this,args.concat(child))
      }
    }
  }
}
```

## diff算法

## vue 组件通信
- $attr、inject、project、props、vuex、$parent、$chidren

## vuex原理

## 加上key就一定性能最优吗？

## 性能监控和错误收集

## 缓存
- 缓存的概念和分类
- 缓存和浏览器操作
- 验证缓存的轮子

## http
- http的现状和痛点
- http2.0特性
- 实时通信

## 双向通信
- sse
- websocket 

## 单页面权限
- anuthentication cookie实现权限
- jwt+cookie

## pomise原理
- 化 Promise 状态（pending）
- 执行 Promise 中传入的 fn 函数，将Promise 内部 resolve、reject 函数作为参数传递给 fn ，按事件机制时机处理
-  then(..) 注册回调处理数组（then 方法可被同一个 promise 调用多次）
- omise里的关键是要保证，then方法传入的参数 onFulfilled 和 onRejected，必须在then方法被调用的那一轮事件循环之后的新执行栈中执行。

## 简述async await原理

## 什么是虚拟DOM？

## vue如何实现路由拦截？
- router.beforeEach

## promise.race
```js

```
## promise.then
```js

```
## promise.all
```js

```
## canvas
- 图片压缩

## webgl
- 材质相关，有哪几种材质，有什么区别，对灯光的感应程度
- 面相关的，如果镂空一个面，镂空的面上加uv
- UV相关的，对应关系
- 几何变换
- webgl和canvas的坐标转化
- 设定坐标轴在几何体的任意位置
- 3D数学，向量，矩阵相关
- 模型围绕一个点运动
- Geometry和BufferGeometry的区别
- 物体描边，Edges
- Shape的使用

## vue2.x不能检测哪些属性变化
- object:增删元素
- array:使用下标更新数组元素、使用赋值方式改变数组长度、用下标增删数组元素

## vue模板解析
- 解析器、优化器、生成器
- template解析为ast、遍历ast给静态节点打上标记、根据优化之后的ast配合vnode提供的方法生成render函数

## diff算法

## vue组件通信方式
- props / $emit 适用 父子组件通信
- ref 与 parent/children 适用 父子组件通信
- EventBus （emit/on） 适用于 父子、隔代、兄弟组件通信
- attrs/listeners 适用于 隔代组件通信
- provide / inject 适用于 隔代组件通信
- Vuex 适用于 父子、隔代、兄弟组件通信

## watch/computed的区别

## v-if与v-show的区别

## react
- setState是异步还是同步？
- useState为什么不能放在条件里？
- 函数组件中如何执行异步请求操作？
- class中请求应该放在哪个生命周期？
- 如何用useEffect实现class的生命周期？

## 输入网址到现实的过程
- 重定向
- 查看缓存
- DNS解析，获取IP地址
- TCP连接建立
- 发送报文请求
- 响应报文数据
- 浏览器解析数据
- 渲染

## 节流与防抖

## 浏览器缓存
- 缓存位置:Service Worker、Menory Cache、Disk Cache、Push Cache
- 缓存策略：强缓存、协商缓存

## cookie与session

## GET/POST的本质区别
## http与https的区别
## CDN的优化原理
## HTTP 2.0 的新特性

## 扫码登录实现原理


