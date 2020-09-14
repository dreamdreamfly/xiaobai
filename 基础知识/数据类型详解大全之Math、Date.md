# Math数学函数中常用的方法
- Math是一个对象数据类型，在他的堆内存中，存储了很多的内置属性和方法，这些方法一般都是用来操作数字的，所有我们把Math称为'数学函数对象'
- Math.PI/Math['PI'] 圆周率 3.141592653589793
- Math.abs([Number]) 绝对值
- Math.ceil([Number])/Math.floor([Number]) 把数字N向上或者向下取整数
- Math.round([Number]) 四舍五入(结果是整数)
- Math.max(N1,N2,N3...)/Math.min(N1,N2...)  获取最大值/最小值
- Math.pow([N],[m]) 获取数字N的m次幂
- Math.sqrt([N]) 给数字N开平方
- Math.random() 随机获取0-1之间的小数 
  + 获取到的随机数的特点：基本上不会重复(Math.random经常应用于'随机'和'不重复')
  + 随机获取n到m之间的整数(包含n和m)
  ```
  Math.round((Math.random()*(m-n) + n)
  ```
# Date
- 计算机当前的时间(本地的)是不安全的，服务器时间是安全的
- new Date(传入时间戳/或者不传) 获取到的是对应/当前时间
```
new Date()
'Mon Sep 14 2020 16:40:20 GMT+0800 (中国标准时间)'
```
- 方法
  + new Date()/+ new Date().getFullYear()获取年 **数字类型的**
  + .getMonth()+1获取月份，记得+1//从零开始的记得加1
  + .getDate()获取日
  + .getDay()获取周几 周日为0 排序‘周日','周一','周二','周三','周四','周五','周六‘
  + .getHours()获取时
  + .getMinutes()获取分
  + .getSeconds()获取秒
- 时间戳（以毫秒为单位，一秒等于1000毫秒）
  + 概念：1970年到现在的时间(时间戳是指格林威治时间1970年01月01日00时00分00秒(北京时间1970年01月01日08时00分00秒)起至现在的总秒数。)
  + 获取时间戳的方法： 
    - console.log(Date.now())
    - console.log(+ new Date)
    - console.log(+ new Date())
