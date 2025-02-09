# AJAX基础

## AJAX概念

* 使用浏览器的 XMLHttpRequest对象 与服务器通信

* 浏览器网页中，使用 AJAX技术（XHR对象）发起获取省份列表数据的请求，服务器代码响应准备好的省份列表数据给前端，前端拿到数据数组以后，展示到网页（让数据变活）

* 这里使用一个第三方库叫 axios, 后续再学习 XMLHttpRequest 对象了解 AJAX 底层原理

* 因为 axios 库语法简单，让我们有更多精力关注在与服务器通信上，而且后续 Vue，React 学习中，也使用 axios 库与服务器通信

### 示例程序

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AJAX概念和axios使用</title>
</head>

<body>
  <!--
    axios库地址：https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js
    省份数据地址：http://hmajax.itheima.net/api/province

    目标: 使用axios库, 获取省份列表数据, 展示到页面上
    1. 引入axios库
  -->
  <p class="my-p"></p>
  <script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>
  <script>
    // 2. 使用axios函数
    axios({
      url: 'http://hmajax.itheima.net/api/province'
    }).then(result => {
      console.log(result)
      // 好习惯：多打印，确认属性名
      console.log(result.data.list)
      console.log(result.data.list.join('<br>'))
      // 把准备好省份列表，插入到页面
      document.querySelector('.my-p').innerHTML = result.data.list.join('<br>') 
    })
  </script>
</body>

</html>
```

