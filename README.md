# cdn-up
又拍云cdn上传

### 使用方法

upUpload(options, [callback])

options:
* `src` glob pattern
* `dest` upload path
* `bucket`
* `operator`
* `password`

callback: [可选]
* error
* result

### 示例
```js
upUpload({
    operator: 'test',
    password: 'test',
    bucket: 'upyun-text',
    domain: ''  // 该 bucket 对应的域名，可不填
    src: 'build/**/*.js',
    dest: '/build',
    pathMap: {  // 上传路径与实际文件路径的映射
      '/Users/tmp/2017/2390392039.png': '/Users/name/test.png'
    }
}, function(err, result) {
    if (err) {
        console.error(err);
    }
});
```
