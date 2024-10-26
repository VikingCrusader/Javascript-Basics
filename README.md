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
