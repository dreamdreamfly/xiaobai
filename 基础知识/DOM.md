# 获取DOM元素的方法(获取到的是对象数据类型)
- document.getElementById([元素的id])：在整个文档中，根据元素的Id，获得一个元素对象   例如：document.getElementById('box')
  + document：是获取元素的上下文(获取元素的范围)，getElementById方法的上下文只能是document
  + 获取到的结构是一个对象(堆内存，里面存储着很多内置的属性和方法)
- document.getElementsByName([name属性值]):根据元素的name属性值，在整个文档中获取一组节点集合NodeList(类数组)
  + 在IE9及以下浏览器中只对表单起作用
- [context].getElementsByTagName([标签名])：在指定的上下文中，基于元素的标签名获取一组元素集合(类数组)
  + 获取的结果是HTMLCollection元素集合(类数组集合)
- [context].getElementsByClassName([样式类名])：在指定上下文中，基于样式类名获取对应的元素集合(类数组)
  + 不兼容IE低版本IE6-8
- document.documentElement:获取整个HTML元素对象(HTML是元素的根节点)
- document.body：获取整个BODY元素对象
- document.head：获取整个HEAD元素对象
- 不兼容IE6-8低版本浏览器，可以根据选择器(类似于css选择器)快速获取元素和元素集合的方法
  + [context].querySelector([SELECTOR])获取一个元素对象(不管匹配的结果是多少，都只获取第一个元素对象) 例如：document.querySelector("#box")
  + [context].querySelectorAll([SELECTOR])获取一组元素集合(类数组)
# DOM增删改
+ document.createElement([标签名])：动态创建一个DOM元素
+ [CONTAINER].appendclid([元素])：把元素动态插入到指定容器的末尾
+ [CONTAINER].insertBefore([新元素],[原始页面中已有的元素])：把创建的元素放到指定容器原始元素的前面(原始页面元素肯定在[CONTAINER]容器中)
+ [CONTAINER].remove([元素])：在指定容器中删除元素
+ document.createTextNode():创建一个文本节点
# 修改DOM元素样式
- 元素.style.xxx:修改(获取)当前元素的行内样式
  + 操作的都是行内样式，哪怕把样式写在样式表中，只要没有写在行内上，也获取不到
  + 元素.style.cssText = `color:red;font-size:12px`批量设置行内样式
- 元素.className：操作的是当前元素的样式类，基于样式类的管理给予不同的样式
  + box.className = 'actuve' 会把之前的样式类覆盖掉
  + box.className += ' active' 这样不会把之前的覆盖掉(记得加空格区分每个样式类)
  + box.classList.add('active')向指定样式集合中新增一个样式类(除了IE都兼容),box.classList.remove('active')删除，box.classList.toggle('active')有就删除没有就添加
# 设置元素的属性/自定义属性
  + 元素.xxx = xxx 操作的堆内存
  + 元素.setAttribute(xxx,xxx) 操作的DOM结构 获取方法：元素.getAttribute('xxx') 移除：元素.removeAttribute('xxx') 
  + 元素行间属性：data-属性名 = 'xxx' 获取：元素.dataset.属性名
  ```
  <div id='box' data-name = 'xx'>
  let box = document.querySelector('#box')
  console.log(box.dataset.name)
  ```
# 给DOM元素设置内容
- innerHTML/innerText:给非表单元素设置或者操作其内容
- value:操作表单元素的内容
# 获取DOM节点的属性和方法
> 我们认为在页面中所有呈现的内容，都是DOM文档中的一个节点(node),例如：元素节点、文本节点、注释节点、文档节点等

| 节点 | 内容 | nodeType | nodeName | nodevalue |
| :--: | :--: | :--: | :--: | :--: |
| 元素节点 |元素标签| 1 | "大写标签名" | null |
| 文本节点 |文字或者标签之间的空格和换行| 3 | "#text" | 文本内容 |
| 注释节点 |注释内容| 8 | "#comment" | 注释内容 |
| 文档节点 |整个页面是一个大的文档节点| 9 | "#document" | null |
# 描述节点和节点之间的属性(获取的节点如果没有就是null)
- [CONTAINER].childNodes:获取当前容器中所有子节点
- [CONTAINER].children:获取当前容器中所有的元素子节点(只有元素节点，在IE低版本浏览器中，会把注释节点当作元素节点，而且不认为空格和换行是节点)
- [NODE].parentNode:获取某一个节点的父节点
- [NODE].previousSibling:获取某一个节点的哥哥节点
- [NODE].previousElementSibling:获取某一个节点的哥哥元素节点(不支持IE低版本)
- [NODE].nextSibling:获取某一个节点的弟弟节点
- [NODE].nextElementSibling:获取某一个节点的弟弟元素节点(不支持IE低版本)
- [CONTAINER].firstClid:获取当前容器的第一个子节点
- [CONTAINER].firstElementClid:获取当前容器的第一个元素子节点(不支持IE低版本)
- [CONTAINER].lastClid:获取当前容器的最后一个子节点
- [CONTAINER].lastElementClid:获取当前容器的最后一个元素子节点(不支持IE低版本)