
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
    
很多杰出的人在 JavaScript 出现前，也就是数十年前已经意识到类继承的风险，你可以找到相关的论文，比如“Object Oriented Programming Considered Harmful”，“Class Considered Harmful” 以及 “New Considered Harmful”。诸如此类的警告发表在 Usenet 上、学术论文中以及受人推崇的出版商上，比如 Doctor Dobb’s Journal —— 一本介绍了软件开发在2014年前40年左右智慧的杂志。

