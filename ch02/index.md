# 一个简单的地图
介绍了那么多，本节开始，我们将直接进入主题，体验一下使用OpenLayers 3做地图的难度，及地图的外观和功能：

<head>
	<link href="../src/ol3.13.1/ol.css" rel="stylesheet" type="text/css" />
	<script type="text/javascript" src="../src/ol3.13.1/ol.js" charset="utf-8"></script>
</head>

<body>
	<div id="map" style="width: 100%"></div>
	<script>
	  new ol.Map({
			layers: [
				new ol.layer.Tile({source: new ol.source.OSM()})
			],
			view: new ol.View({
				center: [0, 0],
				zoom: 2
			}),
			target: 'map'
	  });
	</script>
</body>

要显示上面这个地图，仅需要新建一个html文档，在其中编写如下代码即可：

```html
<!Doctype html>
<html xmlns=http://www.w3.org/1999/xhtml>
<head>                  
	<meta http-equiv=Content-Type content="text/html;charset=utf-8">
	<meta http-equiv=X-UA-Compatible content="IE=edge,chrome=1">
	<meta content=always name=referrer>
	<title>OpenLayers 3地图示例</title>
	<link href="../ol3.13.1/ol.css" rel="stylesheet" type="text/css" />
	<script type="text/javascript" src="../src/ol3.13.1/ol.js" charset="utf-8"></script>
</head>

<body>
	<div id="map" style="width: 100%, height: 400px"></div>
	<script>
	  // 创建地图
	  new ol.Map({
			// 设置地图图层
			layers: [
			  // 创建一个使用Open Street Map地图源的瓦片图层
			  new ol.layer.Tile({source: new ol.source.OSM()})
			],
			// 设置显示地图的视图
			view: new ol.View({
			  center: [0, 0],	// 定义地图显示中心于经度0度，纬度0度处
			  zoom: 2			// 并且定义地图显示层级为2
			}),
			// 让id为map的div作为地图的容器
			target: 'map'	
		});
	</script>
</body>
	
</html>
```

要想使用OpenLayers 3开发地图，必然需要引入了OpenLayers 3的js库文件ol3.js及样式文件ol3.css，参见代码中html头部。它们可以在[github](https://github.com/openlayers/ol3/releases)上下载到。

紧接着就是利用OpenLayers 3的API创建地图，对应于`<script>...</script>`代码块，如代码所见，7行代码就搞定了，是不是非常的简单？！至于代码的含义，可以暂时参照代码中的注释来理解。暂时看不懂也没有关系，接下来我们将详细的介绍它们。
