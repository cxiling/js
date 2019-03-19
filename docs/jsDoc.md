#### 使用一个文档化标签来描述代码：
* Person#say  // 名为"say"的实例方法

* Person.say  // 名为"say"的静态方法

* Person~say  // 名为"say"的内部函数

```
/** @constructor */
Person = function() {
    this.say = function() {
        return "I'm an instance.";
    }

    function say() {
        return "I'm inner.";
    }
}
Person.say = function() {
    return "I'm static.";
}

var p = new Person();
p.say();      // I'm an instance. 实例
Person.say(); // I'm static. 静态
// 这里无法直接访问内部函数 there is no way to directly access the inner function from here
```
