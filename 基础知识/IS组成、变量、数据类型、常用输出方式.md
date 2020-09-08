# JS作用和组成
- 作用：完成人机交互效果
   + 基本的人机交互效果
   + 页面中具体小狗的实现
   + 页面中动态数据的获取和绑定(JS是用来操作DOM和操作浏览器的)
   + 可能会操作浏览器的一些功能
- 组成：
   + ECMAScript(ES3/ES6-9):定义了JS的语法规范
   + DOM(document object model)文档对象模型，提供对应的属性和方法，可以让JS操作页面中的DOM元素。定义了语言本身的变量、数据值、操作语句、内存管理...等
   + BOM(browser object model)浏览器对象模型，通过操作浏览器的属性和方法
> 注意：当代项目开发，一般都是基于Vue/React完成的，基于这两个框架，我们已经不需要操作DOM了，我们操作数据，由框架本身帮助我们完成DOM操作
# JS中的变量(variable)
+ 定义：可变的量(其存储的值是可变的)，设置一个变量(七个名字)，让其代表和指向某一个具体的值
+ 创建变量的方式
   + var
   + let、const(常量)(**ES6**)
   + function 创建函数
   + class 创建一个类
   + import/require 基于ES6Module或者Common.js规范导入模块
   ```
   import axios from './axios'
   let axios = require('./axios')
   ```
+ 变量命名的规范
   + 严格区分大小写
   + 使用驼峰命名法：由有意义英文组成一个名字，第一个单词首字母小写，其余每一个有意义的单词首字母大写
   + 命名规则：
      + 使用"_、$、英文字母、数字"命名
      + 数字不能作为开头
      + 不能使用关键字和保留字
      > + 关键字：在JS中有特殊含义的
      > + 保留字：未来可能会成为关键字的
# JS数据类型
+ 基本数据类型
   + 数字数据类型 Number  NaN infinity(无穷大) -infinity(负无穷大)
   + 布尔值 Boolean
   + 字符串 String **ES6**新增模版字符串``
   + null(空指针对象) (null和undefined有且只和自己本身相等)
   + undefined(未定义)
   + Symbol(唯一值 **ES6**) Symbol('坚持') == Symbol('坚持') => false
+ 引用数据类型
   + 对象数据类型
      + 普通对象 {}
      + 数组对象 []
      + 正则对象 /^$/ RegExp
      + 日期对象 new Date 
      + 数学函数对象 Match
   + 函数数据类型 箭头函数(**ES6**)
# JS中常用的输出方式
- console 控制在浏览器控制台输出
   + console.log()控制台输出日志，特点：输出任意数据类型的数据，控制台展示的也是对应的数据类型，可以一次输出多个值
   + console.dir()控制台详细输出，特点：输出一个对象或者一个值的详细信息，dir只能输出一个值
   + console.table()把数据以表格的形式输出在控制台，把多维的JSON数据以表格形式输出
   + console.time('1')/console.timeEnd('1')计算某个程序消耗的时间，计算出time/timeEnd中间所有程序执行所消耗的时间(预估时间，受当前电脑性能的影响)
- window提示框(输出的结果都是字符串)
   + alert()提示框 需要等到alert弹出框，点击确认关闭后，后面的代码才会继续执行(alert会阻止主线程的渲染),返回值是undefined
   + confirm()确认取消提示框 confirm相对于alert来说给用户提供了确认和取消两种选择，返回值：true点击的是确认，false点击的是取消
   + prompt()在confirm的基础上给用户提供书写操作的原因等信息，返回值：点击取消是null，点击的确认是返回用户输入的原因
- 向页面指定容器中插入内容(输出的结果是字符串)
   + document.write 向页面中输入内容，把内容写入到页面中
   + innerHTML/innerText向页面指定容器中输入内容，会把之前的内容覆盖掉，想要追加得采用+=的方式。innerHTML把标签文本进行识别和渲染，innerText会把所有的内容都当作普通的文本
   + value向页面表单元素中输入内容
>JS中注释
> + 块级注释：Shfit + Alt + A
> + 行级注释：Ctrl + /