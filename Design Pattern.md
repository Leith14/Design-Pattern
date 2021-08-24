# 设计模式学习导读 (3讲)

## 01 | 为什么说每个程序员都要尽早地学习并掌握设计模式相关知识？



## 02 | 从哪些维度评判代码质量的好坏？如何具备写出高质量代码的能力？

### 可维护性（maintainability）



所以，从正面去分析一个代码是否易维护稍微有点难度。不过，我们可以从侧面上给出一个比较主观但又比较准确的感受。如果 bug 容易修复，修改、添加功能能够轻松完成，那我们就可以主观地认为代码对我们来说易维护。相反，如果修改一个 bug，修改、添加一个功能，需要花费很长的时间，那我们就可以主观地认为代码对我们来说不易维护。

### 可读性（readability）

软件设计大师 Martin Fowler 曾经说过：“Any fool can write code that a computer can understand. Good programmers write code that humans can understand.”翻译成中文就是：“任何傻瓜都会编写计算机能理解的代码。好的程序员能够编写人能够理解的代码。”Google 内部甚至专门有个认证就叫作 Readability。只有拿到这个认证的工程师，才有资格在 code review 的时候，批准别人提交代码。可见代码的可读性有多重要，毕竟，代码被阅读的次数远远超过被编写和执行的次数。我个人认为，`代码的可读性应该是评价代码质量最重要的指标之一`。

### 可扩展性（extensibility）

### 灵活性（flexibility）

- 当我们添加一个新的功能代码的时候，原有的代码已经预留好了扩展点，我们不需要修改原有的代码，只要在扩展点上添加新的代码即可。这个时候，我们除了可以说代码易扩展，还可以说代码写得好灵活。
- 当我们要实现一个功能的时候，发现原有代码中，已经抽象出了很多底层可以复用的模块、类等代码，我们可以拿来直接使用。这个时候，我们除了可以说代码易复用之外，还可以说代码写得好灵活。
- 当我们使用某组接口的时候，如果这组接口可以应对各种使用场景，满足各种不同的需求，我们除了可以说接口易用之外，还可以说这个接口设计得好灵活或者代码写得好灵活。

从刚刚举的场景来看，如果一段代码易扩展、易复用或者易用，我们都可以称这段代码写得比较灵活。所以，灵活这个词的含义非常宽泛，很多场景下都可以使用。

### 简洁性（simplicity）

有一条非常著名的设计原则，你一定听过，那就是 KISS 原则：`“Keep It Simple，Stupid”`。这个原则说的意思就是，尽量保持代码简单。代码简单、逻辑清晰，也就意味着易读、易维护。我们在编写代码的时候，往往也会把简单、清晰放到首位。

不过，很多编程经验不足的程序员会觉得，简单的代码没有技术含量，喜欢在项目中引入一些复杂的设计模式，觉得这样才能体现自己的技术水平。实际上，`思从深而行从简，真正的高手能云淡风轻地用最简单的方法解决最复杂的问题。这也是一个编程老手跟编程新手的本质区别之一`。

### 可复用性（reusability）

比如，当讲到面向对象特性的时候，我们会讲到继承、多态存在的目的之一，就是为了提高代码的可复用性；当讲到设计原则的时候，我们会讲到单一职责原则也跟代码的可复用性相关；当讲到重构技巧的时候，我们会讲到解耦、高内聚、模块化等都能提高代码的可复用性。

可见，可复用性也是一个非常重要的代码评价标准，是很多设计原则、思想、模式等所要达到的最终效果。实际上，代码可复用性跟 DRY（Don’t Repeat Yourself）这条设计原则的关系挺紧密的，所以，在后面的章节中，当我们讲到 DRY 设计原则的时候，我还会讲更多代码复用相关的知识，比如，“有哪些编程方法可以提高代码的复用性”等。

### 可测试性（testability）

### 如何才能写出高质量的代码？

比如，面向对象中的继承、多态能让我们写出可复用的代码；编码规范能让我们写出可读性好的代码；设计原则中的单一职责、DRY、基于接口而非实现、里式替换原则等，可以让我们写出可复用、灵活、可读性好、易扩展、易维护的代码；设计模式可以让我们写出易扩展的代码；持续重构可以时刻保持代码的可维护性等等。具体这些编程方法论是如何提高代码的可维护性、可读性、可扩展性等等的呢？我们在后面的课程中慢慢来学习。

### 重点回顾

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

