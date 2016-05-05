# OpenLayers 3 介绍

OpenLayers 3简称ol3，它是一个开源的Web GIS引擎，使用了JavaScript、最新的HTML5技术及CSS技术，支持dom，canvas和webgl三种渲染方式。除了支持网页端，还支持移动端（目前移动端还不成熟，有待进一步完善）。在地图数据源方面，支持各种类型的瓦片地图，既支持在线的，也支持离线的。比如OSM, Bing, MapBox, Stamen, MapQuest等等；还支持各种矢量地图，比如GeoJSON，TopoJSON，KML，GML等等。随着OpenLayers 3的进一步发展，将支持更多的地图类型。

## 不兼容OpenLayers 2
在OpenLayers 3之前，还有OpenLayers 2，虽然从名字上看是一个升级版本，但OpenLayers 3完全是重新设计，采用全新的架构，使用方式及API都不一样，只是在功能上完全实现OpenLayers 2已有的功能。为此，使用OpenLayers 3不必先学习OpenLayers 2。但使用过OpenLayers 2，并不等于直接就会用OpenLayers 3，仍然需要从零开始学习它。

## 浏览器支持
由于OpenLayers 3使用了HTML5技术，所以对各种浏览器的版本有所要求。IE浏览器最低也需要IE9才行，以下的IE浏览器可以考虑使用OpenLayers 2。其他浏览器的最低版本要求为Firefox 3.5，Chrome 3.0，Safari 3.0，Opera 10.5。如果要使用`webgl`渲染方式，则又需要参考各大浏览器的支持程度进行选择。

## 代码规范
* OpenLayers 3采用面向对象的编程范式，类在API中随处可见，比如`ol.Map`，`ol.View`等等。如果你有面向对象的思维，将较为容易的理解API及使用。
* OpenLayers 3采用包管理的方式管理代码，比如`layer`的包名为`ol.layer`，命名方式类似于JAVA的包名。这源于OpenLayers 3采用了Google的[Closure库](https://developers.google.com/closure/library/)。
* OpenLayers 3采用[驼峰式(Camel-Case)命名](http://baike.baidu.com/link?url=-N6ZFy7Q1645xbSZxDwv6CEluYjnBX2mn8hA3cabF0VNZiHnrPyRonRAqEr4GYXBte0GH0BzaIkZOFQFatV5tK)，变量名采用小驼峰命名，类名使用大驼峰命名。

## 资源
OpenLayers 3的官网是[http://openlayers.org/](http://openlayers.org/)，若记不住，请保存到收藏夹。在官网首页上，即可看到相关的介绍，文档，API，以及Examples链接。这些资料都跟随最新的版本实时更新，如果发现本教程有些内容和官方不一致，请以官网资料为准，可能由于版本更新导致的。

喜欢研究源码的开发者，请关注github [https://github.com/openlayers/ol3](https://github.com/openlayers/ol3)。有能力者，可以考虑为OpenLayers 3提交PR和issue，不过在此之前请先阅读[贡献文档](https://github.com/openlayers/ol3/blob/master/CONTRIBUTING.md)