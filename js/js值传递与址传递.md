# js值传递与址传递

标签（空格分隔）： js

---

#### 1.基本数据类型与引用数据类型最大的区别实际就是传值与传址的区别。

###### 1.1 值传递：基本类型采用的是值传递。

```js
var a = 100; //定义一个变量a并赋值100
var b = a; //将a的值100赋给b(a、b都是基本类型：值传递)
b++; //b自加
console.log(a); //100
console.log(b); //101
```

###### 1.2 址传递：引用类型则是地址传递，将存在栈内存中的地址赋值给接收的变量。

```js
var a = [1, 2, 3]; // 数组是引用类型
var b = a; //地址传递：将a的地址传递给b，a、b指向同一块地址
b.push(4); //给b数组末尾追加一个4
console.log(b); //[1, 2, 3, 4]
console.log(a); //[1, 2, 3, 4]
```

>分析：由于a和b都是引用类型，采用的是址传递，即a将地址传递给b，那么a和b必然指向同一个地址（引用类型的地址存放在栈内存中），而这个地址都指向了堆内存中引用类型的值。当b改变了这个值的同时，因为a的地址也指向了这个值，故a的值也跟着变化。

>就好比a租了一间房，将这间房的地址给了b，b通过地址找到了房间，那么b对房间做的任何改变（添加一些绿色植物）对a来说同样是可见的。






