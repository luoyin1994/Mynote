###obj.style和window.getComputedStyle(element,pseudoElement)
####相同：
两个返回的都是一个CSSStyleDeclaration对象
####不同：
#####1. obj.style只是获取元素的内联样式，也就是标签里嵌套的style样式，没有则为空。获取的CSSStyleDeclaration可读写
#####只能获取到height不能获取到background
```html   
<html style="height: 500px">
<style>
        html {
            height: 500px;
            background: red;
        }
</style>
<script>
    var h = document.getElementsByTagName('html')[0]
        console.log(h.style)
</script>
```
#####2. window.getComputedStyle获取全部的。仅可读不可写

CSSStyleDeclaration对象的有两部分
 1. 一部分是item(index) index 下标表示的属性名
 2. 一部分是属性名：属性值对象键值对
 
所以可以通过属性名访问，也可以通过下标访问属性名，同时支持属性getPropertyValue(propertyName)获得属性值。参考[The CSSStyleDeclaration Object](http://w3schools.bootcss.com/jsref/obj_cssstyledeclaration.html)


