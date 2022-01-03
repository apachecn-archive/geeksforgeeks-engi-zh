# 建筑风格、建筑格局和设计格局的区别

> 原文:[https://www . geeksforgeeks . org/建筑风格差异-建筑模式和设计模式/](https://www.geeksforgeeks.org/difference-between-architectural-style-architectural-patterns-and-design-patterns/)

许多软件专业人士认为架构风格和模式是相同的。可悲的是，一些软件开发人员不理解架构模式和设计模式之间的区别。在本文中，我们将总结它们之间的差异。

按照 MSDN 的说法，建筑风格和格局是一回事。但是怎么可能呢？风格这个词的意思是:**“做某事的方式”**，而图案的意思是:**“重复的装饰设计”**。然而，这些定义表明了两件不同的事情。在软件工程中，术语必须更加清晰，并描述一些具体的东西。那么，这些术语之间有什么区别，我们如何区分它们？

### 建筑风格

架构风格展示了我们如何组织我们的代码，或者从 10000 英尺的直升机视图来看，系统将是什么样子，以显示我们系统设计的最高抽象级别。此外，当构建我们系统的架构风格时，我们关注的是层和模块以及它们如何相互通信。

有不同类型的建筑风格，此外，我们可以将它们混合起来，产生一种混合风格，由两种甚至更多的建筑风格组成。以下是每个类别的建筑风格和示例列表:

*   **结构建筑风格:**如分层、管道和过滤器以及基于构件的风格。
*   **消息传递风格:**如隐式调用、异步消息传递和发布-订阅风格。
*   **分布式系统:**例如面向服务、对等风格、对象请求代理和云计算风格。
*   **共享内存风格:**如基于角色、黑板、以数据库为中心的风格。
*   **自适应系统风格:**如微内核风格、反射、特定领域语言风格。

### 建筑模式

架构模式展示了如何使用解决方案来解决重复出现的问题。换句话说，它反映了代码或组件如何相互作用。此外，架构模式描述了我们系统的架构风格，并为我们架构风格中的问题提供了解决方案。就我个人而言，我更喜欢将架构模式定义为实现我们的架构风格的一种方式。例如:如何在我们的架构风格中分离数据模块的 UI？如何将第三方组件与我们的系统集成？在我们的客户机-服务器架构中，我们将有多少个轮胎？架构模式的例子有微服务、消息总线、服务请求者/消费者、MVC、MVVM、微内核、n 层、域驱动设计和表示抽象控制。

### 设计模式

设计模式是软件专业人员多年来积累的最佳实践和经验，通过反复试验来解决他们在软件开发过程中面临的一般问题。“四人帮”(g of，指埃里克·伽马、理查德·赫尔姆、拉尔夫·约翰逊和约翰·弗里西德斯)在 1994 年写了一本名为《设计模式——可重用面向对象软件的要素》的书，他们在书中提出设计模式基于面向对象设计的两个主要原则:

*   开发一个接口，而不是实现。
*   重对象组合轻继承。

此外，他们提出设计模式集包含 23 种模式，并分为三个主要集:

**1。创造设计模式:**
提供一种在隐藏创造逻辑的同时创造对象的方法。因此，对象创建无需直接用“New”关键字实例化对象，从而可以灵活地决定需要为给定的用例创建哪些对象。创造性的设计模式是:

*   **抽象工厂模式:**提供创建对象的接口，而不指定类。
*   **单例模式:**仅提供调用的单个实例和对此实例的全局访问。
*   **构建器模式:**将构造与表示分离，并允许同一构造创建多个表示。
*   **原型模式:**在不影响性能和内存的情况下创建副本。因此，复制的对象是从现有对象的骨架中构建的。

**2。结构模式:**

关注类和对象的组成。结构设计模式是:

*   **适配器模式:**它充当两个不兼容接口之间的桥梁，并编译它们的功能。
*   **桥接模式:**提供了一种将抽象与其实现解耦的方法。
*   **过滤模式:**也称为标准模式，它提供了一种使用不同标准过滤一组对象的方法，并通过逻辑操作以解耦的方式链接它们。
*   **复合模式:**提供了一种将一组对象以类似于单个对象的方式进行处理的方法。它用树形结构来组成对象，以表示部分和整个层次结构
*   **装饰器模式:**允许在不改变现有对象结构的情况下向其添加新功能。
*   **外观模式:**为一组接口提供统一的接口，它隐藏了系统的复杂性，为客户端提供了一个可以访问系统的接口。
*   **Flyweight 模式:**减少创建的对象数量，减少内存占用并提高性能。它通过存储已经存在的相似种类的对象来帮助重用它们，并且当没有找到匹配的对象时创建一个新的对象。
*   **代理模式:**为另一个对象提供一个占位符来控制对它的访问。该对象有一个原始对象，用于将其功能与外部世界接口。

**3。行为模式:**

行为模式与对象之间的通信有关。以下是行为模式列表:

*   **责任模式:**为一个请求创建一个接收者对象链。这种模式根据请求的类型来分离请求的发送方和接收方。
*   **命令模式:**这是一种数据驱动的模式，其中一个请求作为命令被包装在一个对象下，并被传递给调用方对象。
*   **解释器模式:**提供了一种评估语言语法或表达的方法。它包括实现一个表达式接口来解释一个特定的上下文。该模式用于 SQL 解析、符号处理引擎等。
*   **迭代器模式:**提供了一种以顺序方式访问集合对象元素的方法，而无需知道其底层表示。
*   **中介模式:**用于降低多个对象或类之间的通信复杂度。它提供了一个中介类，通常处理不同类之间的所有通信，并支持通过松散耦合轻松维护代码。
*   **memorant 模式:**用于将对象的状态恢复到之前的状态。
*   **观察者模式:**当对象之间存在一对多关系时使用，例如如果一个对象被修改，其从属对象将被自动通知。
*   **状态模式:**用于根据类的状态改变类的行为。
*   **空对象模式:**有一个默认对象，有助于避免空引用。
*   **策略模式:**提供了一种在运行时改变类行为或其算法的方法。
*   **模板模式:**抽象类公开了执行其方法的定义方式/模板。它的子类可以根据需要覆盖方法实现，但是调用的方式与抽象类定义的方式相同。
*   **访客模式:**用于改变一个元素类的执行算法。

还有两个设计模式子集可以添加到 3 类设计模式中:

*   **J2EE 模式:**模式特别关注表示层。这些模式由 Sun Java 中心识别。
*   **并发模式:**如:阻塞、连接、锁和线程池模式

**底线:**

建筑风格是系统的 10000 直升机视图。它展示了最高抽象层次的系统设计。它还显示了应用程序的高级模块以及这些模块是如何交互的。另一方面，架构模式在横向和纵向上都对系统实现有巨大的影响。最后，设计模式用于解决软件实现过程中的本地化问题。此外，与架构模式相比，它对代码的影响更小，因为设计模式更关心代码实现的特定部分，例如初始化对象和对象之间的通信。