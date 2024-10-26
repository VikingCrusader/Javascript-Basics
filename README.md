# Javascript-Basics         
1.let 和 var 的区别       
var在同一作用域可以重复声明，let不行，否则会报错！

2. const 具有 let 的所有出色功能，另外还有一个额外的好处，即使用 const 声明的变量是只读的。 它们是一个常量值，这意味着一旦一个变量被赋值为 const，它就不能被重新赋值
你应该始终使用 const 关键字命名不想重新分配的变量。 这有助于避免给一个常量进行额外的再次赋值。
注意，大多数时候，常量用大写字母表示，而变量的命名多使用驼峰命名法！

3.字符串里面如果想要有引号怎么办？
这么办：const myStr = "I am a \"double quoted\" string inside \"double quotes\"."; 
这样也可以：单引号表示字符串内，可以随便用双引号！ const myStr = '<a href="http://www.example.com" target="_blank">Link</a>';

4. \n换行 \t制表 \\反斜杠（单），可以在引号中使用    

5.JS字符串拼接使用+号           
const ourStr = "I come first. " + "I come second.";
字符串插入元素：引引加加  

6.输出字符串长度，用.length方法
lastNameLength = lastName.length;

7.获取字符串中第一个字符的长度
firstLetterOfLastName = lastName[0]; 

8.字符串不能直接修改一部分，但是可以完全重新编辑

let myStr = "Bob";
myStr[0] = "J"; //这样会报错

let myStr = "Bob";
myStr = "Job"; //能且只能这样

9.获取字符串最后一个元素的一个小技巧
const lastLetterOfLastName = lastName[lastName.length-1];

10.js二维数组创建
const myArray = [[1,2],[3,4]];

11.二维数组 例子
const myArray = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14],
];
const myData = myArray[2][1];//是8

12.数组：push()方法
push() 方法需要一个或多个 参数 并将它们根据出现顺序追加到数组的末尾。 它返回数组的新长度
var myArray = [["John", 23], ["cat", 2]];
myArray.push(["dog", 3]);

13.数组：pop()方法
.pop() 函数用来弹出一个数组末尾的值。 我们可以把这个弹出的值赋给一个变量存储起来。 换句话说就是 .pop() 函数移除数组末尾的元素并返回这个元素。
const myArray = [["John", 23], ["cat", 2]];
var removedFromMyArray = myArray.pop();
输出： MyArray.pop 返回 : [["cat", 2]]
      myArray 剩余 ：[["John", 23]]   

14.数组：shift()方法
与pop()原理一样，唯一不同的就是它移除的是第一个元素，而不是最后一个

15. 数组：unshift()方法
与shift()原理一样，唯一不同的就是它添加元素在数组最前面，类似于开头版本的push().   
