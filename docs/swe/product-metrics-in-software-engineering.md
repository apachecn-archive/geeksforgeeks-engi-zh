# 软件工程中的产品度量

> 原文:[https://www . geesforgeks . org/product-metrics-in-software-engineering/](https://www.geeksforgeeks.org/product-metrics-in-software-engineering/)

产品度量是软件产品在其开发的任何阶段的度量，从需求到已建立的系统。产品指标仅与软件功能相关。

**产品指标分为两类:**

1.  由执行中的程序的测量结果收集的动态度量。
2.  从系统表示(如设计、程序或文档)中进行的测量所收集的静态度量。

动态度量有助于评估程序的效率和可靠性，而静态度量有助于理解、理解和维护软件系统的复杂性。

**动态度量**通常与软件质量属性有非常密切的关系。测量特定任务所需的执行时间和估计启动系统所需的时间相对容易。这些与系统故障的效率直接相关，并且故障的类型可以被记录，并且与软件的可靠性直接相关。

另一方面，静态矩阵与质量属性有间接关系。已经提出了大量这样的矩阵，试图推导和验证复杂性、可理解性和可维护性之间的关系。在这些表中给出的用于评估质量属性的几个静态指标，程序或组件长度和控制复杂性，似乎是可理解性、系统复杂性和可维护性的最可靠的预测因素。

**软件产品指标:**

<center>

| 没有。 | 软件度量 | 描述 |
| --- | --- | --- |
| (1) | 扇入/扇出 | 扇入是对调用其他函数(比如 X)的函数数量的度量。扇出是由函数 X 调用的函数的数量。扇入的高值意味着 X 与设计的其余部分紧密耦合，对 X 的更改将产生广泛的连锁效应。扇出值高意味着协调被调用组件所需的控制逻辑的整体复杂性。 |
| (2) | 代码长度 | 这是程序大小的度量。通常，程序组件的代码越大，该组件就越复杂，越容易出错。 |
| (3) | 圈复杂度 | 这是对程序控制复杂性的度量。这种控制复杂性可能与程序的可理解性有关。 | (4) | 标识符长度 | 这是对程序中不同标识符平均长度的度量。标识符越长，程序越容易理解。 |
| (5) | 条件嵌套的深度 | 这是对 aa 程序中 if 语句嵌套深度的度量。深度嵌套的 if 语句很难理解，并且可能容易出错。 |
| (6) | 雾指数 | 这是对文档中单词和句子平均长度的度量。雾索引的值越高，文档可能越难理解。 |

</center>