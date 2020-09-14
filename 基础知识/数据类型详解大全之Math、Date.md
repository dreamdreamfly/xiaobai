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
