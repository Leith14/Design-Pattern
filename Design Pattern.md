# 设计模式学习导读 (3讲)

## 01 | 为什么说每个程序员都要尽早地学习并掌握设计模式相关知识？



## 02 | 从哪些维度评判代码质量的好坏？如何具备写出高质量代码的能力？

## 可维护性（maintainability）

所以，从正面去分析一个代码是否易维护稍微有点难度。不过，我们可以从侧面上给出一个比较主观但又比较准确的感受。如果 bug 容易修复，修改、添加功能能够轻松完成，那我们就可以主观地认为代码对我们来说易维护。相反，如果修改一个 bug，修改、添加一个功能，需要花费很长的时间，那我们就可以主观地认为代码对我们来说不易维护。

## 可读性（readability）

软件设计大师 Martin Fowler 曾经说过：“Any fool can write code that a computer can understand. Good programmers write code that humans can understand.”翻译成中文就是：“任何傻瓜都会编写计算机能理解的代码。好的程序员能够编写人能够理解的代码。”Google 内部甚至专门有个认证就叫作 Readability。只有拿到这个认证的工程师，才有资格在 code review 的时候，批准别人提交代码。可见代码的可读性有多重要，毕竟，代码被阅读的次数远远超过被编写和执行的次数。我个人认为，`代码的可读性应该是评价代码质量最重要的指标之一`。

## 可扩展性（extensibility）



## 灵活性（flexibility）

- 当我们添加一个新的功能代码的时候，原有的代码已经预留好了扩展点，我们不需要修改原有的代码，只要在扩展点上添加新的代码即可。这个时候，我们除了可以说代码易扩展，还可以说代码写得好灵活。
- 当我们要实现一个功能的时候，发现原有代码中，已经抽象出了很多底层可以复用的模块、类等代码，我们可以拿来直接使用。这个时候，我们除了可以说代码易复用之外，还可以说代码写得好灵活。
- 当我们使用某组接口的时候，如果这组接口可以应对各种使用场景，满足各种不同的需求，我们除了可以说接口易用之外，还可以说这个接口设计得好灵活或者代码写得好灵活。

从刚刚举的场景来看，如果一段代码易扩展、易复用或者易用，我们都可以称这段代码写得比较灵活。所以，灵活这个词的含义非常宽泛，很多场景下都可以使用。

## 简洁性（simplicity）

有一条非常著名的设计原则，你一定听过，那就是 KISS 原则：`“Keep It Simple，Stupid”`。这个原则说的意思就是，尽量保持代码简单。代码简单、逻辑清晰，也就意味着易读、易维护。我们在编写代码的时候，往往也会把简单、清晰放到首位。

不过，很多编程经验不足的程序员会觉得，简单的代码没有技术含量，喜欢在项目中引入一些复杂的设计模式，觉得这样才能体现自己的技术水平。实际上，`思从深而行从简，真正的高手能云淡风轻地用最简单的方法解决最复杂的问题。这也是一个编程老手跟编程新手的本质区别之一`。



## 可复用性（reusability）

比如，当讲到面向对象特性的时候，我们会讲到继承、多态存在的目的之一，就是为了提高代码的可复用性；当讲到设计原则的时候，我们会讲到单一职责原则也跟代码的可复用性相关；当讲到重构技巧的时候，我们会讲到解耦、高内聚、模块化等都能提高代码的可复用性。

可见，可复用性也是一个非常重要的代码评价标准，是很多设计原则、思想、模式等所要达到的最终效果。实际上，代码可复用性跟 DRY（Don’t Repeat Yourself）这条设计原则的关系挺紧密的，所以，在后面的章节中，当我们讲到 DRY 设计原则的时候，我还会讲更多代码复用相关的知识，比如，“有哪些编程方法可以提高代码的复用性”等。



## 可测试性（testability）



## 如何才能写出高质量的代码？

比如，面向对象中的继承、多态能让我们写出可复用的代码；编码规范能让我们写出可读性好的代码；设计原则中的单一职责、DRY、基于接口而非实现、里式替换原则等，可以让我们写出可复用、灵活、可读性好、易扩展、易维护的代码；设计模式可以让我们写出易扩展的代码；持续重构可以时刻保持代码的可维护性等等。具体这些编程方法论是如何提高代码的可维护性、可读性、可扩展性等等的呢？我们在后面的课程中慢慢来学习。



