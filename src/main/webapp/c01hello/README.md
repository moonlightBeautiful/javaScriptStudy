JavaScript
简介：
    简单的讲，就是轻量级网页脚本弱语言。
组成：
    1.ECMAScript，描述了该语言的语法和基本对象。
    2.文档对象模型（DOM），主要是用来把文档解析成DOM树。例如获取或者设置input表单的value值。
        有XML DOM 和 HTML DOM 2种DOM。
    3.浏览器对象模型（BOM），由多个对象组成，通过这些对象与浏览器进行交互。例如：新建窗口、获取屏幕分辨率、浏览器版本号等。
        window对象是BOM的顶层(核心)对象，所有对象都是通过它延伸出来的，也可以称为window的子对象。
        还有其他对象：location对象、navigator对象、history对象等
        如果在全局环境中用var定义了对象、变量或函数都会被添加到window对象中
使用
    写在script标签对中       