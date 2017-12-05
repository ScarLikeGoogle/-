# CJPCD
简介
CJPCD 是一款原生开源的 javascript 插件，用于生成省市区选择器，基本用法十分简单。
使用方法
最简单的使用只需要两个步骤：

#### 1.放置容器，引入依赖<br/>
存放省市区数据的三个 select
```
<select id="province"></select>
<select id="city"></select>
<select id="district"></select>
```
引入插件
```
<script src="./cj-pcd-1.0.1.min.js"></script>
```

#### 2.调用方法
```
var pcd = new CJPCD('province','city','district');
```
效果如下图

