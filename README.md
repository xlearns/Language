## js基本数据类型如何判断
- number、stirng、boolean、bigint、symbol、undefined、null

## 如何理解html语义化

## 什么是BFC

## 响应式布局方案


## 如何实现居中
- flex
- margin
- position

## bootstrap栅格原理

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

