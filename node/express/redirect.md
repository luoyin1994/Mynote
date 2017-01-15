# res.redirect重定向
app.post时，在如下情况，如果id ！== "undefined" 会报错.
问题出现再movie._id上。**可能是由于movie._id数据库中不存在**
```js
app.post('/admin/movie/new', function (req, res) {
    var movie    = req.body
    var id       = req.body._id
    var movieObj = movie
    var _movie
    if (id !== 'undefined') {
        Movie.findById(id, function (err, movie) {
            if (err) {
                console.log(err)
            }
            _movie = _.extend(movie, movieObj)
            _movie.save(function (err, movie) {
                if (err) {
                    console.log(err)
                }
                //这里不能重定向
                res.redirect('/movie/' + movie._id)//问题在movie._id上
                //需要注释掉上边的语句
                // res.redirect('/movie/' + movie._id)
            })
        })

    } else {
        _movie = new Movie({})
        _movie.save(function (err, movie) {
            if (err) {
                console.log(err)
            }
            //注释掉if中的重定向后这里可以重定向
            res.redirect('/movie/' + movie._id)
        })
    }
})
```

 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
