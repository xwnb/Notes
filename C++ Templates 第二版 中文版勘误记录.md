# 《C++ Templates 第2版 中文版》 勘误记录

这是关于一本学习 C++ 模板的书籍，内容和水准都很高，正在努力啃，而且使用了很多 modern C++ 的内容，以下是个人阅读中文版过程中发现的一些疑点及错误的记录（PS: 中文版大佬翻译质量很可以，每次读到国内翻译的书，都不得不感谢这些巨佬们用爱发电，给菜鸡赏饭吃。PSS: 不得不再次吐槽也是忍不住次次吐槽也是唯一吐槽过的一本中文版书籍，那就是 C++ 并行编程实战 中文版 **第一版** **第一版** **第一版** 的译者们。真的，如果不热爱技术没有责任心只是为了刷KPI或者赚钱或者刷知名度等等，不如不翻。PSSS：我都怀疑机翻都翻译不出这种十句有三句错误，二句不同，剩下五句不明所以的中文字）。如有不当，谢谢指正。-- by Wayne

#### P58: 意思不明：第 5.3 节最后一段
+ 译文：我们始终建议使用 this-> 或者 Base<T>:: 来限定修饰在基类中的声明，并在某种程度上依赖于模板参数的任何符号
+ 原文：we recommend that you always qualify any symbol that is declared in a base that is somehow
dependent on a template parameter with this-> or Base<T>::.
+ **NOTE: 翻译似乎哪里差点意思**

#### P173: 错译：第 12.5.3 节该页最后一段
+ 译文：……，并在后面**紧跟着角括号**的情况下，……
+ 原文：…… that **is not followed by angle brackets**……
+ **NOTE: 没有跟着**

#### P176：错译：表格中 受限名称 一行
+ 译文： ……，但是单独一个 class_mem（即前面没有 -> 等）**就是一个受限名称**，……
+ 原文：However, just class_mem in a context that is implicitly equivalent to
this->class_mem **is not a qualified name**
+ **NOTE: 不是一个受限名称**

#### P271：typo: 倒数第二段
+ 译文：t<A1 const>(A1 const*, A1 const*, A1 const* = 0)
+ 原文：T<A1 const>(A1 const*, A1 const*, A1 const* = 0)

#### P319：意思不对；歧义词：第一段
+ 译文：constexpr 静态数据成员就**更不能使用了**，因为只允许浮点类型和其他**文本类型**
+ 原文：constexpr static data members **are slightly more general**, allowing floating-point types as well
as other **literal types**:
+ **NOTE: 意思应该是：constexpr 静态数据成员稍微更通用点 而不是不能使用；literal types 惯用词应该为 字面量**

#### P341：存疑：第二节上面一段
+ 译文/原文：需要注意的是，传递给 **func()** 的调用
+ **NOTE: 这里原文也是 func()， 但是并未找到 func() 函数，怀疑是指 test()**

#### P342：存疑：第19.4.2节上面两段
+ 译文/原文：IsConvertibleT<. . . > 
+ **NOTE: 这里似乎并为提到 IsConvertibleT，包括代码，这一节都在讲 IsDefaultConstructibleT。**

#### P134，P242，P343，P382：用词不一致：helper
+ 译文：**帮助**模板，**辅助**类模板，**helper** VoidT，**helper** 类
+ **NOTE: 多种风格，但不影响阅读**

#### P382: typo：中间一段文本中
+ 译文：isRandomAccessiator
+ **NOTE: 笔误，应该是 IsRandomAccessiator**

#### P382：用词：倒数第二行
+ 译文：EnableIfT<...>::Type（**因此** EnableIf<...>）
+ 原文：EnableIfT<...>::Type (**and therefore** EnableIf<...>)
+ **NOTE: 这里翻译成 即？也就是？ 意思是不是更通顺**

#### P382：用词：倒数第二行
+ 译文：EnableIfT<...>::Type（**因此** EnableIf<...>）
+ 原文：EnableIfT<...>::Type (**and therefore** EnableIf<...>)
+ **NOTE: 翻译成 即？也就是？**

#### P388：存疑：第20.4节第一段末
+ 译文：只要键类型提供=运算符
+ 原文：provide just an equality operator
+ **NOTE: 应该是 ==（相等）运算符，=运算符应该是赋值运算符**

#### P390：存疑：第20.4.2节第一段
+ 译文：向前推进若干**步骤**
+ 原文：which advances an iterator by some number of steps. 
+ **NOTE: 拗口，步骤 -> 步，向前推进若干步**

#### P390：用词：第21.2.3节
+ 译文：门面模式
+ 原文：Facade Pattern
+ **NOTE: 设计模式里称 外观模式 比较常见**

#### P410：存疑：第2节
+ 原文/译文：以上 ListNodeIterator 实现的一个缺点是，作为公共接口，我们被要求公开 dereference()、**advance()** 和 equals() 运算
+ **NOTE：不清楚是不是因为代码示例不完整的缘故，结合上下文，如果是针对 ListNodeIterator 并没有 advance() 接口**

#### P419：图片未更新：图21.4
+ 原文/译文：图片中类图，使用 **typedef DefaultPolicy1 P1; **等。
+ **NOTE：该图片和第一版的图16.1一致，但书中代码及文字均已经更新使用 using 来做模板别名，图片未更新，依然用 typedef 。**

#### P419：未找到源码 inherit/namedtmpl.cpp：第21.5节上面一段
+ 原文/译文：在 **inherit/namedtmpl.cpp** 中可以找到完整的示例。
+ **NOTE：并未在第二版的源码文件中找到这份文件，但这是第一版的一份源码文件**

#### P419：用词：第2点脚注
+ 译文：因为它们被定义在封入它们的类的内容中
+ 原文：because they are defined in the body of their **enclosing class**
+ **NOTE：差点意思，且书中其他几处 enclosing class 使用的是 封闭类 翻译**

#### P454：typo
+ **NOTE：Tranform 应该是 Transform**

#### P469：未找到源码：第21.5节上面一段
+ 原文/译文：完整的构造函数声明在 **tuples/tuple.hpp** 中
+ **NOTE：并未在源码文件中找到这份文件**

#### P471：补充：译注
+ **NOTE：编译倒没问题，这里的问题是运行时，空元组重载了第一个方法，只能输出半个开括号**

未完待续……
