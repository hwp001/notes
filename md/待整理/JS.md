# JS

### document.write()

[简单语法介绍](https://blog.csdn.net/Jzsn_Paul/article/details/80025683)

### 语法类型

##### typeof()

- [详解](https://blog.csdn.net/wang01ping/article/details/80953553)

- 参数为一个变量，判断变量的数据类型

- number

- string 

- object

  - 数组是一个对象

  - null

  - a

    ```js
    var a = new String('zhangsan');
    ```

- function

- boolean

- undefined

  - 未定义的数据类型

##### setTimeout()

- 单次定时

##### setInterval()

- 多次定时

##### toUpperCase()

- 小写转换为大写

- ```js
  str.toUpperCase()
  ```

##### toLowerCase()

- 大写转换为小写

- ```js
  str.toLowerCase()
  ```

##### getFullYear()

- 获取年份

##### getMonth()

- 获取月份

##### getHours()

- 获取小时

##### getDate()

- 获取日期

##### getMinutes()

- 获取分钟

##### getSeconds()

- 获取秒

##### instanceof()

- 判断是否是实例对象



### 文档流（DOM）

##### document.getElementById('img')

- 获取文档流节点里面的id值

##### document.getElementsByClassName()

- 获取文档中的类名
- document.getElementsByClassName()[0]
  - 文档流一切皆节点，类名可以有很多个

##### document.getElementsByTagName()

- 获取文档中的html标签
- document.getElementSByTagName()[0]

##### innerText

- 获取对象的内容
- x.innerText

##### innerHtml

- 获取对象中的内容（包含html标签）

### 数组操作

- ##### 统计数组长度的时候，只统计索引数组，不统计关联数组，默认是索引数组

##### push()

- 数组尾部添加元素

  ```js
  arr.push(6)	
  ```

##### unshift()

- 数组头部添加元素

  ```js
  arr.unshift(0)
  ```

##### pop()

- 删除尾部元素

  ```js
  arr.pop()
  ```

##### shift()

- 删除头部元素

  ```js
  arr.shift()
  ```

##### join()

- 把数组拆分成为字符串

  ```js
  var list = ['name','age','sex'];
  console.log(list.join('#'));
  ```

##### concat()

- 合并数组

  ```php
  arr.concat(arr1)
  ```


### 函数

##### 构造函数

- 内容较多自查

- [first](https://www.cnblogs.com/wuyaxing/p/6415844.html)

- 工厂模式（函数里面写对象，返回对象）

- new关键字使用自定义的构造函数去创建对象

- 

  ```js
  	function Student(name,age){
  		//添加属性
  		this.name = name;
  		this.age = age;
  		
  		//添加方法
  		this.sing = function(){
  			return this.name+this.age;
  		};
  	}
  	var ps1 = new Student("jack",100);
  	var ps2 = new Student("jack",100);
  
  	console.log(ps1.sing());//方法
  	console.log(ps2.sing);//对象
  	console.log(ps1.sing == ps2.sing) //false
  	//实例化对象，不是原型对象，所以调用的不是同一块内存区域
  output:
  1、jack100
  2、内存地址，类似一个对象
  ```

  























