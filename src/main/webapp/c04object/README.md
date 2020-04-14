JavaScript
js对象：
   1.定义
        1.var p = {};   
        2.var p = new Object（）；  有个老祖宗，Object。
        3.构造函数
   2.内置对象
        1.String字符串对象
        2.Date日期对象
        3.Array数组对象
        4.Function函数对象
            每一个函数都有一个arguments对象，它包括了函数所要调的参数，通常我们把它当作数组使用
        还有 Boolean对象;4.Math对象;5.Number对象;6.Object对象;7.RegExp对象;9.Global对象;等等
   3.浏览器window对象
        1.有全局的变量都是window的属性，在函数外面声明或者函数内部
        2.所有全局的函数都是window的方法
            使用var定义变量，则方法外是全局变量，方法内是局部变量。
            不使用var定义变量，则是全局变量，但是需要函数执行一下，方法内部定义的全局变量才有效。
        常用内置函数：
            escape()、eval()【计算 JavaScript 字符串，并把它作为脚本代码来执行。】等等
            alert()、confirm、prompt
            setTimeout("要执行的函数"，毫秒)：多少毫秒后执行一次
            setInterval("要执行的函数"，毫秒)：每间隔多少毫秒后执行一次
            open("地址")：打开窗口
        常用属性
            onload=func()：文档加载完毕后执行   也等于=body标签上行 onload="func()"
            onresize=func()：浏览器窗口大小发生变化后执行  
        浏览器中有文档，文档有document对象。
        document是window的一个对象属性。Window 对象表示浏览器中打开的窗口。
        如果文档包含框架（frame 或 iframe 标签），浏览器会为 HTML 文档创建一个 window 对象，并为每个框架创建一个额外的 window 对象。
        document   对 Document 对象的只读引用。
   4.函数对象
        一，普通函数
            function 函数名 (参数){ 函数体;
                return 返回值;
            }
        二.函数调用形式
            1.
                function add(){
                  alert("函数被调用了")；
                  alert(this);//当前的this指向了window
                //执行的一些操作
                }   
                //2.函数的执行
                add()；
            2.
                var add = function(){
                    alert('函数被调用了')；
                }
                add()
                
        
   
   