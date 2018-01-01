## 深入理解JS
重新学习JS，查缺补漏，记录学习过程中的新发现

### 关于this
- 旧认知：函数中的this指向的是函数本身，既函数就是一个作用域
- 新发现：函数中的this指向的是函数所处的作用域中


- 新发现：对象中的this指向的是对象本身，既对象就是一个新的作用域，若某属性是一个函数且该属性属于某对象，直接调用该对象的此函数属性其this指向对象本身


### 关于call和apply
- 新发现：apply和call的区别仅为参数上的区别，第一个参数都表示影响的作用域；第二个参数apply为数组对象，call为非数组；call为apply的封装实现

- 新发现：apply和call仅在某函数运行时替换作用域，执行结束后原函数作用域不变，例：
 
``` javascript
var obj1={
  age:1
}

var func1=function(){
  console.log(this.age)
}

func1.apply(obj1)  // Output: 1

func1()   // Output: undefined

```




