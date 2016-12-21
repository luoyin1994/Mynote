### 百分比宽度
- html默认高度为0,但是html背景却可以满屏（此时的背景色是浏览器的背景色）
- 如果html没有设置background-color的话body不设置高度都会全屏显示背景色（此时的背景色是浏览器的背景色），但是没有高度
- 如果html设置背景色，body也仅仅只设定了背景色的话body的背景色会被html覆盖
- 此时body设置了百分比高度没有任何作用，因为html没有设置高度
- 只有当html设置高度后才可以有显示
- 宽高百分比是参考元素父元素的宽高计算，如果元素要使用百分数 其父元素宽高必须设置 auto和不设置是不起作用的。参考张鑫旭[对html与body的一些研究与理解](http://www.zhangxinxu.com/wordpress/2009/09/%E5%AF%B9html%E4%B8%8Ebody%E7%9A%84%E4%B8%80%E4%BA%9B%E7%A0%94%E7%A9%B6%E4%B8%8E%E7%90%86%E8%A7%A3/)

##### 以下代码会渲染为全屏red，body#ccc会被覆盖
```css
        html {
            background: red;
        }

        body {
            background: #cccccc;
        }
```
##### 以下代码无变化
```css
        html {
            background: red;
        }
        
        html {
            height: 100%;
            width:100%;
            background: red;
        }
```
html可以设置百分比，他的百分比参考对象是谁？？？
