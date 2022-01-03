# 在软件中获得高可靠性

> 原文:[https://www . geeksforgeeks . org/get-软件中的高可靠性/](https://www.geeksforgeeks.org/getting-high-reliability-in-software/)

**软件可靠性**是保证软件性能一致、软件值得信赖的软件质量。这也保证了软件的准确性相当好，几乎接近完美。

**如何在软件中获得高可靠性？**
如果我们需要开发一个高可靠性的软件，那么在开发高可靠性软件的时候，有几点是需要考虑的:

**1。错误避免:**
在软件开发过程中，应尽可能避免错误出现的每一种可能性。因此，为了开发高可靠性软件，我们需要以下属性:

*   **经验丰富的开发人员:**为了获得高可靠性，为了尽可能避免错误，我们需要经验丰富的开发人员。
*   **软件工程工具:**对于高可靠性的软件，需要最好的软件工程工具。
*   **CASE 工具:**所使用的 CASE 工具应合适且适应性强。

**2。错误检测:**
不是使用最好的方法来避免错误，但仍有可能软件中存在一些错误。因此，为了得到高可靠性的软件，每个错误都应该被检测。错误检测的过程以测试的形式完成。这包括各种测试过程。要检测软件中的错误，需要遵循一些特定的步骤。这里用于错误检测的最常见测试是可靠性测试。

**3。错误清除:**
现在当软件中检测到错误时，我们需要修复它们。为了修复错误，换句话说，为了从软件中移除错误，我们需要一次又一次重复的测试过程。对于错误消除过程，一个错误被消除，测试人员检查错误是否被完全消除。因此，这种技术是可靠性测试过程的重复。

**4。容错:**
容错是指尽管系统出现故障，仍能给出预期的正确结果。尽管使用了错误避免、错误检测和删除，但开发一个百分之百无错误的软件实际上是不可能的。尽管一次又一次地执行不同的测试过程，一些错误仍然可能存在。为了制造高可靠性的软件，我们需要软件具有容错性。有几种技术可以使系统容错。这包括:

*   **N 版编程:**软件的 N 个副本制作成不同的版本。
*   **恢复块:**使用不同的算法来开发不同的块。
*   **回滚恢复:**每次访问系统时，都会对其进行测试。