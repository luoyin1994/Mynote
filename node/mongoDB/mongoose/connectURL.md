# mongoose.connect
windows下连接方式
连接前需要开启数据库
```
   mongod --dbpath [db path] #可以是./data/db 
```
本地访问127.0.0.1=localhost
```js
    // /imooc是db库名
    mongoose.connect('localhost:27017/imooc')
    mongoose.connect('127.0.0.1:27017/imooc')
```
也可以用下边的方式
```js
    mongoose.connect('mongodb://localhost:27017/imooc')
    mongoose.connect('mongodb://127.0.0.1:27017/imooc')
```
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
