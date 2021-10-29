## let  和const

let 通常用作变量：

- let str ="asdasd"
- let a =55

const 通常用作常量：

​	const PI =Math.PI

​	导入模块 conts mysql =require("mysql");



let能够防止变量穿透，不过写web 还是建议var 因为有些浏览器不支持





## 字符串模板

字符串拼接可以不使用+ 和“”   而使用 飘键  ·

- str =· my name is ${name}·   



## 箭头函数

以后的开发中经常使用

- function被箭头代替
- 如果方法只有return 直接省去花括号和ruturn
- 如果只有一个参数，参数小括号括号也省去

  //箭头函数 有点像lambda

 ```js
 var sum=(a,b)=>{

    return a + b

  }



  var sum1=(a,b)=>a+b;
 ```

第三种 把方法体内的函数简化

```js

    var arr=[1,2,3,4,5]
    var arr1=arr.map(function(obj){
        return obj*2
    })
    var arr2=arr.map((obj)=>obj*2)
console.log(arr1)
console.log(arr2)
```







## 对象初始化

- 如果对象的key：value 和外面的变量一样  ，则可以直接写上
- 如果value 为一个函数，则直接把  ：function 省略（类似java）

```js
//普通方法
        let info={
            title:"giaogiao",
            name:"你不是人",
            go:function(){
                console.log(`我是info`)
            }
        }

        //es6
        title="giaogiao"
        let info2={
            title,
            name:"你不是人",
            go(){
                console.log(`我是info`)
            }
        }
```

效果：

![image-20210706111613602](es6/image-20210706111613602.png)



## 对象结构

获取数据：

```js
//对象结构
         //es6
         title="giaogiao"
        let info2={
            title,
            name:"你不是人",
            go(){
                console.log(`我是info`)
            }
        }
//对象是以key：value 存在f
//获取方法 为 .  或者 []
console.log(info2.go())
console.log(info2[title])


//es6 快速获取对象结构
var{title,name}=info2
//原本代码：
// var title=info2.title
// var name=info2.name
console.log(title,name)
```



传播操作符：

对象创建另一个时，不需要的属性，则使用 此方法来解构过滤

   var {name,phone,...info2}=info;

```js
        let info ={
            name:"hehe",
            phone:123456,
            link:"http://www.baidu.com",
            hoby:"aaa",
            go(){
                console.log("gogogo")
            }
        }


    //结构出来
    var {name,phone,...info2}=info;

    console.log(info2)
```





## map和reduce的了解

map： 迭代器，自带for循环，并把循环的值回填相应的位置

var 数组2 = 数组.map(element=>element*2)





reduce： 数组.reduce  斐波那契数列





















