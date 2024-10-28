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

16.创建函数
function reusablefunction() {
  console.log("Hi World");
}

17.作用域
未使用 let 或 const 关键字声明的变量（例如var）会在 global 范围内自动创建。 当在代码其他地方无意间定义了一个变量，刚好变量名与全局变量相同，这时会产生意想不到的后果。 你应该总是用 let 或 const 声明你的变量。
在函数内部定义的变量，只属于此函数的局部作用域，并不影响此函数外面的.
const outerWear = "T-Shirt";
function myOutfit() {
  let outerWear = 'sweater'; //局部作用域（函数内重载）    
  return outerWear;
}
myOutfit();

18.严格相等
严格相等 ( ===) 是相等运算符 ( ) 的对应项==。但是，与尝试将两个被比较的值转换为通用类型的相等运算符不同，严格相等运算符不执行类型转换。
3 ===  3  // true  
3 === '3' // false
不严格相等:!==

19. switch 记住冒号和break,还有default表示未找到匹配项的时候输出的结果
    switch(val){
    case 1:
      answer = 'alpha';
      break;
    case 2:
      answer = 'beta';
      break;
    case 3:
      answer = 'gamma';
      break;
    case 4:
      answer = 'delta';
      break;
    default:
      answer = 'stuff';
      break;
  }
注意case不是数字的时候带引号，例如 case "a":  
下面这样也行，那么就是1，2，3都可以输出Low
    case 1:
    case 2:
    case 3:
      answer = 'Low';
    
21. return a<b; 意思是，如果a<b，就返回True，否则返回False

22. JS 对象的创建
  const myDog = {
  name:'wangcai',
  legs:4,
  tails:1,
  friends:['miao','miaomiao']
};

23.对象的访问：点访问法 
const hatValue = testObj.hat;
方括号访问法：不常用，但是要了解
注意，如果属性名中包含空格，就必须使用引号（单引号或双引号）将它们包裹起来。
const testObj = {
  "an entree": "hamburger",
  "my side": "veggies",
  "the drink": "water"
};
const entreeValue = testObj["an entree"];   
const drinkValue = testObj["the drink"];     

24.给对象添加新属性：直接添加
const myDog = {
  "name": "Happy Coder",  
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"]
};
myDog.bark = 'woof';

25.delete关键字：删除对象中的属性
const myDog = {
  "name": "Happy Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"],
  "bark": "woof"
};

delete myDog.tails;

26.haveOwnProperty()方法
要检查给定对象上的属性是否存在，可以使用该.hasOwnProperty()方法。someObject.hasOwnProperty(someProperty)返回true或false取决于是否在对象上找到该属性。
语法如下：
function checkForProperty(object, property) {
  return object.hasOwnProperty(property);
}

27.访问嵌套对象的属性
我们可以叠加点和方括号
const myStorage = {
  "car": {
    "inside": {
      "glove box": "maps",
      "passenger seat": "crumbs"
     },
    "outside": {
      "trunk": "jack"
    }
  }
};

const gloveBoxContents = myStorage.car.inside["glove box"];

28.访问数组对象的属性
const myPlants = [
  {
    type: "flowers",
    list: [
      "rose",
      "tulip",
      "dandelion"
    ]
  },
  {
    type: "trees",
    list: [
      "fir",
      "pine",
      "birch"
    ]
  }
];

const secondTree = myPlants[1].list[1];

29.多维数组
function multiplyAll(arr) {
  let product = 1;
  for (let i=0; i<arr.length; i++){
    for (let j=0; j<arr[i].length;j++){
      product *= arr[i][j];
    }
  }
  return product;
}

multiplyAll([[1, 2], [3, 4], [5, 6, 7]]);

30.调用 Math.random()，
生成并返回 0 和 9 之间的随机整数。
return Math.floor(Math.random()*10);

返回一个在 myMin（包括 myMin）和 myMax（包括 myMax）之间的随机整数。
function randomRange(myMin, myMax) {
  var a = Math.floor((myMax-myMin+1)*Math.random())+myMin;
  return a;
}

31. parseInt(str) 字符串转化为数字
 const a = parseInt("007"); 默认转化为十进制
const a = parseInt("11", 2); 转化为二进制

32.三元运算符 ？：    
function findGreater(a, b) {
  return a > b ? "a is greater" : "b is greater or equal";
}

function findGreaterOrEqual(a, b) {
  return (a === b) ? "a and b are equal" : (a > b) ? "a is greater" : "b is greater";
}
