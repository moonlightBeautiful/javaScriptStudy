JavaScript
简介：
    简单的讲，就是轻量级网页脚本弱语言。
组成：
    1.ECMAScript，描述了该语言的语法和基本对象。
    2.文档对象模型（DOM），主要是用来把文档解析成DOM树。例如获取或者设置input表单的value值。
        有XML DOM 和 HTML DOM 2种DOM。
        document对象是DOM的顶层对象。
    3.浏览器对象模型（BOM），由多个对象组成，通过这些对象与浏览器进行交互。例如：新建窗口、获取屏幕分辨率、浏览器版本号等。
        window对象是BOM的顶层(核心)对象，其他所有对象都是通过它延伸出来的，也可以称为window对象的属性。
        还有其他对象：location对象、navigator对象、history对象等
        如果在全局环境中用var定义了对象、变量或函数都会被添加到window对象中
document与window对象的联系
    简单来说，document是window的一个对象属性。document   对 Document 对象的只读引用。
    Window 对象表示浏览器中打开的窗口。
    document 独享标识浏览器中打开的文档。
    如果浏览器中的文档包含框架（frame 或 iframe 标签），则浏览器会为每个框架创建一个额外的 window 对象。
    所有的全局函数和对象都属于Window 对象的属性和方法。
使用
    1.直接写在script标签对中       
    2.写在js文件中，然后引入 <script src="外部的js文件">  </script>