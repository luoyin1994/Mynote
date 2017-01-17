```html
<p id="p1" class="p1" style="color:#222">我是一个p元素</p>
```
```js
var p1 = document.getElementById('p1')
console.log(p1.id)//输出 p1
console.log(p1.style)//输出 CSSStyleDeclaration 只能访问到color的值
```
 
 
 
 
```js
   $(function () {
        var id = $('#p1').data('id')
        console.log(id)
        $("p").click(function (e) {
             var target = $(e.target)
            console.log(target.data('id'))
        });
    })
```
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
