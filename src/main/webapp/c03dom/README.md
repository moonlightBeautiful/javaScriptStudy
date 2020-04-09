JavaScript
DOM节点：
   1.处理DOM事件
        1.事件类型
        2.事件绑定
            1.行内绑定  <标签 事件="">
            2.js绑定  document.getElementById("id").事件= ；
   2.操作DOM节点
        1.获取
            document.getElementById("#s")
        2.创建
            var para = document.createElement("p标签");
            var node = document.createTextNode("...前...内容");
            para.appendChild(node);
        3.修改
            从新赋值或者修改属性值 
        4.添加
            必须知道父节点，插入到父节点内容部
            parent.insertBefore(要插入的节点, parent的son之前插入);
            parent.appendChild(要插入的节点); //作为parent的最后一个son插入
        5.删除
            必须知道父节点
            parent.removeChild(son1);  //移除parent的孩子son1
   3.修改DOM节点样式
        style属性.样式属性="值"
   