实际上，面向对象编程从字面上，按照最简单、最原始的方式来理解，**就是将对象或类作为代码组织的基本单元，来进行编程的一种编程范式或者编程风格**，并不一定需要封装、抽象、继承、多态这四大特性的支持。但是，在进行面向对象编程的过程中，人们不停地总结发现，有了这四大特性，我们就能更容易地实现各种面向对象的代码设计思路。

> 什么是面向对象分析和面向对象设计？

前面我们讲了面向对象编程（OOP），实际上，跟面向对象编程经常放到一块儿来讲的还有另外两个概念，那就是面向对象分析（OOA）和面向对象设计（OOD）。面向对象分析英文缩写是 OOA，全称是 Object Oriented Analysis；面向对象设计的英文缩写是 OOD，全称是 Object Oriented Design。OOA、OOD、OOP 三个连在一起就是面向对象分析、设计、编程（实现），正好是面向对象软件开发要经历的三个阶段。

> 什么是 UML？我们是否需要 UML？

讲到面向对象分析、设计、编程，我们就不得不提到另外一个概念，那就是 UML（Unified Model Language），统一建模语言。很多讲解面向对象或设计模式的书籍，常用它来画图表达面向对象或设计模式的设计思路。

> 重点回顾

1. 什么是面向对象编程？
2. 什么是面向对象编程语言？
3. 如何判定一个编程语言是否是面向对象编程语言？
4. 面向对象编程和面向对象编程语言之间有何关系？
5. 什么是面向对象分析和面向对象设计？