## 重点回顾

今天的内容到此就讲完了。我们来一起回顾一下，你需要重点掌握的几个知识点。

- 如何评价代码质量的高低？

代码质量的评价有很强的主观性，描述代码质量的词汇也有很多，比如可读性、可维护性、灵活、优雅、简洁等，这些词汇是从不同的维度去评价代码质量的。它们之间有互相作用，并不是独立的，比如，代码的可读性好、可扩展性好就意味着代码的可维护性好。代码质量高低是一个综合各种因素得到的结论。我们并不能通过单一的维度去评价一段代码的好坏。

- 最常用的评价标准有哪几个？

最常用到几个评判代码质量的标准是：可维护性、可读性、可扩展性、灵活性、简洁性、可复用性、可测试性。其中，`可维护性、可读性、可扩展性`又是提到最多的、最重要的三个评价标准。

- 如何才能写出高质量的代码？

  要写出高质量代码，我们就需要掌握一些更加细化、更加能落地的编程方法论，这就包含面向对象设计思想、设计原则、设计模式、编码规范、重构技巧等等，这也是我们后面课程学习的重点。

## 03 | 面向对象、设计原则、设计模式、编程规范、重构，这五者有何关系？

![img](https://static001.geekbang.org/resource/image/f3/d3/f3262ef8152517d3b11bfc3f2d2b12d3.png)

# 设计原则与思想：面向对象 (11讲)

[04 | 理论一：当谈论面向对象的时候，我们到底在谈论什么？](https://time.geekbang.org/column/article/161575)

面向对象编程的英文缩写是 `OOP`，全称是 `Object Oriented Programming`。对应地，面向对象编程语言的英文缩写是 `OOPL`，全称是 `Object Oriented Programming Language`。

- 面向对象编程是一种编程范式或编程风格。它以类或对象作为组织代码的基本单元，并将**封装、抽象、继承、多态**四个特性，作为代码设计和实现的基石 。

- 面向对象编程语言是支持类或对象的语法机制，并有现成的语法机制，能方便地实现面向对象编程四大特性（**封装、抽象、继承、多态**）的编程语言。

[05 | 理论二：封装、抽象、继承、多态分别可以解决哪些编程问题？](https://time.geekbang.org/column/article/161114)

[06 | 理论三：面向对象相比面向过程有哪些优势？面向过程真的过时了吗？](https://time.geekbang.org/column/article/161587)

[07 | 理论四：哪些代码设计看似是面向对象，实际是面向过程的？](https://time.geekbang.org/column/article/164907)

[08 | 理论五：接口vs抽象类的区别？如何用普通的类模拟抽象类和接口？](https://time.geekbang.org/column/article/165103)

[09 | 理论六：为什么基于接口而非实现编程？有必要为每个类都定义接口吗？](https://time.geekbang.org/column/article/165114)

[10 | 理论七：为何说要多用组合少用继承？如何决定该用组合还是继承？](https://time.geekbang.org/column/article/169593)

[11 | 实战一（上）：业务开发常用的基于贫血模型的MVC架构违背OOP吗？](https://time.geekbang.org/column/article/169600)

[12 | 实战一（下）：如何利用基于充血模型的DDD开发一个虚拟钱包系统？](https://time.geekbang.org/column/article/169631)

[13 | 实战二（上）：如何对接口鉴权这样一个功能开发做面向对象分析？](https://time.geekbang.org/column/article/171760)

[14 | 实战二（下）：如何利用面向对象设计和编程开发接口鉴权功能？](https://time.geekbang.org/column/article/171767)

# 设计原则与思想：设计原则 (12讲)

[15 | 理论一：对于单一职责原则，如何判定某个类的职责是否够“单一”？](https://time.geekbang.org/column/article/171771)

[16 | 理论二：如何做到“对扩展开放、修改关闭”？扩展和修改各指什么？](https://time.geekbang.org/column/article/176075)

[17 | 理论三：里式替换（LSP）跟多态有何区别？哪些代码违背了LSP？](https://time.geekbang.org/column/article/177110)

[18 | 理论四：接口隔离原则有哪三种应用？原则中的“接口”该如何理解？](https://time.geekbang.org/column/article/177442)

[19 | 理论五：控制反转、依赖反转、依赖注入，这三者有何区别和联系？](https://time.geekbang.org/column/article/177444)

[20 | 理论六：我为何说KISS、YAGNI原则看似简单，却经常被用错？](https://time.geekbang.org/column/article/177448)

[21 | 理论七：重复的代码就一定违背DRY吗？如何提高代码的复用性？](https://time.geekbang.org/column/article/179607)

[22 | 理论八：如何用迪米特法则（LOD）实现“高内聚、松耦合”？](https://time.geekbang.org/column/article/179615)

[23 | 实战一（上）：针对业务系统的开发，如何做需求分析和设计？](https://time.geekbang.org/column/article/182001)

[24 | 实战一（下）：如何实现一个遵从设计原则的积分兑换系统？](https://time.geekbang.org/column/article/183007)

[25 | 实战二（上）：针对非业务的通用框架开发，如何做需求分析和设计？](https://time.geekbang.org/column/article/179644)

[26 | 实战二（下）：如何实现一个支持各种统计规则的性能计数器？](https://time.geekbang.org/column/article/179673)

# 设计原则与思想：规范与重构 (11讲)

[27 | 理论一：什么情况下要重构？到底重构什么？又该如何重构？](https://time.geekbang.org/column/article/179679)

[28 | 理论二：为了保证重构不出错，有哪些非常能落地的技术手段？](https://time.geekbang.org/column/article/185684)

[29 | 理论三：什么是代码的可测试性？如何写出可测试性好的代码？](https://time.geekbang.org/column/article/186691)

[30 | 理论四：如何通过封装、抽象、模块化、中间层等解耦代码？](https://time.geekbang.org/column/article/187761)

[31 | 理论五：让你最快速地改善代码质量的20条编程规范（上）](https://time.geekbang.org/column/article/188622)

[32 | 理论五：让你最快速地改善代码质量的20条编程规范（中）](https://time.geekbang.org/column/article/188857)

[33 | 理论五：让你最快速地改善代码质量的20条编程规范（下）](https://time.geekbang.org/column/article/188882)

[34 | 实战一（上）：通过一段ID生成器代码，学习如何发现代码质量问题](https://time.geekbang.org/column/article/190979)

[35 | 实战一（下）：手把手带你将ID生成器代码从“能用”重构为“好用”](https://time.geekbang.org/column/article/191621)

[36 | 实战二（上）：程序出错该返回啥？NULL、异常、错误码、空对象？](https://time.geekbang.org/column/article/191642)

[37 | 实战二（下）：重构ID生成器项目中各函数的异常处理代码](https://time.geekbang.org/column/article/191647)

# 设计原则与思想：总结课 (3讲)



[38 | 总结回顾面向对象、设计原则、编程规范、重构技巧等知识点](https://time.geekbang.org/column/article/193093)

[39 | 运用学过的设计原则和思想完善之前讲的性能计数器项目（上）](https://time.geekbang.org/column/article/193221)

[40 | 运用学过的设计原则和思想完善之前讲的性能计数器项目（下）](https://time.geekbang.org/column/article/193555)

# 设计模式与范式：创建型 (7讲)



[41 | 单例模式（上）：为什么说支持懒加载的双重检测不比饿汉式更优？](https://time.geekbang.org/column/article/194035)

[42 | 单例模式（中）：我为什么不推荐使用单例模式？又有何替代方案？](https://time.geekbang.org/column/article/194068)

[43 | 单例模式（下）：如何设计实现一个集群环境下的分布式单例模式？](https://time.geekbang.org/column/article/196790)

[44 | 工厂模式（上）：我为什么说没事不要随便用工厂模式创建对象？](https://time.geekbang.org/column/article/197254)

[45 | 工厂模式（下）：如何设计实现一个Dependency Injection框架？](https://time.geekbang.org/column/article/198614)

[46 | 建造者模式：详解构造函数、set方法、建造者模式三种对象创建方式](https://time.geekbang.org/column/article/199674)

[47 | 原型模式：如何最快速地clone一个HashMap散列表？](https://time.geekbang.org/column/article/200786)

# 设计模式与范式：结构型 (8讲)



[48 | 代理模式：代理在RPC、缓存、监控等场景中的应用](https://time.geekbang.org/column/article/201823)

[49 | 桥接模式：如何实现支持不同类型和渠道的消息推送系统？](https://time.geekbang.org/column/article/202786)

[50 | 装饰器模式：通过剖析Java IO类库源码学习装饰器模式](https://time.geekbang.org/column/article/204845)

[51 | 适配器模式：代理、适配器、桥接、装饰，这四个模式有何区别？](https://time.geekbang.org/column/article/205912)

[52 | 门面模式：如何设计合理的接口粒度以兼顾接口的易用性和通用性？](https://time.geekbang.org/column/article/206409)

[53 | 组合模式：如何设计实现支持递归遍历的文件系统目录树结构？](https://time.geekbang.org/column/article/207456)

[54 | 享元模式（上）：如何利用享元模式优化文本编辑器的内存占用？](https://time.geekbang.org/column/article/208572)

[55 | 享元模式（下）：剖析享元模式在Java Integer、String中的应用](https://time.geekbang.org/column/article/209343)

# 设计模式与范式：行为型 (18讲)



[56 | 观察者模式（上）：详解各种应用场景下观察者模式的不同实现方式](https://time.geekbang.org/column/article/210170)

[57 | 观察者模式（下）：如何实现一个异步非阻塞的EventBus框架？](https://time.geekbang.org/column/article/211239)

[58 | 模板模式（上）：剖析模板模式在JDK、Servlet、JUnit等中的应用](https://time.geekbang.org/column/article/212049)

[59 | 模板模式（下）：模板模式与Callback回调函数有何区别和联系？](https://time.geekbang.org/column/article/212802)

[60 | 策略模式（上）：如何避免冗长的if-else/switch分支判断代码？](https://time.geekbang.org/column/article/214014)

[61 | 策略模式（下）：如何实现一个支持给不同大小文件排序的小程序？](https://time.geekbang.org/column/article/215132)

[62 | 职责链模式（上）：如何实现可灵活扩展算法的敏感信息过滤框架？](https://time.geekbang.org/column/article/216278)

[63 | 职责链模式（下）：框架中常用的过滤器、拦截器是如何实现的？](https://time.geekbang.org/column/article/217395)

[64 | 状态模式：游戏、工作流引擎中常用的状态机是如何实现的？](https://time.geekbang.org/column/article/218375)

[65 | 迭代器模式（上）：相比直接遍历集合数据，使用迭代器有哪些优势？](https://time.geekbang.org/column/article/219290)

[66 | 迭代器模式（中）：遍历集合的同时，为什么不能增删集合元素？](https://time.geekbang.org/column/article/219964)

[67 | 迭代器模式（下）：如何设计实现一个支持“快照”功能的iterator？](https://time.geekbang.org/column/article/221269)

[68 | 访问者模式（上）：手把手带你还原访问者模式诞生的思维过程](https://time.geekbang.org/column/article/221852)

[69 | 访问者模式（下）：为什么支持双分派的语言不需要访问者模式？](https://time.geekbang.org/column/article/222762)

[70 | 备忘录模式：对于大对象的备份和恢复，如何优化内存和时间的消耗？](https://time.geekbang.org/column/article/223947)

[71 | 命令模式：如何利用命令模式实现一个手游后端架构？](https://time.geekbang.org/column/article/224549)

[72 | 解释器模式：如何设计实现一个自定义接口告警规则功能？](https://time.geekbang.org/column/article/225904)

[73 | 中介模式：什么时候用中介模式？什么时候用观察者模式？](https://time.geekbang.org/column/article/226710)

# 设计模式与范式：总结课 (2讲)



[74 | 总结回顾23种经典设计模式的原理、背后的思想、应用场景等](https://time.geekbang.org/column/article/227452)

[75 | 在实际的项目开发中，如何避免过度设计？又如何避免设计不足？](https://time.geekbang.org/column/article/229157)

# 开源与项目实战：开源实战 (14讲)



[76 | 开源实战一（上）：通过剖析Java JDK源码学习灵活应用设计模式](https://time.geekbang.org/column/article/229996)

[77 | 开源实战一（下）：通过剖析Java JDK源码学习灵活应用设计模式](https://time.geekbang.org/column/article/230708)

[78 | 开源实战二（上）：从Unix开源开发学习应对大型复杂项目开发](https://time.geekbang.org/column/article/232061)

[79 | 开源实战二（中）：从Unix开源开发学习应对大型复杂项目开发](https://time.geekbang.org/column/article/232427)

[80 | 开源实战二（下）：从Unix开源开发学习应对大型复杂项目开发](https://time.geekbang.org/column/article/232687)

[81 | 开源实战三（上）：借Google Guava学习发现和开发通用功能模块](https://time.geekbang.org/column/article/233742)

[82 | 开源实战三（中）：剖析Google Guava中用到的几种设计模式](https://time.geekbang.org/column/article/234758)

[83 | 开源实战三（下）：借Google Guava学习三大编程范式中的函数式编程](https://time.geekbang.org/column/article/235334)

[84 | 开源实战四（上）：剖析Spring框架中蕴含的经典设计思想或原则](https://time.geekbang.org/column/article/236935)

[85 | 开源实战四（中）：剖析Spring框架中用来支持扩展的两种设计模式](https://time.geekbang.org/column/article/237810)

[86 | 开源实战四（下）：总结Spring框架用到的11种设计模式](https://time.geekbang.org/column/article/238418)

[87 | 开源实战五（上）：MyBatis如何权衡易用性、性能和灵活性？](https://time.geekbang.org/column/article/239239)

[88 | 开源实战五（中）：如何利用职责链与代理模式实现MyBatis Plugin？](https://time.geekbang.org/column/article/240147)

[89 | 开源实战五（下）：总结MyBatis框架中用到的10种设计模式](https://time.geekbang.org/column/article/240971)

# 开源与项目实战：项目实战 (9讲)



[90 | 项目实战一：设计实现一个支持各种算法的限流框架（分析）](https://time.geekbang.org/column/article/242314)

[91 | 项目实战一：设计实现一个支持各种算法的限流框架（设计）](https://time.geekbang.org/column/article/243175)

[92 | 项目实战一：设计实现一个支持各种算法的限流框架（实现）](https://time.geekbang.org/column/article/243961)

[93 | 项目实战二：设计实现一个通用的接口幂等框架（分析）](https://time.geekbang.org/column/article/245022)

[94 | 项目实战二：设计实现一个通用的接口幂等框架（设计）](https://time.geekbang.org/column/article/245788)

[95 | 项目实战二：设计实现一个通用的接口幂等框架（实现）](https://time.geekbang.org/column/article/246379)

[96 | 项目实战三：设计实现一个支持自定义规则的灰度发布组件（分析）](https://time.geekbang.org/column/article/247776)

[97 | 项目实战三：设计实现一个支持自定义规则的灰度发布组件（设计）](https://time.geekbang.org/column/article/248714)

[98 | 项目实战三：设计实现一个支持自定义规则的灰度发布组件（实现）](https://time.geekbang.org/column/article/249369)

# 开源与项目实战：总结课 (2讲)



[99 | 总结回顾：在实际软件开发中常用的设计思想、原则和模式](https://time.geekbang.org/column/article/250942)

[100 | 如何将设计思想、原则、模式等理论知识应用到项目中？](https://time.geekbang.org/column/article/251930)

# 不定期加餐 (11讲)



[加餐一 | 用一篇文章带你了解专栏中用到的所有Java语法](https://time.geekbang.org/column/article/166698)

[加餐二 | 设计模式、重构、编程规范等相关书籍推荐](https://time.geekbang.org/column/article/172690)

[春节特别加餐 | 王争：如何学习《设计模式之美》专栏？](https://time.geekbang.org/column/article/192789)

[加餐三 | 聊一聊Google是如何做Code Review的](https://time.geekbang.org/column/article/252937)

[加餐四 | 聊一聊Google那些让我快速成长的地方](https://time.geekbang.org/column/article/254190)

[加餐五 | 听一听小争哥对Google工程师文化的解读](https://time.geekbang.org/column/article/255037)

[加餐六 | 什么才是所谓的编程能力？如何考察一个人的编程能力？](https://time.geekbang.org/column/article/255697)

[加餐七 | 基础学科的知识如何转化成实际的技术生产力？](https://time.geekbang.org/column/article/256866)

[加餐八 | 程序员怎么才能让自己走得更高、更远？](https://time.geekbang.org/column/article/257513)

[加餐九 | 作为面试官或候选人，如何面试或回答设计模式问题？](https://time.geekbang.org/column/article/258207)

[加餐十 | 如何接手一坨烂业务代码？如何在烂业务代码中成长？](https://time.geekbang.org/column/article/259489)

# 结束语 (1讲)

