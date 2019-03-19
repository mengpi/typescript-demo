# TypeScript Use Demo

|更新时间|创建时间|来源|
|--|--|--|
|2019/03/15|2019/03/13|demo|

> 测试时 TypeScript 版本为： `v3.3.33`

## 总结
+ TS 最好的方式是 `自顶往下` 设计.
+ 先有类型，有了整体架构，再开始写代码

## Demo List

### 01* 项目配置

+ [0101-tsconfig-outDir](./demo/0101-tsconfig-outDir) -- 指定输出文件夹
+ [0102-tsconfig-alwaysStrict](./demo/0102-tsconfig-alwaysStrict) -- 输出严格模式
+ [0103-tsconfig-declaration](./demo/0103-tsconfig-declaration) -- 输出 d.ts 设置
+ [0104-tsconfig-module](./demo/0104-tsconfig-module) -- 输出模块的类型

### 02* 基本语法

+ [0201-type](./demo/0201-type) -- 基本类型演示
  + 01.介绍(类型汇总)
  + 02.数组类型
  + 03.元组类型
  + 04.枚举类型
  + 05.void类型
  + 06.null和undefined
  + 07.never
  + 08.object
  + 09.类型断言

+ [0202-interface](./demo/0202-interface) -- 接口
  + 01.基本使用
  + 02.只读属性
  + 03.只读数组
  + 04.可选属性
  + 05.额外的属性检查("泛" 属性)
  + 06.函数型接口
  + 07.可索引的类型(js对数字索引的处理，ts的处理, 字典模式)
  + 08.类类型-实现接口
  + 09.类静态部分与实例部分的区别(构造器签名)
  + 10.继承接口(一个接口可以继承多个接口)
  + 11.混合类型(接口作为函数和对象[函数对象]使用--第三方库可以这样使用)
  + 12.继承类(接口继承带有私有属性的类, 子类实现这个接口)
  
+ [0203-classs](./demo/0203-class)
  + 01.基本使用
  + 02.继承(子类、派生类、父类、基类、超类、重写、super)
  + 03.默认为 public
  + 04.私有属性和方法(private)
  + 05.保护类型(protecte)
  + 06.只读类型(readonly)
  + 07.存取器(get set)
  + 08.静态属性和方法(static)
  + 09.抽象类(abstract, 指定类型的实现，和类实现接口的相似性)
  + 10.构造函数
  + 11.将类作为接口使用

+ [0204-function](./demo/0204-function)
  + 01.介绍
  + 02.为函数定义类型(函数接收参数类型，返回类型)
  + 03.书写完整函数类型(完整例子)
  + 04.推断类型(给函数指定函数类型，让函数的参数根据类型推断)
  + 05.可选参数和默认参数(函数参数的 ? 和 =)
  + 06.函数剩余参数(剩余参数如何处理)
  + 07.this和监听函数(Notice: 和文档案例有出入)
  + 08.this参数在回调函数里(Notice: 看不懂，选择性略过)
  + 09.重载(重载与函数实体)

+ [0205-generics](./demo/0205-generics)
  + 01.泛型介绍
  + 02.泛型变量
  + 03.泛型类型
  + 04.泛型类
  + 05.泛型约束
  + 06.在泛型约束中使用类型参数
  + 07.在泛型里使用类类型

+ [0206-enums](./demo/0206-enums)
  + 01.数字枚举
  + 02.字符串枚举
  + 03.异构枚举(枚举成员有类型有数字和字符串的姿势)
  + 04.计算的和常量成员(默认赋值、指定值、简写方式、赋值使用运算符，转换二进制规则)
  + 05.联合枚举与枚举成员的类型(枚举的成员成为了类型，此时 某些成员只能是枚举成员的值)
  + 06.运行时的枚举(枚举在运行时是存在的)
  + 07.反向映射(反向映射的条件, name -> value && value -> name)
  + 08.const 枚举(让枚举功能消失在.js文件中)
  + 09.外部枚举(命名空间里面导出 declear 的枚举)

