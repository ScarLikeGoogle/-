# CJPCD
简介
CJPCD 是一款原生开源的 javascript 插件，用于生成省市区选择器，基本用法十分简单。
注明:项目是从这位老兄star过来的https://github.com/nicolahery/markdownpad-github
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

小记:
Module模块化开发:有点像Java面向对象编程中的类，例如JsonHelper 专门负责 json 解析，FilesUpload,专门用来做文件上传的。<br/>
每一个模块负责一个功能的实现<br/>
插件就是采用模块化思想开发的
```
<!DOCTYPE html>
    <html>
    <head>
        <title>Module</title>
    </head>
    <body>
        <div Id="hello"></div>
        <div Id="hi"></div>
        <script type="text/javascript">
            var HelloWorld = function(objId){
                var _get_dom = function(Id){
                    return document.getElementById(Id);
                }
                var _aim_obj = _get_dom(objId);
                var _say_hello = function(str){
                    _aim_obj.innerHTML = str;
                }
                return{
                    sayHello:_say_hello
                }
            }
            var Hei = new HelloWorld('hello');
            Hei.sayHello('hello world');
            
            var Hei = new HelloWorld('hi');
            Hei.sayHello('hello world');        
        </script>
    </body>
    </html>
```
上面例子中HelloWorld就是模块，_get_dom、_say_hello都是内部函数（方法），外部是不能调用的；
return中sayHello就是给外部调用的API，参数是objId，即dom节点的id
所以调用方法就是new HelloWorld('hello world')