[05 | 理论二：封装、抽象、继承、多态分别可以解决哪些编程问题？](https://time.geekbang.org/column/article/161114)

TODO: Python 是多继承，为什么

而 duck-typing 只有一些动态语言才支持，比如 Python、JavaScript 等。

> 关于封装特性

封装也叫作信息隐藏或者数据访问保护。类通过暴露有限的访问接口，授权外部仅能通过类提供的方式来访问内部信息或者数据。它需要编程语言提供权限访问控制语法来支持，例如 Java 中的 private、protected、public 关键字。封装特性存在的意义，一方面是保护数据不被随意修改，提高代码的可维护性；另一方面是仅暴露有限的必要接口，提高类的易用性

> 关于抽象特性

封装主要讲如何隐藏信息、保护数据，那抽象就是讲如何隐藏方法的具体实现，让使用者只需要关心方法提供了哪些功能，不需要知道这些功能是如何实现的。抽象可以通过接口类或者抽象类来实现，但也并不需要特殊的语法机制来支持。抽象存在的意义，一方面是提高代码的可扩展性、维护性，修改实现不需要改变定义，减少代码的改动范围；另一方面，它也是处理复杂系统的有效手段，能有效地过滤掉不必要关注的信息。

> 关于继承特性

继承是用来表示类之间的 is-a 关系，分为两种模式：单继承和多继承。单继承表示一个子类只继承一个父类，多继承表示一个子类可以继承多个父类。为了实现继承这个特性，编程语言需要提供特殊的语法机制来支持。继承主要是用来解决代码复用的问题。

> 关于多态特性

多态是指子类可以替换父类，在实际的代码运行过程中，调用子类的方法实现。多态这种特性也需要编程语言提供特殊的语法机制来实现，比如继承、接口类、duck-typing。多态可以提高代码的扩展性和复用性，是很多设计模式、设计原则、编程技巧的代码实现基础。



[06 | 理论三：面向对象相比面向过程有哪些优势？面向过程真的过时了吗？](https://time.geekbang.org/column/article/161587)

> 什么是面向过程编程与面向过程编程语言？

理解这两个概念最好的方式是跟面向对象编程和面向对象编程语言进行对比。**相较于面向对象编程以类为组织代码的基本单元，面向过程编程则是以过程（或方法）作为组织代码的基本单元。它最主要的特点就是数据和方法相分离。**相较于面向对象编程语言，面向过程编程语言最大的特点就是不支持丰富的面向对象编程特性，比如继承、多态、封装。

> 面向对象编程相比面向过程编程有哪些优势？

面向对象编程相比起面向过程编程的优势主要有三个:

- 对于大规模复杂程序的开发，程序的处理流程并非单一的一条主线，而是错综复杂的网状结构。面向对象编程比起面向过程编程，更能应对这种复杂类型的程序开发。
- 面向对象编程相比面向过程编程，具有更加丰富的特性（封装、抽象、继承、多态）。利用这些特性编写出来的代码，更加易扩展、易复用、易维护。
- 从编程语言跟机器打交道的方式的演进规律中，我们可以总结出：面向对象编程语言比起面向过程编程语言，更加人性化、更加高级、更加智能。

大家的留言都好精彩啊！！多看看！

> 为什么说面向对象编程语言比面向过程编程语言更高级？

[07 | 理论四：哪些代码设计看似是面向对象，实际是面向过程的？](https://time.geekbang.org/column/article/164907)

> 有哪些看似是面向对象实际是面向过程风格的代码？

- 滥用 getter、setter 方法
- Constants 类、Utils 类的设计问题
- 基于贫血模型的开发模式

> 在面向对象编程中，为什么容易写出面向过程风格的代码？

> 面向过程编程和面向过程编程语言就真的无用武之地了吗？

[08 | 理论五：接口vs抽象类的区别？如何用普通的类模拟抽象类和接口？](https://time.geekbang.org/column/article/165103)



[09 | 理论六：为什么基于接口而非实现编程？有必要为每个类都定义接口吗？](https://time.geekbang.org/column/article/165114)

你需要掌握的重点内容。

1. “基于接口而非实现编程”，这条原则的另一个表述方式，是“基于抽象而非实现编程”。后者的表述方式其实更能体现这条原则的设计初衷。我们在做软件开发的时候，一定要有抽象意识、封装意识、接口意识。越抽象、越顶层、越脱离具体某一实现的设计，越能提高代码的灵活性、扩展性、可维护性。

2. 我们在定义接口的时候，一方面，命名要足够通用，不能包含跟具体实现相关的字眼；另一方面，与特定实现有关的方法不要定义在接口中。
3. “基于接口而非实现编程”这条原则，不仅仅可以指导非常细节的编程开发，还能指导更加上层的架构设计、系统设计等。比如，服务端与客户端之间的“接口”设计、类库的“接口”设计。

[10 | 理论七：为何说要多用组合少用继承？如何决定该用组合还是继承？](https://time.geekbang.org/column/article/169593)

如果类之间的继承结构稳定（不会轻易改变），继承层次比较浅（比如，最多有两层继承关系），继承关系不复杂，我们就可以大胆地使用继承。反之，系统越不稳定，继承层次很深，继承关系复杂，我们就尽量使用组合来替代继承。

除此之外，还有一些设计模式会固定使用继承或者组合。比如，装饰者模式（decorator pattern）、策略模式（strategy pattern）、组合模式（composite pattern）等都使用了组合关系，而模板模式（template pattern）使用了继承关系。

1. **为什么不推荐使用继承？**

   继承是面向对象的四大特性之一，用来表示类之间的 is-a 关系，可以解决代码复用的问题。虽然继承有诸多作用，但继承层次过深、过复杂，也会影响到代码的可维护性。在这种情况下，我们应该尽量少用，甚至不用继承。

   **组合相比继承有哪些优势？**

   继承主要有三个作用：表示 is-a 关系，支持多态特性，代码复用。而这三个作用都可以通过组合、接口、委托三个技术手段来达成。除此之外，利用组合还能解决层次过深、过复杂的继承关系影响代码可维护性的问题。

   **如何判断该用组合还是继承？**

   尽管我们鼓励多用组合少用继承，但组合也并不是完美的，继承也并非一无是处。在实际的项目开发中，我们还是要根据具体的情况，来选择该用继承还是组合。如果类之间的继承结构稳定，层次比较浅，关系不复杂，我们就可以大胆地使用继承。反之，我们就尽量使用组合来替代继承。除此之外，还有一些设计模式、特殊的应用场景，会固定使用继承或者组合。

[11 | 实战一（上）：业务开发常用的基于贫血模型的MVC架构违背OOP吗？](https://time.geekbang.org/column/article/169600)

我们平时做 Web 项目的业务开发，大部分都是基于贫血模型的 MVC 三层架构，在专栏中我把它称为传统的开发模式。之所以称之为“传统”，是相对于新兴的基于充血模型的 DDD 开发模式来说的。基于贫血模型的传统开发模式，是典型的面向过程的编程风格。相反，基于充血模型的 DDD 开发模式，是典型的面向对象的编程风格。

不过，DDD 也并非银弹。对于业务不复杂的系统开发来说，基于贫血模型的传统开发模式简单够用，基于充血模型的 DDD 开发模式有点大材小用，无法发挥作用。相反，对于业务复杂的系统开发来说，基于充血模型的 DDD 开发模式，因为前期需要在设计上投入更多时间和精力，来提高代码的复用性和可维护性，所以相比基于贫血模型的开发模式，更加有优势。

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

