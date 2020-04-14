JavaScript
实例原型：
   1.实例原型简介：
        在声明了一个函数之后，浏览器会自动按照一定的规则创建一个对象，这个对象就叫做原型对象。这个原型对象其实是储存在了内存当中。
   2.函数、实例、实例原型，三者关系：
        函数的prototype属性指向实例原型，
        实例的__proto__属性指向实例原型。
        实例原型的constructor属性指向构造函数（声明的函数）。
   3.原型链
        当读取实例的属性时，如果实例中找不到，就会查找与对象关联的原型中的属性，如果还查不到，就去找原型的原型，一直找到最顶层为止。
        最顶层为Object.prototype。也就是说Object.prototype.__proto__的值为null。
        实例属性访问顺序：对象-原型-上一级原型-...最顶层原型，找不到则返回undefined 
            function Person() {}
            var person = new Person();
            console.log(person.name) // undefined           
            Person.prototype.name = 'xiaoming';
            person.name = 'hhh';
            console.log(person.name) // hhh           
            delete person.name;
            console.log(person.name) // xiaoming
