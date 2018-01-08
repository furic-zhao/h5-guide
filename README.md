## 移动端(H5专属规范)

### 代码结构规范

请参考：[Mobile Boilerplate](https://html5boilerplate.com/mobile/)

```
<!DOCTYPE html>
<html class="no-js">
    <head>
        <meta charset="utf-8">
        <title></title>
        <meta name="description" content="">
        <meta name="HandheldFriendly" content="True">
        <meta name="MobileOptimized" content="320">
        <meta name="viewport" content="width=device-width, initial-scale=1, minimal-ui">
        <meta http-equiv="cleartype" content="on">

        <link rel="apple-touch-icon-precomposed" sizes="144x144" href="img/touch/apple-touch-icon-144x144-precomposed.png">
        <link rel="apple-touch-icon-precomposed" sizes="114x114" href="img/touch/apple-touch-icon-114x114-precomposed.png">
        <link rel="apple-touch-icon-precomposed" sizes="72x72" href="img/touch/apple-touch-icon-72x72-precomposed.png">
        <link rel="apple-touch-icon-precomposed" href="img/touch/apple-touch-icon-57x57-precomposed.png">
        <link rel="shortcut icon" sizes="196x196" href="img/touch/touch-icon-196x196.png">
        <link rel="shortcut icon" href="img/touch/apple-touch-icon.png">

        <!-- Tile icon for Win8 (144x144 + tile color) -->
        <meta name="msapplication-TileImage" content="img/touch/apple-touch-icon-144x144-precomposed.png">
        <meta name="msapplication-TileColor" content="#222222">

        <!-- SEO: If mobile URL is different from desktop URL, add a canonical link to the desktop page -->
        <!--
        <link rel="canonical" href="http://www.example.com/" >
        -->

        <!-- Add to homescreen for Chrome on Android -->
        <!--
        <meta name="mobile-web-app-capable" content="yes">
        -->

        <!-- For iOS web apps. Delete if not needed. https://github.com/h5bp/mobile-boilerplate/issues/94 -->
        <!--
        <meta name="apple-mobile-web-app-capable" content="yes">
        <meta name="apple-mobile-web-app-status-bar-style" content="black">
        <meta name="apple-mobile-web-app-title" content="">
        -->

        <!-- This script prevents links from opening in Mobile Safari. https://gist.github.com/1042026 -->
        <!--
        <script>(function(a,b,c){if(c in b&&b[c]){var d,e=a.location,f=/^(a|html)$/i;a.addEventListener("click",function(a){d=a.target;while(!f.test(d.nodeName))d=d.parentNode;"href"in d&&(d.href.indexOf("http")||~d.href.indexOf(e.host))&&(a.preventDefault(),e.href=d.href)},!1)}})(document,window.navigator,"standalone")</script>
        -->

        <link rel="stylesheet" href="css/normalize.css">
        <link rel="stylesheet" href="css/main.css">
        <script src="js/vendor/modernizr-2.7.1.min.js"></script>
    </head>
    <body>

        <!-- Add your site or application content here -->
        <script src="js/helper.js"></script>
        <script src="js/main.js"></script>
    </body>
</html>

```
### 移动端字体设置最佳实践

```css
body {
    font-family: -apple-system, BlinkMacSystemFont, "PingFang SC","Helvetica Neue",STHeiti,"Microsoft Yahei",Tahoma,Simsun,sans-serif;

}
```

iOS 4.0+ （iOS 9以下系统已经非常少） 使用英文字体 Helvetica Neue，之前的iOS版本降级使用 Helvetica。
中文字体设置为华文黑体STHeiTi。

iOS 9+ Safari开始支持 -apple-system 参数， Chrome 使用 BlinkMacSystemFont ，兼容 iOS ／ MacOS     

`微软雅黑`是为了兼容Win系统，毕竟视网膜分辨率的win系统用`Simsun`是非常丑陋的，可以用4K屏 windows 去看 JD 淘宝，你能忍的话我就没话说

`PingFang SC` 是简体苹方，看需要 如果要命中对应 苹方字体的话 直接写  PingFang 不带引号。


需补充说明，华文黑体并不存在iOS的字体库中(http://support.apple.com/kb/HT5484?viewlocale=en_US)，
但系统会自动将华文黑体STHeiTi兼容命中系统默认中文字体黑体-简或黑体-繁：

```
Heiti SC Light 黑体-简 细体
Heiti SC Medium 黑体-简 中黑
Heiti TC Light 黑体-繁 细体
Heiti TC Medium 黑体-繁 中黑
```

原生Android下中文字体与英文字体都选择默认的无衬线字体。

4.0之前版本英文字体原生Android使用的是Droid Sans，中文字体原生Android会命中Droid Sans Fallback。

4.0+ 中英文字体都会使用原生Android新的Roboto字体。

其他第三方Android系统也一致选择默认的无衬线字体。

Android 就直接让它命中系统字体吧，因为你无法预知发行厂商会去内置什么字体，或者人家root去修改什么字体。

**参考阅读**
* [Droid, the default font for older versions of Android](http://en.wikipedia.org/wiki/Droid_fonts)
* [Roboto, the default font for newer versions of Android](http://en.wikipedia.org/wiki/Roboto)

### 移动端开发资源和工具

* [iOS5 Web调试工具iWebinspector](http://www.iwebinspector.com/) 

* [html5与css3技术应用评估](http://html5please.com/ "html5与css3技术应用评估")
 
* [各种奇妙的hack](http://browserhacks.com/ "各种奇妙的hack")
 
* [几乎所有设备的屏幕尺寸与像素密度表](http://en.wikipedia.org/wiki/List_of_displays_by_pixel_density "几乎所有设备的屏幕尺寸与像素密度表")
 
* [ios端移动设备参数速查](http://ivomynttinen.com/blog/the-ios-design-cheat-sheet-volume-2/ "ios端移动设备参数速查")
 
* [浏览器兼容表](http://www.quirksmode.org/compatibility.html "浏览器兼容表")
 
* [移动设备查询器](https://deviceatlas.com/device-data/devices "移动设备查询器")
 
* [移动设备适配库](http://51degrees.codeplex.com/ "移动设备适配库")
 
* [viewport与设备尺寸在线检测器](https://deviceatlas.com/device-data/devices "viewport与设备尺寸在线检测器")
 
* [html5移动端兼容性速查](http://mobilehtml5.org/ "html5移动端兼容性速查")
 
* [在线转换字体](http://www.fontsquirrel.com/tools/webfont-generator "在线转换字体")
 
* [css3选择器测试](http://tools.css3.info/selectors-test/test.html "css3选择器测试")
 
* [兼容性速查表](http://caniuse.com/ "兼容性速查表")
 
* [浏览器的一些独特参数](http://www.browserscope.org/ "浏览器的一些独特参数")
 
* [各种各样的媒体查询收集](http://nmsdvid.com/snippets/ "各种各样的媒体查询收集")
 
* [css3动画在线制作器](http://ecd.tencent.com/css3/tools.html "css3动画在线制作器")
 
* [css3渐变在线制作器](http://www.colorzilla.com/gradient-editor/ "css3渐变在线制作器")

* [赛贝尔曲线在线制作器](http://cubic-bezier.com/ "赛贝尔曲线制作器")

* [flexbox在线制作器](http://the-echoplex.net/flexyboxes/ "flexbox在线制作器")

* [CSS3各种渲染效果在线工具（IE出品）](http://ie.microsoft.com/testdrive/Graphics/hands-on-css3/see-also.htm "CSS3各种渲染效果在线工具（IE出品）")
 
* [resize添加到收藏夹后，可直接在浏览器中出现各种分辨率的选择工具来查看不同分辨率下的页面效果](http://lab.maltewassermann.com/viewport-resizer/ "resize")

* [移动端手势表](http://ww1.sinaimg.cn/large/c2c57f68jw1e4fh7dmw12j20fi2w6qe1.jpg "移动端手势表")

* [webkit独有的样式分析](http://ued.ctrip.com/blog/wp-content/webkitcss/ "webkit独有的样式分析")

* [地图地区分布配色方案选择工具](https://github.com/axismaps/colorbrewer/ "地图地区分布配色方案选择工具")

* [在线配色选择器](http://www.peise.net/tools/web/ "在线配色选择器")

### 移动端开发常见问题及解决方案汇总

####  伪类 :active 生效

要CSS伪类 `:active` 生效，只需要给 document 绑定 `touchstart` 或 `touchend` 事件

```
    <style>
    a {
      color: #000;
    }
    a:active {
      color: #fff;
    }
    </style>
    <a herf=foo >bar</a>
    <script>
      document.addEventListener('touchstart',function(){},false);
    </script>
```

####  消除 transition 闪屏

两个方法

```
    -webkit-transform-style: preserve-3d;
    /*设置内嵌的元素在 3D 空间如何呈现：保留 3D*/
    -webkit-backface-visibility: hidden;
    /*（设置进行转换的元素的背面在面对用户时是否可见：隐藏）*/
```

####  消除 IE10 里面的那个叉号

```
    input:-ms-clear{display:none;}
```

来源出处：[http://msdn.microsoft.com/en-us/library/windows/apps/hh767361.aspx](http://msdn.microsoft.com/en-us/library/windows/apps/hh767361.aspx "article4")

#### 关于 iOS 与 OS X 端字体的优化(横竖屏会出现字体加粗不一致等)
iOS 浏览器横屏时会重置字体大小，设置 `text-size-adjust` 为 `none` 可以解决 iOS 上的问题，但桌面版 Safari 的字体缩放功能会失效，因此最佳方案是将 `text-size-adjust` 为 `100%` 。

```
    -webkit-text-size-adjust: 100%;
    -ms-text-size-adjust: 100%;
	text-size-adjust: 100%;
```

####  JS 事件相关
click 事件普遍 300ms 的延迟
在手机上绑定 click 事件，会使得操作有 300ms 的延迟，体验并不是很好。
开发者大多数会使用封装的 tap 事件来代替 click 事件，所谓的 tap 事件由 touchstart 事件 + touchmove 判断 + touchend 事件封装组成

####  iOS 点击会慢 300ms 问题

 [https://developers.google.com/mobile/articles/fast_buttons?hl=de-DE](https://developers.google.com/mobile/articles/fast_buttons?hl=de-DE "article5")
 [http://stackoverflow.com/questions/12238587/eliminate-300ms-delay-on-click-events-in-mobile-safari](http://stackoverflow.com/questions/12238587/eliminate-300ms-delay-on-click-events-in-mobile-safari "article5")

使用 CSS3 动画的时尽量利用3D加速，从而使得动画变得流畅。动画过程中的动画闪白可以通过 backface-visibility 隐藏。

```
    -webkit-transform-style: preserve-3d;
    -webkit-backface-visibility: hidden;
```

####  IE10 的特殊鼠标事件

[http://www.mansonchor.com/blog/blog_detail_73.html](http://www.mansonchor.com/blog/blog_detail_73.html "article5")

####  不让 Android 手机识别邮箱

```
    <meta content="email=no" name="format-detection" />
```

####  禁止 iOS 识别长串数字为电话

```
    <meta content="telephone=no" name="format-detection" />
```

####  禁止 iOS 弹出各种操作窗口

```
    -webkit-touch-callout:none
```

####  禁止用户选中文字

```
    -webkit-user-select:none
```

####  动画效果中，使用 translate 比使用定位性能高

<http://paulirish.com/2012/why-moving-elements-with-translate-is-better-than-posabs-topleft/>

####  获取滚动条

```
    window.scrollY
    window.scrollX
```

 比如要绑定一个 touchmove 的事件，正常的情况下类似这样(来自呼吸二氧化碳)

```
    $('div').on('touchmove', function(){
       //.….code
    });
```

而如果中间的 code 需要处理的东西多的话，FPS 就会下降影响程序顺滑度，而如果改成这样

```
    $('div').on('touchmove', function(){
       setTimeout(function(){
         //.….code
       },0);
    });
```

把代码放在 setTimeout 中，会发现程序变快.

####  关于 iOS 系统中，WebAPP 启动图片在不同设备上的适应性设置

[http://stackoverflow.com/questions/4687698/mulitple-apple-touch-startup-image-resolutions-for-ios-web-app-esp-for-ipad/10011893#10011893](http://stackoverflow.com/questions/4687698/mulitple-apple-touch-startup-image-resolutions-for-ios-web-app-esp-for-ipad/10011893#10011893)

#### 移动端 HTML5 audio autoplay 失效问题

这个不是 BUG，由于自动播放网页中的音频或视频，会给用户带来一些困扰或者不必要的流量消耗，所以苹果系统和安卓系统通常都会禁止自动播放和使用 JS 的触发播放，必须由用户来触发才可以播放。

解决方法思路：先通过用户 touchstart 触碰，触发播放并暂停（音频开始加载，后面用 JS 再操作就没问题了）。

解决代码：

```
document.addEventListener('touchstart', function () {
    document.getElementsByTagName('audio')[0].play();
    document.getElementsByTagName('audio')[0].pause();
});
```
方案出处：[http://stackoverflow.com/questions/17350924/iphone-html5-audio-tag-not-working](http://stackoverflow.com/questions/17350924/iphone-html5-audio-tag-not-working)

扩展阅读：[http://yujiangshui.com/recent-projects-review/#toc-7](http://yujiangshui.com/recent-projects-review/#toc-7)

#### Android平台遮罩层下的input、select、a等元素可以被点击和focus(点击穿透)

  问题发现于三星手机，这个在特定需求下才会有，因此如果没有类似问题的可以不看。首先需求是浮层操作，在三星上被遮罩的元素依然可以获取focus、click、change. <a href="https://code.google.com/p/android/issues/detail?id=6721">bug issue</a> ，在查看bug报告list以后，找到了两种解决方案，第一是通过层显示以后加入对应的class名控制，第二是通过将可获取焦点元素加入的disabled属性，也可以利用属性加dom锁定的方式（disabled的一种变换方式）

#### 部分机型存在type为search的input，自带close按钮样式修改方法

  有些机型的搜索input控件会自带close按钮（一个伪元素），而通常为了兼容所有浏览器，我们会自己实现一个，此时去掉原生close按钮的方法为

```
	#Search::-webkit-search-cancel-button{
    	display: none;
	}
```

  如果想使用原生close按钮，又想使其符合设计风格，可以对这个伪元素的样式进行修改。

#### 唤起select的option展开
zepto方式:

```
$(sltElement).trrgger("mousedown");
```
原生js方式:
```
function showDropdown(sltElement) {
    var event;
    event = document.createEvent('MouseEvents');
    event.initMouseEvent('mousedown', true, true, window);
    sltElement.dispatchEvent(event);
};
```