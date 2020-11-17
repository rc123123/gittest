#es6
###let关键字：
    1.当前作用域不允许重复声明两个相同的变量
    2.let声明的变量具有块级作用域(对象不属于块级作用域)
    3.let声明的变量具有暂时性死区（绑定到当前作用域上） 
    4.let声明的变量不具有变量提升
###const关键字：
    1.const定义的变量必须赋初始值
    2.const也具有块级作用域
    3.const定义的变量属于常量（不可变的量）。内存地址不可改变，可以更改地址里面的内容--对象
###数组的解构赋值：概念：按照一一对应的关系把数组中的内容赋值给变量。
    1.let [a, b, c] = [1, 2, 3]//a=1 b=2 c=3;
    2.let [a, b, c,d] = [1, 2, 3]//a=1 b=2 c=3 d=undefined;
    3.let [a, [b], c] = [1, [2], 3]//a=1 b=2 c=3
    4.let [a, , c] = [1, 2, 3]//a=1 c=3;
    4.let [a, b = 5, c] = [1, , 3]//a=1 b=5(如果有对应的值默认值无效) c=3;
###对象的解构赋值： 属性名相等则解构成功。
    1.  let { age, name } = { name: 'zs', age: 10, sex: 'nan' };//age=10 name=zs
    2.  let { age: myAge, name } = { name: 'zs', age: 10, sex: 'nan' };//myAge=10;
    3.  let { age: myAge, name1 } = { name: 'zs', age: 10, sex: 'nan' };//age=10  name1=undefined
###箭头函数：
    function(){}-------去掉function 中间=>连接
        let fn = () => {
            console.log(123)
        }
        fn()
    1.变体：如果参数只有一个可以省略括号
        let fn = x=>{console.log(x)}
    2.变体：如果只有一个表达式 可以省略{}
        let fn = x=>console.log(x)
+   箭头函数的this指向问题：
        1.箭头函数中的this指向的是父级作用域。
        2.箭头函数中的this定义时已经确定。通过call  apply  bind无法更改.
        3.箭头函数没有arguments.
        4.使用new关键字是无效
        5.箭头函数是没有原型对象
###扩展运算符   ...

###Set数据结构---对象  类似于数组
     let s1 = new Set([1, 2, 3, 1, 2, 3]) 只能存储唯一的值 
    相关方法：  
    添加值：
        s1.add(4) 
    删除值：
        s1.delete(4)
    清空值：
         s1.clear()
    判断值：
        s1.has(值) 有值返回true否则返回false
    循环值:
    s1.forEach((item)=>{
        console.log(item)
    })    
###es6新增方法：
    from：数组转化 对象
    let obj = {
        '0': 1,
        "1": 2,
        "length": 2
    }
    console.log(Array.from(obj))
    
    find:查找元素：
    arr.find(item=>{
        return item==1
    })
    findIndex：查找元素索引
      arr.findIndex(item=>{
        return item==1
    })
    数组是否包含某一项：
    arr.includes(2)
###模板字符串：
    1.let str = `${值}`
    特性：
        1.${可以存放变量}
        2.${可以存放字符串}
        3.${函数名}
        4.${三元表达式}
