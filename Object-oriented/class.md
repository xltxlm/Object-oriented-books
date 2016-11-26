#类 面向对象的设计基础

* 命名方式第一个字母大写
* 如果此类明确不会被继承，在前面加上final限制
* 所有写入的方法都支持链式调用模型  - 需要工具自动完成配合
* __invoke 函数作为运行的入口


#废弃：继承
凡是采用继承的方式 来写功能类，全部不合格。
继承只能用来写配置类。

功能类概念

```
class tool
{
      /**
      * 此处实现功能
      */
      public function __invoke()
     {
     }
}

```

配置类：定义一些配置的属性，供扩展填写
```
abstract class xxxConfig
{
    protected name="";
    protected age"";
    ....
    
}
```
#新概念：组合编程 trait

trait 不能嵌套，否则复杂度
