# phantomjs_demos

### The first demo
001_hello_world.js
phantomjs 001_hello_world

### The second demo
002_loadpage.js 加载网页并截图
phantomjs 002_loadpage

### The third demo
003_load_speed.js 测试加载指定网页的速度
phantomjs 003_load_speed http://cuiqingcai.com

输出结果：
Loading http://cuiqingcai.com
Loading time 253968 msec

### The fourth demo
004_evaluate.js 输出网页源代码

```js
var url = 'http://www.baidu.com';
var page = require('webpage').create();
page.open(url, function(status) {
  var title = page.evaluate(function() {
    return document.title;
  });
  console.log('Page title is ' + title);
  phantom.exit();
});
```

输出结果：
Page title is 百度一下，你就知道