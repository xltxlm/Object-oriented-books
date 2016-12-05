#方法原则

所有的方法只能是类似 get/set/add/clean 的处理方式：提供 读/写 概念

+ 名称含义
    * get读取属性，也可能是内置自动解析处理的内容
    * set设置属性，外部传递进来需要处理的参数
    * add 添加数组型的内容的一个子集
    * clean 清空掉 static类型的内容

* 特性
    + 读类型的方法不接受任何参数
    + 写类型的方法只能接受一个参数

为什么只能接受一个参数？

假设需要处理经纬度，那么按照常规的方式是 


```
function setLatitudeAndLongitude(latitude,longitude) {
    ...
}
```

看起来完全没有问题！
思考下面的问题
+ setLatitudeAndLongitude(51.2,125.33) 请问：凭什么知道第一个参数传入的就是纬度呢？ 常识？ 框架约定？ 看函数注释？看函数定义？ 看函数名？
+ 为什么在 setLatitudeAndLongitude(51.2,125.33) 一次做了2个事情，类的第一原则是：单一职责原则

正确的做法是


```
final class LatitudeAndLongitude
{
    protected latitude {get,set}
    protected longitude {get,set}
}


function setLatitudeAndLongitude(LatitudeAndLongitude) {
    ...
}
```

#依赖倒置/注入

setxxx 就是！
