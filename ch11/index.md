# 动画
在OpenLayers 3中，动画是随处可见的，比如平移地图时，地图移动会有惯性，停止移动后，还会继续沿着之前的方向移动一会。 比如下面这个地图具有回到原始点的功能，一个是有动画效果的，一个是没有动画效果的。

<head>                  
	<link href="../src/ol3.13.1/ol.css" rel="stylesheet" type="text/css" />
	<script type="text/javascript" src="../src/ol3.13.1/ol.js" charset="utf-8"></script>
</head>
<div id="map" style="width: 100%"></div>
<input type="button" value="回到原点-不带动画" onclick="backNoAnim()"></input>
<input type="button" value="回到原点-带动画" onclick="backWithAnim()"></input>
<script type="text/javascript">
	var map = new ol.Map({
		layers: [
		  new ol.layer.Tile({
		    source: new ol.source.OSM()
		  })
		],
		target: 'map',
		view: new ol.View({
		  center: ol.proj.transform(
		      [104, 30], 'EPSG:4326', 'EPSG:3857'),
		  zoom: 10
		})
	});

	function backNoAnim() {
    map.getView().setCenter(ol.proj.transform([104, 30], 'EPSG:4326', 'EPSG:3857'));
	}

	function backWithAnim() {
		var pan = ol.animation.pan({
      duration: 2000,
      source: map.getView().getCenter()
    });
    map.beforeRender(pan);
    map.getView().setCenter(ol.proj.transform([104, 30], 'EPSG:4326', 'EPSG:3857'));
	}
	
</script>

先把地图移动到北京，再点击下方的两个按钮，感受一下带动画，和不带动画的差别，绝大多数人还是会喜欢带动画的。 无疑，动画具有很大的吸引力。 本章节将把你带入OpenLayers 3的动画世界，让你也能应用动画效果，做出漂亮的效果。
