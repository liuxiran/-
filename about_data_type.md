#关于js的数据类型

##js的数据类型

js的数据类型有6种，分别是 Undefined、Null、Boolbean、Number、String(简单类型)和Object(引用类型)
1. Undefined
var a               //"undefined",未初始化的变量会自动赋予undefined的值。
typeof b            //"undefined",未声明的变量获取类型时，也是undefined。

2. Null
Null类型只有一个特殊值，null，表示一个空对象指针。保存对象的变量在真正保存对象之前，声明为null。

3. Boolbean
该类型的字面量只有两个值：true和false，区分大小写。和其他类型的值之间的转化关系如下表：
>
| 数据类型       | 转换为true的值                | 转化为false的值   |
| ---------------| ------------------------------| ------------------|
| Boolbean       | true                          | false             |
| String         | 任何非空字符串                | ""                |
| Number         | 任何非零数字值（包括无穷大）  | 0和NaN            |
| Object         | 任何对象                      | null              |
| Undefined      | 无                            | undefined         | 

Boolbean类型的转化函数：Boolbean()

4. 关于Number、String和Object类型，后续会有专门的整理文档。

##获取变量数据类型的方法

常用来获取变量数据类型的方法是typeof：是一个一元运算，放在运算数之前，运算数可以是任意类型，返回结果见下表：
| 返回类型     | 实例                                                                             |
| -------------| ---------------------------------------------------------------------------------|
| 'underfined' | typeof 未声明变量 / typeof undefined                                             |
| 'boolbean'   | typeof true/typeof false                                                         |
| 'string'     | typeof "1"                                                                       | 
| 'number'     | typeof 1 /typeof NaN                                                             |
| 'object'     | typeof [] / typeof {} / typeof null / typeof /^a*/ / typeof new Date() 等引用类型|
| 'function'   | typeof function(){}                                                              |


