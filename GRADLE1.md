# Gradle下载及配置
## 下载 Gradle
下载网址：https://gradle.org/releases/

![](img/A0.png)

## 解压
记住解压的路径（例D:\Gradle\gradle-6.6.1）

## 配置环境变量
1）新增系统变量：GRADLE_HOME 变量值：
   D:\Gradle\gradle-6.6.1（解压路径）

2）新增PATH环境变量：%GRADLE_HOME%\bin

## 检验是否配置完成
cmd中输入gradle -v 若显示版本号则配置完成。

![](img/A1.png)

# Groovy的基本语法
1）Groovy类和Java是二进制兼容的，Groovy编译器产生的字节码与Java编译器产生的字节码是完全一样的。

2）**对于JVM而言，Groovy和Java是完全一样的**，因此，Groovy能够完全使用各种Java API。

3）Groovy也是一门面向对象的语言。也就是说，Groovy中每一个事物最终都会被当做某些类的一个实例对象。

**4）groovy支持函数式编程，不需要main函数。**

5）groovy支持单元测试和模拟（对象），可以简化测试。

6）groovy中默认都是public（类、成员属性、方法等），groovy接口中不允许定义非public的方法。

7）groovy类会默认会成员变量生成getter与setter方法。无论你是直接使用还是调用get/set，最终都是调用     get/set方法，如：person.name相当于person.getName()

**8）在Groovy可以用def定义无类型的变量和返回值为无类型的方法。**

**部分语法代码演示:**

```Groovy
// 1.句尾分号可以省略
// 2.括号可以省略
// 3.定义变量用 def 例如
def i=10

// 4.定义集合，由于{ }是给闭包使用，所以定义集合或数据要用[ ]
def list=[‘a’,’b’]
list  << ‘c’
println list.get(2);

// 5.定义一个map
def map=['key1':'value1','key2':value2]
map.key3='value3'
println map.get(“key3”)

// 6.Groovy中的闭包

// 闭包其实是一段代码块，我们主要把闭包当作参数来使用
 def b1={
　　println “hello b1”
}

// 定义一个方法，方法里面需要闭包类型的参数
 def method1(Closure closure){
　　closure()
}
method1(b1)

// 7.定义一个闭包带参数
def b2={
　　V ->
　　println “hello ${v}”
}

 def method2(Closure closure){
　　closure(“b2”)
}
method2(b2)
```
