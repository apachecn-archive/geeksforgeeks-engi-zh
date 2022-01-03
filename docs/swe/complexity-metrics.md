# 复杂性度量

> 原文:[https://www.geeksforgeeks.org/complexity-metrics/](https://www.geeksforgeeks.org/complexity-metrics/)

如果只以单位时间内的代码行数来衡量生产率，那么生产率可能会因所开发系统的复杂性而有很大差异。与简单的应用程序相比，程序员会为高度复杂的系统程序生成较少的代码。同样，复杂性对维护程序的成本有很大影响。为了量化复杂程度，超越程序容易构建或理解的模糊概念，需要一些度量来衡量程序的复杂性。

复杂性度量是一种 [**圈复杂性**](https://www.geeksforgeeks.org/cyclomatic-complexity/) ，其中模块的复杂性是模块的[流程图中独立循环的数量。已经提出了许多度量标准来量化程序的复杂性，并且已经进行了研究来将复杂性与维护工作联系起来。在本文中，我们将讨论一些复杂性度量。其中大部分都是在程序的背景下提出的，但是它们也可以应用于或适用于详细的设计。](https://www.geeksforgeeks.org/software-engineering-control-flow-graph-cfg/)

**<u>大小度量</u> :** 复杂度度量试图捕捉理解一个模块的难度。换句话说，它试图量化一个程序的认知方面。众所周知，一般来说，模块越大，越难理解。因此，模块的大小可以作为模块复杂性的简单度量。可以看出，平均来说，随着模块规模的增加，其中的决策数量很可能会增加。这意味着平均来说，随着尺寸的增加，**圈复杂度**也会增加。尽管两个相同大小的程序显然有可能具有本质上不同的复杂性，但总的来说，大小与一些复杂性度量有很大的关系。

**<u>霍尔斯特德的测度</u> :** 霍尔斯特德也基于他的软件科学提出了许多其他的测度。其中一些可以被认为是复杂性度量。已经定义了许多变量来解释这一点。分别是 **n1** (唯一操作数个数) **n2** (唯一操作数个数) **N1** (操作数总频率) **N2** (操作数总频率)。由于任何程序都必须至少有两个操作符:一个用于函数调用，一个用于语句结束——由于程序中的操作符数量较多，因此 **n1/2** 的比值可以被认为是相对的难度水平。比率 **N2/n2** 代表操作数的平均使用次数。在变量变化更频繁的程序中，这个比例会更大。由于此类程序较难理解，阅读或书写的便利性定义为:

> ![D = \frac{n_{1}*N_{2}}{2*n_{2}}](img/0f3e267daa7853e0cf30b439b4628011.png "Rendered by QuickLaTeX.com")

**<u>霍尔斯特德的复杂性度量</u>** 关注模块的内部复杂性，正如**麦凯布的复杂性度量**一样。因此，模块与其环境连接的复杂性并不重要。在霍尔斯特德的度量中，模块与其环境的联系反映在操作数和运算符方面。对另一个模块的调用被视为运算符，所有参数都被视为该运算符的操作数。

**<u>活变量</u> :** 在计算机程序中，典型的赋值语句只使用和修改几个变量。然而，一般来说，语句具有更大的上下文，即为了构造或理解语句，程序员必须跟踪大量变量，而不是那些直接在语句中使用的变量。一句话，这样的数据项叫做**活变量**。直觉上，语句的活变量越多，就越难理解一个程序。因此，**活动变量**的概念可以用作程序复杂性的度量。

首先，让我们更精确地定义**活变量**。在模块中，从变量的第一个引用到最后一个引用，包括引用该变量的第一个语句和最后一个语句之间的所有语句，都被认为是活动的。使用这个定义，通过分析模块的代码，可以很容易地计算出每个语句的活变量集。确定活动变量的过程可以很容易地自动化。

对于一条语句，活变量的数量代表语句的难度。这可以通过定义活动变量的平均数量扩展到整个模块。活动变量的平均数量是活动变量的计数(对于所有可执行语句)除以可执行语句的数量的总和。这是模块的复杂性度量。

活动变量是从数据使用的角度定义的。模块的逻辑没有明确包括在内。该逻辑仅用于确定变量的第一个和最后一个引用语句。因此，这种复杂性的概念与**圈复杂性**有很大不同，圈复杂性完全基于逻辑，将数据视为次要的。

另一个面向数据使用的概念是 **span** ，一个变量两次连续使用之间的语句数。如果一个变量在一个模块中的不同位置被引用到 **N** 处，那么该变量有**(N–1)个跨度**。平均跨度大小是变量的两个连续引用之间的可执行语句的平均数量。大的**跨度**意味着程序的读者必须在更长的时间内记住变量的定义(或更多的语句)。换句话说，**跨度**可以被认为是一个复杂性度量；**跨度**越大，模块越复杂。

**<u>结计数</u> :** 已经提出了一种基于程序的控制转移的位置来量化复杂性的方法。它主要是为 **FORTRAN** 程序设计的，其中通过使用[转到](https://www.geeksforgeeks.org/goto-statement-in-c-cpp/)语句来显示明确的控制权转移。一个程序员，为了理解一个给定的程序，通常从控制转移的点画箭头到它的目的地，帮助创建一个程序和其中的控制转移的精神图像。根据这个标准，这些箭头越是交织在一起，程序就越复杂。这个概念被捕获在**结**的概念中。

一个**结**本质上是两个这样的控制转移箭头的交集。如果程序中的每个语句都写在单独的一行上，这个概念可以形式化如下。从线路 **a** 到线路 **b** 的跳跃由**对(a，b)** 表示。如果**最小(a，b) <最小(p，q) <最大(a，b)** 和**最大(p，q) >最大(a，b)** 或**最小(a，b) <最大(p，QA)<两次跳跃 **(a，b)** 和 **(p，q)** 产生一个**结****

使用结构化构造确定程序的**结**计数时可能会出现问题。一种方法是将这样的程序转换成明确显示控制转移的程序，然后计算**结**计数。基本方案可以推广到流图，尽管流图只能得到界限。

**<u>【拓扑复杂性】</u> :**
一种对结构嵌套敏感的复杂性度量被提出。像**圈复杂度**一样，它是基于一个模块或者程序的流程图。程序的复杂性被认为是它的最大交集数最小。

为了计算最大交集，流图被转换成强连通图(通过画一个从终端节点到初始节点的箭头)。强连通图将图分成有限个区域。区域的数量为(边–节点+ 2)。如果我们画一条线正好进入每个区域一次，那么这条线与图中的弧相交的次数就是最大相交最小值，它被认为是程序的复杂性。