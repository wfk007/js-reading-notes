# Javascript 高级程序设计 dom部分

1. Node

  - childNodes属性，保存一个NodeList对象（有生命有呼吸的对象，类数组对象，并不是Array的实例）

    parentNode属性，指向文档树中的父节点。

  - previousSibling nextSlibling firstChild lastChild

  - appendChild() insertBefore() replaceChild() removeChild()

  - clone() true=>深克隆，复制节点和整个节点数。false=>浅克隆，只复制节点。深浅克隆都不会克隆js属性，只复制特性。

2. Document (nodeType = 9)

  - document.documentElement // =>取得对<html>的引用

    document.body // =>取得对<body>的引用

  - document.URL //=>取得完整的URL

    document.domain //=>取得域名

    document.referrer //=>取得来源页面的URL

  - getElementById() // =>只返回文档中第一次出现的元素

    getElementsByTagName() //=>返回一个 HTMLCollection 对象 namedItem()

    getElementsByName() // =>返回一个 HTMLCollection 对象,最常用在获取单选框.

3. Element (nodeType = 1)

  - getAttribute() setAttribute() removeAttribute()

    属性的值和通过getAttribute()返回的值不同:style和onclick这样的事件处理函数.一般使用对象属性,而不使用getAttribute()

  - setAttribute() removeAttribute()

  - document.createElement() //=>创建元素

4. Text(nodeType = 3)

5. Comment(nodeType = 8)

