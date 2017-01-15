#jade each循环的问题
###each引入的是一个对象
* 单值each会循环对象的val值
```jade
   - var elelment = {key1:val1,key2:val2,key3:val3}
   tr
    //- val 可以声明为任何的变量值
    each val in element
      th #{val} 
```
编译为
```html
  <tr>
    <th>val1</th>
    <th>val2</th>
    <th>val3</th>
  </tr>
```
* 双值each会循环对象的key，val值
```jade
   - var elelment = {key1:val1,key2:val2,key3:val3}
   tr
    //- key,val 可以声明为任何的变量值
    each val,key in element
      th #{key}:#{val} 
```
编译为
```html
  <tr>
    <th>key1:val1</th>
    <th>key2:val2</th>
    <th>key3:val3</th>
  </tr>
```
###each引入的是一个数组
* 单值each会循环数组的val值
```jade
   - var arr = [val1, val2, val3]
   tr
    //- val 可以声明为任何的变量值
    each val in arr
      th #{val} 
```
编译为
```html
  <tr>
    <th>val1</th>
    <th>val2</th>
    <th>val3</th>
  </tr>
```
* 双值each会循环数组的index，val值
```jade
   - var arr = [val1, val2, val3]
   tr
    //- index,val 可以声明为任何的变量值
    each val,index in arr
      th #{index}:#{val} 
```
编译为
```html
  <tr>
    <th>0:val1</th>
    <th>1:val2</th>
    <th>2:val3</th>
  </tr>
```
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
