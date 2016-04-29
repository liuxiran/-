
###js的数据类型

js的数据类型有6种，分别是 Undefined、Null、Boolbean、Number、String(简单类型)和Object(引用类型)

* Undefined

  var a               //"undefined",未初始化的变量会自动赋予undefined的值。

  typeof b            //"undefined",未声明的变量获取类型时，也是undefined。
* Null
Null类型只有一个特殊值，null，表示一个空对象指针。保存对象的变量在真正保存对象之前，声明为null。
* Boolbean
  该类型的字面量只有两个值：true和false，区分大小写。和其他类型的值之间的转化关系如下表：

  | 数据类型       | 转换为true的值                 | 转化为false的值    |
  | ---------------|:------------------------------:|:------------------:|
  | Boolbean       | true                           | false              |
  | String         | 任何非空字符串                 | " "                |
  | Number         | 任何非零数字值（包括无穷大）   | 0和NaN             |
  | Object         | 任何对象                       | null               |
  | Undefined      | 无                             | undefined          | 
  Boolbean类型的转化函数：Boolbean()
* 关于Number、String和Object类型，后续会有专门的整理文档。

###获取变量数据类型的方法

* 常用来获取变量数据类型的方法是typeof：是一个一元运算，放在运算数之前，运算数可以是任意类型，返回结果见下表：

  | 返回类型       | 实例                                                                          |
  | ---------------|:-----------------------------------------------------------------------------:|
  | 'underfined'   | typeof 未声明变量、typeof undefined                                           |
  | 'boolbean'     | typeof true、typeof false                                                     |
  | 'string'       | typeof "1"                                                                    |
  | 'number'       | typeof 1 、typeof NaN                                                         |
  | 'object'       | typeof []、typeof {}、typeof null、typeof /^a*/ 、typeof new Date() 等引用类型| 
  | 'function'     | typeof function(){}                                                           |
* 对于引用类型的变量来说，typeof运算后得到的都是'object'，进一步区分可以用 Object.prototype.toString.call()方法，返回结果见下表

  | 返回结果           | 使用方法                                         |
  | -------------------|:------------------------------------------------:|
  | "[object Array]"   | Object.prototype.toString.call([])               |
  | "[object RegExp]"  | Object.prototype.toString.call(/^a*/)            |
  | "[object Object]"  | Object.prototype.toString.call({})               |
  | "[object Null]"    | Object.prototype.toString.call(null)             |
  | "[object Date]"    | Object.prototype.toString.call(new Date())       | 

  其他的数据类型用此方法也可以区分，返回结果见下表

  | 返回结果            | 使用方法                                         |
  | --------------------|:------------------------------------------------:|
  | "[object Number]"   | Object.prototype.toString.call(45)               |
  | "[object Function]" | Object.prototype.toString.call(function(){})     |
  | "[object Boolean]"  | Object.prototype.toString.call(true)             |
  | "[object Undefined]"| Object.prototype.toString.call(undefined)        |
* instanceof：二元运算符，用来判断左边对象是否是右边类的实例，本意是用来处理复杂关系继承的运算，但可以利用来判断'object'类型的变量的具体类型。

   例如：[1,2] instanceof Array  ----> true



