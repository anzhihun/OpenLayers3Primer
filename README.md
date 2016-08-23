# OpenLayers 3 Primer

## 介绍
这是一个关于OpenLayers 3使用的入门教程。帮助初学者逐步认识OpenLayers 3，理解地图组成，以及各个组成部分的作用。在此基础上，逐个突破，结合大量的实例，指导大家应用OpenLayers 3开发出符合业务的地图。在这个过程中，辅以对应的理论知识，学习了解OpenLayers 3背后的原理，尽量做到知其然且知其所以然，为更高级的OpenLayers 3开发打下坚实的基础。本教程将坚持实用为主，对应用中遇到的重点、难点加以详细讲解，提出实用方案。

为了满足广大初学者的需要，教程将坚持一个原则：即以**浅显易懂**为基础，以**有效实用**为最终目标的原则。

## 为什么要写这样一个教程
故事是从我学习OpenLayers 3开始的。那时版本才3.0.0，当时学习OpenLayers 3很快就入手了，没有遇到任何障碍。 但后来发现有些初学者并不是这样的，都不知道怎么入手，遇到很多问题，我在回答了很多类似问题后，开始寻找入门难的原因。 总结下来有两个主要原因：
* 第一，虽然官网有关于每个类和方法的API文档，也有相关的例子，但就是没有一个系统的教程把他们串起来，对着例子虽然能做出一些类似的业务，但并不能灵活应用，自然会遇到很多问题。 同时国内目前并没有一本关于OpenLayers 3学习的书籍或教程，这是比较让人遗憾的事。庆幸地是国外的同仁已经写了两本英文书籍，一本是[OpenLayers 3: Beginner's Guide](https://www.packtpub.com/web-development/openlayers-3-beginner%E2%80%99s-guide)，需要付费；另一本是[The book of OpenLayers 3](https://leanpub.com/thebookofopenlayers3)，需要付费，但同时也支持开放。但对于国内开发者而言，还是中文更加可读。 (国外最近又出了两本需要付费的书，一本是[Mastering Openlayers 3](https://www.packtpub.com/web-development/mastering-openlayers-3)，这本书内容涵盖也比较全面，对英文没有障碍的初学者，可以学习。 另一本是[OpenLayers 3.x Cookbook - Second Edition](https://www.packtpub.com/web-development/openlayers-3x-cookbook-second-edition))
* 第二，使用OpenLayers 3的初学者并不都是GIS专业出身，有很大一部分是前端开发者，或者其他领域的开发者，GIS相关的理论知识欠缺。同时，还有一些开发者连JavaScript语言也不熟练，API文档都不知道如何阅读。 但由于任务或者项目压身，不得不使用Openlayers开发，自然会遇到很多困难。

为了解决这个问题，我写过一篇[OpenLayers 3 入门指南](http://www.jianshu.com/p/6785e755fa0d)，一开始想当然地认为可以解决入门问题，直到有一天在群里来了一个初学者，他看了这篇文章后，觉得并没有什么卵用。这时我才意识到问题的严重性，问题没解决，反而多了一篇垃圾。因为入门者需要的是更为具体的东西。 在征集了大多数人的意见后，我决定写这本教程（在此一并感谢QQ群里那些提出意见，给予帮助的帅哥美女们）。目前国内存在很多OpenLayers 3的爱好者和使用者，我所在的QQ群就有将近千人，同时还存在很多其他关于OpenLayers的群，后续还会有更多的开发者使用它。

本教程作为一次尝试，我愿意做第一本国内的OpenLayers 3教程，希望能在开放的情况下，真正帮助到国内OpenLayers 3的初学者入门，虽然这并不容易，但我愿意挑战自己，并加入到开源的潮流中去，以此向OpenLayers 3这个优秀的开源引擎致敬，向它的开发团队和所有贡献者致敬！

## 目标读者
本教程的主要目标读者是刚开始接触OpenLayers 3的应用开发者，但对它有一定了解的开发者也可以通过这个教程的后续部分来提升自己的理解和认识。同时希望对它有深入了解的开发者review本教程，提交issue或者PR。

## 环境
* OpenLayers 3的版本: 3.13.1
* 浏览器: chrome 47.0.2526.111(64bit)

## 关于作者
QQ群 OpenLayers官方旗舰群[2] 里面的 **扯淡大叔**     
QQ: 11364382

### BTW
我和一帮天南海北的朋友们正在开发一个开源的WEB 3D GIS引擎[F3Earth](http://www.f3earth.com)，有兴趣的朋友可以了解一下，谢谢大家的支持。
