1.js hello
    简介：js是浏览器脚本语言
2.js 基础
    1.引入方式：
        1.内部
        2.外部
    2.注释：
        1.单行：//
        2.多行：/* */
    3.变量：
        统一用var，弱语言类型，类型随时可变。
    4.基本数据类型：
        1.数值类型
        2.字符串类型
        3.布尔类型
        4.undefined
        5.null
    5.运算符
        1.算术运算符： = + - * / % ++ ()
        2.比较运算符： ==值相等  ===值和类型相等  !=  >  >= <=
        3.逻辑运算符： && || !
        4.三目运算符： x>y?x:y
    6.选择和循环语句：
        1.if else
        2.switch case break default
        3.for
        4.while do while
    7.函数：可重载，return直接结束函数
        function 函数名(入参){函数体}
    8.continue break
3.JS DOM
    1.操作dom节点事件
        给HTML标签添加onclick事件，然后js函数写这个事件的函数
    2.操作dom
        修改dom节点的值
            document.getElementById().innerHTML="";     //容器 比如div
            document.getElementById().value="";   //非容器 比如 input text
        添加dom节点
            创建节点元素和节点值，然后得到父节点，在父节点的里面添加
            var para = document.createElement("p");
            var node = document.createTextNode("...前...");
            var para2 = document.createElement("p");
            var node2 = document.createTextNode("...后...");
            para.appendChild(node);
            para2.appendChild(node2);
            var parent = document.getElementById("parent");
            var son1 = document.getElementById("son1");
            parent.insertBefore(para, son1);
            parent.appendChild(para2);
        删除dom节点
            得到父节点，删除子节点
             var parent = document.getElementById("parent");
             var son1 = document.getElementById("son1");
             parent.removeChild(son1);
    3.操作dim节点样式
        .style.样式=""
        document.getElementById("gril").style.color = "red";
4.js 对象
    1.原型 没搞懂
    2.实例化一个对象：var 对象 = new Object();
    3.动态添加属性：对象.随便取个属性名 = 值；
    4.动态添加方法：对象.随便取个方法名 = 函数名，不用带括号和入参；
    5.删除属性和方法：
        delete 对象.属性	或者  对象.属性 = undefined   //动态删除属性
        delete 对象.方法	 或者  p.方法 = undefined    //动态删除方法,不用写()和参数
    6.对象构造方法：
        function 方法名(参数1，参数2){
            var 变量 = "私有属性";   	//私有属性，私有属性不是对象属性，但是可以在内部使用
            this.属性名11=参数1；	 //对象添加属性
            this.属性名22=参数2；	 //对象添加属性
            this.方法名1=function(){	 //对象添加方法
                //这里面可以访问外面的对象属性this.属性和私有属性
            }；
            this.方法名22=方法名2；
            function 方法名2(){		//私有方法，私有方法不是对象方法，但是可以在内部使用
                //这里面可以访问外面的对象属性this.属性和私有属性
            }
        }
        var p = new 方法名(参数1，参数2);
        p.对象属性
        p.对象方法名(入参)
    7.内置对象：
        1.字符串对
            实例化：
                var s1="实例化字符串方式一";
                var s2=new String("实例化字符串abc方式二");
            常用方法：
                s2.length：字符串长度
                s2.indexOf("abc", 0)：返回指定字符串在s2中首次出现的位置，可以指定位置开始
                s2.replace("abc", "java1234")：返回替换后的字符串,源字符串
        2.日期：var date = new Date();
            date.getTime()：1970年1月1日至今的毫秒数
            date.getFullYear()： 年
            date.getMonth()：月 从0开始（0-11）
            date.getDate()：日，在一个月中的某一日（1-31）
            date.getHours()：时（0-23）
            date.getMinutes()：分（0-59）
            date.getSeconds()：秒（0-59）
            date.getDay()：日，在一个星期中的某一日，从0开始。（0-6）
        3.数组：var arr = new Array();
            arr[0] = "jack";   //长度和值是动态的
            arr[1] = "marry";
            arr.sort()      //排序，会改变原数组
            arr.join("字符")      //把数组的值串联起来，可以指定字符，不指定则是逗号
            arr.concat(arr2)    //把数组1和数组2的值用，逗号串联起来
            arr.reverse()   //颠倒，会改变原数组
5.js 常用函数
     1.全局函数：不属于任何一个对象
        1.eavl():计算字符串表达式，也可以把json字符串转换成json对象
     2.window对象常用函数
        1.alert()
        2.confirm()
        3.prompt()
        4.setTimeout("指定函数",毫秒)：只执行一次
        5.setInterval("指定函数",毫秒)：指定间隔执行
        6.open("url"[其他参数自己选择])：打开窗口
        7.onload=函数 或者 body标签onload=函数：文档加载完毕
        8.onresize=函数：窗口大小发生变化
6.js function对象
      1.方法声明
      2.函数对象实例化2中方式、使用
      2.方法和属性
7.js 闭包 外部读取函数内部的句部变量
    1.变量的作用域：局部和全局
    2.内函数
8.js 面向对象
    1.三大特性：封装、继承、多态
    2.封装就不多说了
    3.继承：2种方式
        1.apply(this,参数)：把别的函数的实现属性和方法的引用过来，继承。本身类型不会变。
            this:子函数对象
            参数：子函数参数
        2.子类型.prototype = new 父类型();
            prototype表示了一个类的属性的集合
    4.多态：子类型.prototype = new 父类型();
        多个子类型 instanceOf 父类型
        
       
工作中的获得：
    1.在js文件中，引入其他的js文件
        document.write("<script src='.js'></script>");