+ [0207-type-inference](./demo/0207-type-inference)
  + 01.基本推论
  + 02.最佳通用类型(那个才是 MVP)
  + 03.上下文类型

+ [0208-type-compatibility](./demo/0208-type-compatibility)
  + 01.兼容性全局介绍
  + 02.关于可靠性的注意事项(接口和值赋值时如何处理、函数参数如何处理)
  + 03.函数参数双向协变(函数参数检查时原理为什么这样)
  + 04.可选参数及剩余参数，为什么要这样处理
  + 05.枚举(枚举对象互相赋值是如何检查的)
  + 06.类(类之间赋值是如何检查的)
  + 07.泛型(泛型为什么要这样处理)

+ [0209-advanced-types](./demo/0209-advanced-types)(高级类型 **)
  + 01.交叉类型(类型合并)
  + 02.联合类型
  + 03.类型包含与区分类型
  + 04.用户自定义的类型保护
  + 05.typeof 类型保护
  + 06.intanceof 类型保护
  + 07.可以为 null 的类型
  + 08.可选参数和可选属性
  + 09.类型保护和类型断言
  + 10.类型别名
  + 11.接口 vs. 类型别名
  + 12.字符串字面量类型
  + 13.数字字面量类型
  + 14.枚举成员类型
  + 15.可辨识类型(标签联合|代数数据类型): 可以合并单例类型、联合类型、类型保护和类型别名.
  + 16.完整性检查
  + 17.多态的 this 类型
  + 18.索引类型(keyof T: `索引类型查询操作符`, T[K]：`索引访问操作符`)
  + 19.`所有类型`和`字符串索引签名`
  + 20.映射类型
  + 21.由映射类型进行推断
  + 22.条件类型介绍(T extends U ? X : Y)
  + 23.类型判断中使用类型推论(type 中使用 `？:`)

+ [0210-Symbols](./demo/0210-Symbols)
  + 01.介绍(tsconfig.json配置)
  + 02.Symbol方法

+ [0211-iterators-and-generators](./demo/0211-iterators-and-generators)
  + 01.可迭代性说明( `Symbol.iterator` )
  + 02.`for...of` 语句
  + 03.`for...of Vs. for...in` 语句.
  + 04.代码生成原则( `target` )

+ [0212-modules](./demo/0212-modules)
  + 01.介绍(export import)
  + 02.导出声明(export、导出声明、导出语句)
  + 03.重新导出(export as from)
  + 04.导入
    + 导入一个模块中的某个导出内容(`{}`)
    + 将整个模块导入到一个变量，并通过它来访问模块的导出部分(`* as`)
  + 05.具有副作用的导入模块
  + 06.默认导出
  + 07.export = 和 import = require()
  + 08.外部模块
  + 09.外部模块简写
  + 10.模块声明通配符
  + 11.创建模块结构指导(AAA, 危险信号)

+ [0213-namespace](./demo/0213-namespace)
  + 01.介绍(外部模块：模块(module)、内部模块：命名空间namespace)
  + 02.命名空间里面使用export
  + 03.别名
  + 04.外部命名空间(D3的写法)

+ [021302-multi-file-namespace-module-demo](./demo/021302-multi-file-namespace-module-demo)(多文件+命名空间+模块案例。需要 reference, 注意 `export namespace foo`)
+ [021303-multi-file-module-demo](./demo/021303-multi-file-module-demo)(多文件+模块)

+ [0214-namespaces-and-modules](./demo/0214-namespaces-and-modules)
  + 01.没 `d.ts` 或者 `.js` 写的第三方模块，在 TS 使用时如何阻止报错.
  + 不必要的命名空间(shapes.Shapes、以及改进例子)


## 03* 配合工具使用


## blue cat and archness 3000 question ?

+ TS 中使用了命名空间，通过命名空间使用
需要导出, 例子: 0205-generics > 07