# 常见问题

* Q: ol3支持gif吗？

  A: ol.style.Icon并不支持，但可以通过ol.Overlay来加载dom的方式支持。注意：在一个地图中如果存在几千个overlay，将影响效率。
  
* Q: 地图缩小后，在一个页面出现多个一样的地图，如何才能只显示一个？

  A: 在创建source的时候，设置wrapX属性为false就可以。
  

