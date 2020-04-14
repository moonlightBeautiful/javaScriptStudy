JavaScript
js面向对象：
   1.三大特征
        封装、继承、多态
        js本身没有这些特性，但是可以模拟实现。
   2.自定义对象
        1.对象初始化器方式
        2.构造函数方式
   3.对象和类属性   
   4.对象和类方法
   5.封装
        对象有方法和属性
   6.继承
        1.apply，子函数内部使用：父函数.apply（this，arguments）          
            子函数 对象 = new 子函数()
            本身原型不改变
        2.apply，子函数内部使用：父函数.apply（this，arguments）
            子函数.prototype = new 父函数();  //原型继承
            子函数 对象 = new 子函数()
            本身原型改变
   7.多态
        继承的基础上，instanceof