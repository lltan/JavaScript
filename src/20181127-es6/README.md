## ES6的骚操作

### 目录

- var function
  - var存在的问题 
    - 会变量提升（先声明，不会复制）
    - 没有块级作用域，是全局作用域/函数作用域
- let const  
  - let的优势 
    - 不会变量提升，不能重复被定义，不会污染全局变量
    - 会和{}产生作用域
    - 
  - let存在一定问题
```js
let a = 2
{
  console.log(a)
  let a =1
}
// undefined
  ```  
  - const
    - let 可以重新赋值 const不能改变赋值的空间
```js
const a = 1
a = 2
// 报错
const b = []
b.push(1)
// 正常运行
```

- 扩展运算符
  - 对任意个数求和
    - ES5实现 slice
    - ES6...实现
  - 合并两个数组
    - ES5实现 concat
    - ES6...实现
  - 合并两个对象
  - 存在的问题（深拷贝、浅拷贝）
    - 深拷贝 拷贝的不是引用地址
    - ...只能展开一层是个浅拷贝，需要递归处理
      - JSON.parse可以简单解决
      - JSON存在一定问题
        - 可以处理null/date
        - 处理不了正则、函数
    - 基于以上考虑实现一个深拷贝
      ...

- 解构赋值
  - 对象解构
  - 数组解构

- 箭头函数 arrowFn
  - 没有this
  - 没有argument

- Object.defineProperty
  - 使用
  - 应用
    - vue2.0实现数据双向绑定
  - 缺点
    - 不能检测数组

- proxy、reflect
  - 应用
    - vue3.0重写数据双向绑定
  - 缺点
    - 兼容性不好
  - 优点
    - 能检测数组
  - 深度监控（可以递归）（自行思考）

- 类 class
  - ES5知识
    - __proto__ 找的是所属类的原型，所有的类型
    - prototype 这是原型，只有构造函数才有原型
    - 继承
      - 继承实例上的属性
        - call
      - 继承公共属性
        - 
        - Object.create 
          - Child.prototype = Object.create(Parent.prototype, { constructor: { value: Child } })
          - ES5如何实现
      - 全都要
        - call + 原型继承
  - ES6的类
    - 编译成ES5的样子

- 装饰器
  - 装饰类
  - 装饰类中的属性
  - 装饰类中的方法
  - 不能装饰函数，因为函数有变量提升

- Set/Map
  - API一览
  - 面试题
    - 两个数组求并集
    - 两个数组求交集
    - 两个数组求差集

- 数组的方法
  - findIndex
  - reduce
    - 应用
      - 数组求和
      - 组合 compose
  
