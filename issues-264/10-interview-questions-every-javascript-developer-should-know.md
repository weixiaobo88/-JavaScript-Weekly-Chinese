
# 每个 JavaScript 开发人员都应该知道的 10 个面试题 
##—— 精通 JavaScript 的关键


[查看原文](https://medium.com/javascript-scene/10-interview-questions-every-javascript-developer-should-know-6fa6bdf5ad95?utm_source=javascriptweekly&utm_medium=email)

在大多数公司，为了考核候选者的技能，一般都会让开发人员进行技术面试。如何面试呢？

## 你可能不同意，不过没关系

我建议你根据一个开发人员是否相信类继承来雇用他，为什么？因为喜欢类继承的人通常都是一意孤行。正如 Bruce Lee 的名言一样：

>
那些不知道到自己在黑暗中行走的人永远不会寻求光明。

我不会雇用他们，你也不应该。

[我看到过类的使用对项目、公司以及生活带来的破坏](https://medium.com/javascript-scene/inside-the-dev-team-death-spiral-6a7ea255467b)，很多杰出的人都不同意我的观点，然而在否定我的观点前，思考以下几点：

我在 SaaS 初期开了一家 app 咨询公司，当然在 SaaS 这个词被滥用之前。我已经在上百个项目上工作过，不管是创业项目还是500强公司。我有 C++、Java（还有 AutoLisp、Delphi 等）的背景，我在几十家 Java 和 C++ 应用（都是面向类的面向对象编程语言）上做过咨询。我曾经也是一个类继承的支持者，甚至为它写过多语言的快速软件开发工具（Rapid Application Development，RAD）。

我多次看到类范式将无经验开发人员引向错误之路，而且我还看到过非常极端的影响。我看到有些产品为了停止损失不得不停止使用，开发人员被解雇，公司被打败，类以及类继承的不合理使用造成的混乱代码库。
    
在 JS 中类并不是面向对象原型的无害语法糖，类就是一个病毒，它会感染到任何和它接触的东西。这种现象伴随着 ES6 的正式使用，而与此同时，React 出现了。很多人开始在 React 组件中使用类（你不应该这样，最新的 React 0.14 支持纯函数的组件，或者你可以使用 [react-stamp](https://github.com/stampit-org/react-stamp)）。
    
很多人不知道你可以创建一个不是类的 React 组件，而这在 React 组件和其他 React 生态系统（components、mixins、component wrappers）中可组合的元素之间造成混淆和不一致。
    
在 Backbone 统治（Backbone 用它自己的类的形式）的年代，我看到一个扩展性不凑的代码库变的脆弱和混乱。我看到很多代码为了调用类的API而必须使用'new'来抽象，或者使用工厂，强迫使用容器的依赖注入，使得每个依赖都与容器 API 强绑定，这些都使代码变的复杂。Angular 有四种不同的方式来创建 service，并使用一个依赖注入容器对其抽象。
    
很多杰出的人在 JavaScript 出现前，也就是数十年前已经意识到类继承的风险，你可以找到相关的论文，比如“Object Oriented Programming Considered Harmful”，“Class Considered Harmful” 以及 “New Considered Harmful”。诸如此类的警告发表在 Usenet 上、学术论文中以及受人推崇的出版商上，比如 Doctor Dobb’s Journal —— 一本介绍了软件开发在2014年前40年左右智慧的杂志。很巧的是，还有一篇题为“Considered Harmful Considered Harmful”的文章，不过我离题了。

Erlang 的创造者 Joe Armstrong 总结了一个著名的问题，这个问题在书《[Coders at Work](http://amzn.to/1WcDcJt)》中被称为“大猩猩与香蕉问题”。

> 面向对象语言的问题在于它们会抓住周围所有的隐式的环境信息。你只想要一个香蕉，但是你得到的是拿着香蕉的大猩猩以及整个丛林。

面向对象设计的经典书籍“[Design Patterns: Elements of Reusable Object-Oriented Software](http://amzn.to/1Qs3VOv)”中提到“组合由于类继承”。

> 
  有些读者想要更多关于类的讨论，下面的资料能知道为什么我不喜欢JavaScript中的类。
  
  * [The Two Pillars of JavaScript: How to Escape the 7th Circle of Hell](https://medium.com/javascript-scene/the-two-pillars-of-javascript-ee6f3281e7f3)
  * [A Simple Challenge to Classical Inheritance Fans](https://medium.com/javascript-scene/a-simple-challenge-to-classical-inheritance-fans-e78c2cf5eead)
  * [Common Misconceptions About Inheritance in JavaScript](https://medium.com/javascript-scene/common-misconceptions-about-inheritance-in-javascript-d5d9bab29b0a)
  * [How to Fix the ES6 `class` Keyword](https://medium.com/javascript-scene/how-to-fix-the-es6-class-keyword-2d42bb3f4caf)
  * [Introducing the Stamp Specification](https://medium.com/javascript-scene/introducing-the-stamp-specification-77f8911c2fee)

如果你是一个类继承的忠实粉丝，你可能不同意这些文章中所论述的内容，不过其中也有有价值的部分，你可以去其糟粕，取其精华，我不会为此而生气。

## 始于某些人的言论

在[How to Build a High Velocity Development Team](https://medium.com/javascript-scene/how-to-build-a-high-velocity-development-team-4b2360d34021) 中，我提出一个观点：没有什么比一个非同一般的团队能预测业务的结果。如果你想打破这个断言，你应该现在开始做。

正如 Marcus Lemonis 说的，关注在 3 个 P 上：“People, Process, Product”。

你早期应该雇用经验丰富的候选者，这些人可以招聘或者指导其他开发人员，帮助后期招进来的中级或初级开发人员的成长。

[Why Hiring is So Hard in Tech](https://medium.com/javascript-scene/why-hiring-is-so-hard-in-tech-c462c3230017)文章可以对候选者的评价给出建议。

> 考察一个候选者最好的方式就是结对编程。

和候选者结对编程，让候选者来驱动，多看他怎么写的，多听他怎么说的。一个好的项目可能会从Twitter API上pull很多tweets然后将其显示在时间轴上。

也就是说，没有一个单一的练习会告诉你需要知道的所有事情。面试可能是一个非常有用的工具，但是不要把时间花费在问一些语法问题或者语言的一些怪癖上。你需要关注更重要的事情上。你可以问一些架构或范式的东西，这些对于整个项目来讲很重要。

语法和特性很容易通过Google找到，但是对于软件精髓或通用的范式这些需要经验的东西来说并不是很容易能Google到。

JavaScript很特殊，它在每个大型的应用中都起到了重要的作用，是什么让JavaScript这么不同于其他语言呢？

下面这些问题可以帮助你来思考这个问题：

1. 你能说出对JavaScript开发人员来说很重要的两种编程范式吗？

JavaScript是一个多范式的语言，支持指令式/过程式编程，也支持面向对象编程和函数式编程。JavaScript支持原型继承的面向对象编程。

很高兴能听到以下内容: 

- 原型继承（或原型、OLOO）
- 函数式编程（或闭包、一等函数、lambdas）

危险信号：

- 不知道什么范式，没有提到原型面向对象或函数式编程。

更多资料：

- [The Two Pillars of JavaScript Part 1](https://medium.com/javascript-scene/the-two-pillars-of-javascript-ee6f3281e7f3)——原型面向对象
- [The Two Pillars of JavaScript Part 2](https://medium.com/javascript-scene/the-two-pillars-of-javascript-pt-2-functional-programming-a63aa53a41a4)——函数式编程


2. 什么是函数式编程

函数式编程的程序由数学函数组成，并且不会共享状态和不会有可变的数据。Lisp(1958年声明)是第一个支持函数式编程的语言，这其中受到了lambda微积分的很大启发。Lisp 和很多 Lisp 家族语言在今天仍然很常用。

函数式编程是JavaScript的精髓概念（是JavaScript的两个支柱之一），在 ES5 中已经加入了很多常用的函数式功能。

很高兴能听到以下内容: 

- 纯函数
- 避免副作用
- 简单的函数组合
- 函数式语言的例子：Lisp、ML、Haskell、Erlang、Clojure、Elm、F Sharp、OCaml 等
- 提到支持函数式编程的特性：一等函数、高阶函数、函数作为参数或值

危险信号：

- 没有提到纯函数或避免副作用
- 不能说出哪些语言是函数式编程语言
- 不能说出JavaScript支持函数式编程的特性

更多资料：

- [The Two Pillars of JavaScript Part 2](https://medium.com/javascript-scene?source=logo-lo_d50cb5f9e62f-c0aeac5284ad)
- [The Dao of Immutability](https://medium.com/javascript-scene/the-dao-of-immutability-9f91a70c88cd)
- [Professor Frisby’s Mostly Adequate Guide to Functional Programming](https://github.com/MostlyAdequate/mostly-adequate-guide)
- [The Haskell School of Music](http://haskell.cs.yale.edu/wp-content/uploads/2015/03/HSoM.pdf)

3. 类式继承和原型继承有什么区别？

类式继承：实例继承自类（像一个计划——类的描述），创建子类关系：分层体系。实例是由构造函数通过'new'关键字来初始化的。类式继承在 ES6中可能使用 'class' 关键字。

原型继承：实例继承自其他对象。实例通过工厂函数或'Object.create()' 来初始化，实例可能通过多个不同对象组成，允许简单的选择性继承。

> 在JavaScript中，原型继承比类继承更简单更灵活。

很高兴能听到以下内容: 

- 类：创建紧耦合，紧层次/紧分类
- 原型：提到可拼接的继承，原型代理，函数式继承，对象组合

危险信号：

- 相比类继承，对于原型继承和组合没有偏好

更多资料：

- [The Two Pillars of JavaScript Part 1 — Prototypal OO](https://medium.com/javascript-scene/the-two-pillars-of-javascript-ee6f3281e7f3)
- [Common Misconceptions About Inheritance in JavaScript](https://medium.com/javascript-scene/common-misconceptions-about-inheritance-in-javascript-d5d9bab29b0a)

4. 函数式编程和面向对象编程的优缺点分别是什么？

面向对象编程优点：很容易理解对象以及方法调用的基本概念。面向对象编程倾向于使用命令式的风格而非声明式的风格，这读起来就像电脑执行指令一样。

面向对象编程确定：面向对象编程依赖于共享的状态。对象和行为在同一个实体上绑定在一起，对于运行顺序不确定的多个函数来说，可能会被随机访问，这可能会导致预想不到的结果，比如竞争条件。

函数式编程的优点：




