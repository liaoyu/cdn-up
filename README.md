# upyun_cdn
又拍云cdn上传

### 使用方法

upyun_cdn(options, auth, [callback])

options:
* `src` glob pattern
* `dest` upload path

auth:
* `bucket`
* `operator`
* `password`

callback: [可选]
* error
* result

### 示例
```js
upyun_cdn({
    src: 'build/**/*.js',
    dest: '/build',
    pathMap: {  // 上传路径与实际文件路径的映射
      '/Users/tmp/2017/2390392039.png': '/Users/name/test.png'
    }
}, {
    bucket: 'upyun-text',
    operator: 'test',
    password: 'test',
    domain: ''  // 该 bucket 对应的域名，可不填
}, function(err, result) {
    if (err) {
        console.error(err);
    }
});
```
