# forum-ads
论坛使用的广告模块

### 安装说明
1. 安装jQuery
```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.min.js"></script>
```
由于NodeBB自带jQuery所以不用在NodeBB中安装
2. 安装bootstrap carousel JS
~~~
<script src="https://bootstrapdocs.com/v2.0.3/docs/assets/js/bootstrap-carousel.js"></script>
~~~
在NodeBB中`Appearance > Custom HTML/CSS > Custom Header`
3. 安装bootstrap carousel CSS

复制bootstrap.carousel.min.css内容。在NodeBB中，黏贴到`Appearance > Custom HTML/CSS > Custom CSS`
4. 打开widget.html

### 模块维护
1. 替换widget.html中的ads value的图片链接array。使用atom, sublime或bracket可以看到图片预览
2. 将内容通过[minifier](https://kangax.github.io/html-minifier/)轻量化
3. 使用轻量化内容替换NodeBB `Extend > Widgets > Global Footer`内容
4. **新版块**：在版块url中寻找版块id，并在ads中添加新key & value pair

**所有value必须是array**

##### KEY
~~~
-1 HOME
11 NEW
8 SALE
7 CAR
6 HOUSE
12 OTHER
~~~

### Known Issues
- Performance: jQuery添加图片很慢。目前load速度大概要5秒以上
  - 预计解决方案：改为html模块，通过JS更改可见模式

