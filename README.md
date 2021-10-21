## js基本数据类型如何判断
- number、stirng、boolean、bigint、symbol、undefined、null

## 如何理解html语义化
- 优点：seo、方便阅读、不用看css
## 什么是BFC

## 响应式布局方案
- %、rem、em、@media、vw

## 如何实现居中
- flex
- margin
- position

## bootstrap栅格原理
- %、@media
## flex布局和传统布局的性能对比

## %相对于谁


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
- 非严格调用
- 直接调用
- 对象调用
- apply、call、bind
- 
## 闭包
- 

## reduce实现

## compose实现

## apply、bind、call实现

## new实现

## 继承

## class继承与原型继承区别

## 宏任务 微任务

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

## promise.race

## promise.then

## promise.all
