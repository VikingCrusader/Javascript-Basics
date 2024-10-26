# Javascript-Basics         
1.let 和 var 的区别       
var在同一作用域可以重复声明，let不行，否则会报错！ 
2. const 具有 let 的所有出色功能，另外还有一个额外的好处，即使用 const 声明的变量是只读的。 它们是一个常量值，这意味着一旦一个变量被赋值为 const，它就不能被重新赋值

你应该始终使用 const 关键字命名不想重新分配的变量。 这有助于避免给一个常量进行额外的再次赋值。

注意，大多数时候，常量用大写字母表示，而变量的命名多使用驼峰命名法！ 
3.字符串里面如果想要有引号怎么办？ 
这么办：const myStr = "I am a \"double quoted\" string inside \"double quotes\"."; 
这样也可以：单引号表示字符串内，可以随便用双引号！ const myStr = '<a href="http://www.example.com" target="_blank">Link</a>';

