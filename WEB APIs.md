# WEB APIs

> 之前学习的JavaScript基础大部分属于ECMAScript（ES）的知识体系
>
> ECMAScript是一套语言标准规范，如变量、数据类型、表达式、语句、函数等语法规则都是由ECMAScript规定的。
>
> 而接下来学习的Web APIs是浏览器扩展的功能，ECMAScript运行在浏览器中然后再结合Web APIs才是真正的JavaScript。
>
> **Web APIs 的核心是 DOM 和 BOM**
>
> DOM，文档对象模型，定义了一套操作HTML文档的API。
>
> BOM，浏览器对象模型，定义了一套操作浏览器窗口的API。
>
> ECMAScript早期的版本号采用数字顺序编号如ECMAScript3、ECMAScript5，后来由于更新速度较快便采用年份做为版本号，如 ECMAScript2017，ECMAScript2018这种格式，ECMAScript6是 2015 年发布的，常叫叫做EMCAScript2015。

![guide](C:\Users\Lenovo\Desktop\未同步\Notes\assets_WEB APIs\guide.png)

## 补充内容

### JS的书写习惯

CSS里面每一句代码后面都是有分号的，而HTML和JS是没有的。

### 变量声明

变量声明有三个关键字：var，let，const。

首先var先排除，老派写法，问题很多，可以淘汰掉。

**在实际开发中我们尽量使用const。**

原因：const 语义化更好， 实际开发中也是，比如react框架，基本都用const。

实际应用：有了变量先给const，如果发现它后面是要被修改的，再改为let。

### const关键字

 const声明的值不能更改，而且const声明变量的时候需要里面进行初始化。

但是对于引用数据类型，const声明的变量，里面存的不是值，而是地址。

因此建议数组和对象使用 const 来声明。（对象也是引用类型）

## DOM

DOM（Document Object Model——文档对象模型）是用来呈现以及与任意 HTML 或 XML 文档交互的API。

是浏览器提供的一套专门用来操作网页内容的一组功能，用来动态修改 HTML 。

![demo](C:\Users\Lenovo\Desktop\未同步\Notes\assets_WEB APIs\demo.gif)

### DOM树

将 HTML 文档以树状结构直观的表现出来，我们称之为文档树或 DOM 树。

**文档树直观的体现了标签与标签之间的关系。**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>标题</title>
</head>
<body>
  文本
  <a href="">链接名</a>
  <div id="" class="">文本</div>
</body>
</html>
```

![web-api](C:\Users\Lenovo\Desktop\未同步\Notes\assets_WEB APIs\web-api.jpg)

### DOM节点

节点是文档树的组成部分，**每一个节点都是一个 DOM 对象**，主要分为元素节点、属性节点、文本节点等。

1. 【元素节点】其实就是 HTML 标签，如上图中 `head`、`div`、`body` 等都属于元素节点。
2. 【属性节点】是指 HTML 标签中的属性，如上图中 `a` 标签的 `href` 属性、`div` 标签的 `class` 属性。
3. 【文本节点】是指 HTML 标签的文字内容，如 `title` 标签中的文字。
4. 【根节点】特指 `html` 标签。

### DOM对象

浏览器根据html标签生成的JS对象。**（在HTML中称标签，在JS里称为对象）**

所有的标签属性都可以在这个对象上面找到。

修改这个对象的属性会自动映射到标签身上。

DOM的核心思想就是把网页内容当作对象处理。

**Document是JavaScript内置的专门用于DOM的对象，网页所有内容都在document里面，它提供的属性和方法都是用来访问和操作网页内容的，例：document.write()。**

Document是学习 DOM 的核心。

### 获取DOM对象

> 我们想要操作某个标签首先做什么？肯定首先选中这个标签，跟 CSS选择器类似，选中标签才能操作。
>
> JS中的选择器和CSS中的选择器有相似之处。
>
> CSS中的类选择器（例：.box）对应标签里的class属性，CSS中的id选择器（例：#box）对应标签里面的id属性。
>
> JS中的getElementById对应标签里的id属性，JS中的getElementsByClassName对应标签里的class属性。
>
> name这个属性值在表单标签中曾经使用过，例如用于单选框的分组。
>
> id属性和name属性都是JS里常用的属性，class是在CSS里常用的属性。

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DOM - 查找节点</title>
</head>
<body>
  <h3>查找元素类型节点</h3>
  <p>从整个 DOM 树中查找 DOM 节点是学习 DOM 的第一个步骤。</p>
  <ul>
      <li>元素1</li>
      <li>元素2</li>
      <li>元素3</li>
      <li>元素4</li>
  </ul>
  <div>我是老爹
        <span>我是家里老大</span>
        <span>我是家里老二</span>
        <span>我是家里老四</span>
  </div>
  <button name="老大">我是老大</button>
  <button name="小弟">我是小弟</button>
  <button class="Fuli" id="Fuli">点击我，给你送水果啦！</button>
</body>
    <script>
    /*1.querySelector，通过CSS选择器（标签选择器，类选择器，id选择器，后代选择器等）选择匹配的第一个元素*/
    /*返回值：CSS选择器匹配的第一个元素,一个HTMLElement对象，我们可以直接修改它的值，如果没有匹配到，则返回null*/
    /*参数：包含一个或多个有效的CSS选择器(要加引号！！！)*/
    const botton1 = document.querySelector('button');
    const li1 = document.querySelector('ul li:first-child');
    console.log(botton1);
    console.log(li1);
    
    /*2.querySelectorAll  通过CSS选择器（标签选择器，类选择器，id选择器，后代选择器等）选择满足条件的元素集合*/
    /*返回值：CSS选择器匹配的NodeList对象集合，得到的是一个伪数组（有长度有索引号，但是没有pop()，push()等数组方法，想要得到里面的每一个对象，则需要遍历（for）的方式获得），我们无法直接对返回值进行修改，只能通过遍历的方式来实现*/
    /*哪怕只有一个元素，通过querySelectAll() 获取过来的也是一个伪数组，里面只有一个元素而已*/
    /*参数：包含一个或多个有效的CSS选择器(要加引号！！！)*/
  	const lis = document.querySelectorAll('ul li');  // 获取所有的li标签
    console.log(lis);
        
    /*3.getElementsByClassName  根据标签的class属性(类选择器)查找（了解）*/
    /*参数：class属性里面的内容，是一个字符串，前面没有点号，因为这不是个CSS选择器，切记！*/
    const button2 = document.getElementsByClassName('Fuli');
    console.log(button2);
    
    /*4.getElementById  根据标签的ID属性（ID选择器）查找（了解）*/
    /*参数：id属性里面的内容，是一个字符串，前面没有井号，因为这不是个CSS选择器，切记！*/
    const button3 = document.getElementById('Fuli');
    console.log(button3);
    
    /*5.getElementsByTagName  通过标签选择器进行选择，获取满足条件的第一个元素（了解）*/
    const p = document.getElementsByTagName('p');
    console.log(p);
  </script>
</html>
```

### 操作元素内容

**如果文本内容中包含 `html` 标签时推荐使用 `innerHTML`，否则建议使用 `innerText` 属性。**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>操作元素内容</title>
</head>
<body>
    <div class="box1">盒子1</div>
    <div class="box2">盒子2</div>
    <div class="box3">盒子3</div>
    <div class="box4">盒子4</div>
</body>
    <script>
        // innerText，文本中包含的标签不会被解析
        const box1 = document.querySelector('.box1')
        box1.innerText = '嗨~ 我叫李雷！'
        console.log(box1.innerText)
        const box2 = document.querySelector('.box2')
        box2.innerText = '<h4>嗨~ 我叫李雷</h4>'
        console.log(box2.innerText)
        // innerHTML，文本中包含的标签会被解析
        const box3 = document.querySelector('.box3')
        box3.innerHTML = '嗨~ 我叫韩梅梅！'
        console.log(box3.innerHTML)
        const box4 = document.querySelector('.box4')
        box4.innerHTML = '<h4>嗨~ 我叫韩梅梅！</h4>'
        console.log(box4.innerHTML)
    </script>
</html>
```

### 常用属性修改

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>常用属性修改</title>
</head>
<body>
    <img src="#" alt="照片加载失败" width="200" height="200" class="pic">
</body>
    <script>
        const pic = document.querySelector('.pic')
        pic.width = '100'
        pic.height = '100'  
        //都要打引号，很容易错，这里的width和height是标签内的属性，没有单位px一说
        pic.alt = '照片不存在'
        /*pic.src = 'https://www.baidu.com/img/flexible/logo/pc/result.png'*/
        console.log(pic.src)
    </script>
</html>
```

### 控制样式修改

#### 通过style属性修改

适用于修改样式较少的情况

**如要遇到 `css` 属性中包含字符 `-` 时，要应用驼峰法**

**如 `background-color` 要写成 `box.style.backgroundColor`**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>控制样式修改1</title>
</head>
<body>
    <div class="box">随便一些文本内容</div>
</body>
    <script>
        //因为我们修改的是样式属性，一定别忘记，大部分数字后面都需要加单位
        const box = document.querySelector('.box')
        //如选择的标签具有唯一性，那可以跳过选择这步，直接进行修改，例如，修改body样式属性的话，直接写document.body.style.属性名 = ‘’即可
        box.style.width = '200px'
        box.style.height = '200px'
        box.style.backgroundColor = 'red'
        box.style.color = 'white'
        box.style.fontSize = '20px'
        box.style.textAlign = 'center'
        box.style.lineHeight = '200px'
        box.style.borderRadius = '50%'
    </script>
</html>
```

#### 通过类名（className）修改

如果修改的样式很多，那么上面的方法就很繁琐，所以我们通过类名进行修改

类似于先写好一个模板，在把这个模板覆盖到节点上的思想

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>控制样式修改2</title>
    <style>
        .red {
            width: 200px;
            height: 200px;
            background-color: red;
            color: white;
            font-size: 20px;
            text-align: center;
            line-height: 200px;
            border-radius: 50%;
        }
        .blue {
            width: 200px;
            height: 200px;
            background-color: blue;
            color: white;
            font-size: 20px;
            text-align: center;
            line-height: 200px;
            border-radius: 50%;
        }
    </style>
</head>
<body>
    <div class="red"></div>
</body>
    <script>
        const box = document.querySelector('.red')
        box.addEventListener('click',function() {
            box.className = 'blue'
            //由于class是关键字, 所以使用className去代替
            //className是使用新值换旧值, 如果需要添加一个类,需要保留之前的类名
            /*box.setAttribute('class','blue')*/
        })
    </script>
</html>
```

#### 通过classList操作类修改（最常用）

为了解决className容易覆盖以前的类名的问题，可以用classList方式追加或者删除类名

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>控制样式修改3</title>
    <style>
        .box {
            width: 200px;
            height: 200px;
            background-color: blue;
        }

        .active {
            width: 300px;
            height: 300px;
            background-color: red;
            margin-left: 100px;
        }
    </style>
</head>
<body>
    <div class="box">我是一个测试盒子</div>
</body>
    <script>
        /*1.获取元素*/
        let box = document.querySelector('div') 
        
        /*2.操作元素*/
        box.classList.add('active')//add方法：添加追加类。类名不加点号，而且是字符串。
        box.classList.remove('box')//remove方法：类移除。类名不加点号，而且是字符串。
        box.classList.toggle('box')//toggle方法：切换。有就删掉，没有就加上，类似于开关选项
    </script>
</html>
```

### 操作表单元素属性

应用场景：文本框和密码框的转换，小眼睛点击之后可以查看密码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <input type="text" value="请输入">
    <button disabled>按钮</button>
    <input type="checkbox" name="" id="" class="agree">
    <script>
        // 1. 获取元素
        let input = document.querySelector('input')
        // 2. 取值或者设置值  得到input里面的值可以用 value
        // console.log(input.value)
        input.value = '小米手机'
        input.type = 'password'

        // 2. 启用按钮
        let btn = document.querySelector('button')
        // disabled 不可用，不写属性值默认为True  赋值成新值False  这样可以让按钮启用
        btn.disabled = false
        // 3. 勾选复选框
        let checkbox = document.querySelector('.agree')
        checkbox.checked = false
    </script>
</body>

</html>
```

### 自定义属性

标准属性：标签天生自带的属性比如class、id、title等，直接用语法操作的属性比如disabled、checked、selected等。

在html5中推出来了专门的data-自定义属性 ，在标签上一律以data-开头。

**在DOM对象上一律以dataset对象方式获取。**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
   <div data-id="1"> 自定义属性 </div>
    <script>
        // 1. 获取元素
        let div = document.querySelector('div')
        // 2. 获取自定义属性值
         console.log(div.dataset.id)
      
    </script>
</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 表示这棵树可以开花 -->
    <button id="btn" isFlower="yes" >我是一棵树</button>
</body>
<script>
    var tree = document.getElementById('btn');
    // console.log(tree);
    var flag = tree.getAttribute('isFlower');
    console.log(flag);
</script>
</html>
```

## 间歇函数

`setInterval` 是 JavaScript 中内置的函数。

它的作用是间隔固定的时间自动重复执行另一个函数，也叫定时器函数。

```html
<script>
  // 1. 定义一个普通函数
  function repeat() {
    console.log('不知疲倦的执行下去....')
  }

  // 2. 使用 setInterval 调用 repeat 函数
  // 间隔 1000 毫秒，重复调用 repeat
  setInterval(repeat, 1000)
</script>
```

## 事件

事件是编程语言中的术语，它是用来描述程序的行为或状态的，**一旦行为或状态发生改变，便立即调用一个函数。**

所谓的事件无非就是找个机会（事件触发）调用一个函数（回调函数）。

### 事件监听

`addEventListener` 是 DOM 对象专门用来添加事件监听的方法

它的两个参数分别为【事件类型】和【事件回调】。

【事件类型】决定了事件被触发的方式，如 `click` 代表鼠标单击，`dblclick` 代表鼠标双击。

【事件处理程序】决定了事件触发后应该执行的逻辑。

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>事件监听</title>
</head>
<body>
  <h3>事件监听</h3>
  <p id="text">为 DOM 元素添加事件监听，等待事件发生，便立即执行一个函数。</p>
  <button id="btn">点击改变文字颜色</button>
  <script>
    // 1. 获取 button 对应的 DOM 对象
    const btn = document.querySelector('#btn')

    // 2. 添加事件监听
    btn.addEventListener('click', function () {
      //这里不用加on,直接在js加监听事件就不用加on
      console.log('等待事件被触发...')
      // 改变 p 标签的文字颜色
      let text = document.getElementById('text')
      text.style.color = 'red'
    })

    // 3. 只要用户点击了按钮，事件便触发了！！！
  </script>
</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- <button id="btn" onclick=alert(1) >我是一个按钮</button> -->
    <button id="btn"  >我是一个按钮</button>
    <button id="btn" onclick=handleFn() >我是一个按钮</button>
</body>
<script>
    // document.getElementById('btn').onclick = function() {
    //     alert(1);
    // };
     function handleFn() {
         alert(1);
     }
</script>
</html>
```

### 事件类型

#### 鼠标事件

```html
<body>
  <h3>鼠标事件</h3>
  <p>监听与鼠标相关的操作</p>
  <hr>
  <div class="box"></div>
  <script>
    // 需要事件监听的 DOM 元素
    const box = document.querySelector('.box');

    // 监听鼠标是移入当前 DOM 元素
    box.addEventListener('mouseenter', function () {
      // 修改文本内容
      this.innerText = '鼠标移入了...';
      // 修改光标的风格
      this.style.cursor = 'move';
    })
  </script>
</body>

<body>
  <h3>鼠标事件</h3>
  <p>监听与鼠标相关的操作</p>
  <hr>
  <div class="box"></div>
  <script>
    // 需要事件监听的 DOM 元素
    const box = document.querySelector('.box');

    // 监听鼠标是移出当前 DOM 元素
    box.addEventListener('mouseleave', function () {
      // 修改文本内容
      this.innerText = '鼠标移出了...';
    })
  </script>
</body>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 鼠标双击时触发 -->
    <!-- <button ondblclick=alert(1)></button>  -->
    <!-- 鼠标按下时触发 -->
    <!-- <button onmousedown=alert(1)></button> -->
    <!-- 鼠标释放时触发 -->
    <!-- <button onmouseup=alert(1)></button> -->
    <!-- 鼠标在元素移动触发 -->
    <!-- <div onmousemove=console.log(1)>测试盒子</div> -->
    <!-- 鼠标进入元素触发 -->
    <!-- <div onmouseenter=console.log(1)>测试盒子</div> -->
    <!-- 鼠标离开元素触发 -->
    <!-- <div onmouseleave=console.log(1)>测试盒子</div> -->

</body>
<style>
    div {
        background-color: blue;
    }
</style>
</html>
```

鼠标经过事件：

mouseover 和 mouseout 会有冒泡效果

mouseenter  和 mouseleave   没有冒泡效果 (推荐)

#### 键盘事件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 键盘按下触发 -->
    <div keydown=console.log(1)>测试盒子</div>
    <!-- 键盘释放触发 -->
    <div keyup=console.log(1)>测试盒子</div>
    
</body>
</html>
```

#### 焦点事件/表单事件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 聚焦事件 -->
    <!-- <input type="text" id="myInput" /> -->
    <!-- 失去焦点 -->
    <input type="text" id="myInput" />
    <!-- 改变事件 -->
     <!-- <input type="text" id="myInput" /> -->
    <script>
    document.getElementById('myInput').addEventListener('blur', function() {
        console.log("你失去了焦点");
      });
    </script>
</body>
</html>
```

#### 文本框输入事件

```

```

#### 其他事件

```html
<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>滚动监听示例</title>
    <style>
        body {
            height: 2000px; /* 让页面可以滚动 (必须给body加一高度)*/
            margin: 0;
        }
    </style>
</head>
<body>
    <script>
    //     window.addEventListener('resize', function() {
    //         console.log("窗口尺寸改变");
	//	   });   
    //     window.addEventListener('scroll', function() {
    //         console.log("视图在滑动");
    //     });
           /*加载外部资源（如图片、外联CSS和JavaScript等）加载完毕时触发的事件，有些时候需要等页面资源全部处理完了做一些事情*/
    //     window.addEventListener('load', function() {
    //         console.log("视图加载完毕");
    //     });
    //     window.addEventListener('unload', function() {
    //         console.log("视图加载完毕");
    //     });
    //     //页面关闭时加载
    	   window.addEventListener('beforeunload', function(event) {
    // 标准方式：弹出提示框
           		const message = "确定要离开此页面吗？";
    // 这行代码是为了确保大多数浏览器能够显示默认的警告框
           		event.returnValue = message; 
               //event.returnValue：这是现代浏览器推荐的方式。
    // 将它设置为字符串时，浏览器会显示一个默认的提示框（并且有可能让用户确认是否要离开页面）。
    // 这行是为了兼容某些老浏览器或自定义提示内容
        		return message;
			});
    </script>
</body>
</html>
```

#### event事件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id="box">测试盒子</div>
</body>
<script>
    // 设置一个点击事件对象，用event接收
    document.getElementById('box').addEventListener('click',function(event) {
        console.log(event);
    })
</script>
</html>
```

### 事件对象

任意事件类型被触发时与事件相关的信息会被以对象的形式记录下来，我们称这个对象为事件对象。

```html
<body>
  <h3>事件对象</h3>
  <p>任意事件类型被触发时与事件相关的信息会被以对象的形式记录下来，我们称这个对象为事件对象。</p>
  <hr>
  <div class="box"></div>
  <script>
    // 获取 .box 元素
    const box = document.querySelector('.box')

    // 添加事件监听
    box.addEventListener('click', function (e) {
      console.log('任意事件类型被触发后，相关信息会以对象形式被记录下来...');

      // 事件回调函数的第1个参数即所谓的事件对象
      console.log(e)
    })
  </script>
</body>
```

事件回调函数的【第1个参数】即所谓的事件对象，通常习惯性的将这个对数命名为 `event`、`ev` 、`ev` 。

接下来简单看一下事件对象中包含了哪些有用的信息：

1. `ev.type` 当前事件的类型
2. `ev.clientX/Y` 光标相对浏览器窗口的位置
3. `ev.offsetX/Y` 光标相于当前 DOM 元素的位置

注：在事件回调函数内部通过 window.event 同样可以获取事件对象。

### 环境对象

> 能够分析判断函数运行在不同环境中 this 所指代的对象。

环境对象指的是函数内部特殊的变量 `this` ，它代表着当前函数运行时所处的环境。

```html
<script>
  // 声明函数
  function sayHi() {
    // this 是一个变量
    console.log(this);
  }

  // 声明一个对象
  let user = {
    name: '张三',
    sayHi: sayHi // 此处把 sayHi 函数，赋值给 sayHi 属性
  }
  
  let person = {
    name: '李四',
    sayHi: sayHi
  }

  // 直接调用
  sayHi() // window
  window.sayHi() // window

  // 做为对象方法调用
  user.sayHi()// user
	person.sayHi()// person
</script>
```

结论：

1. `this` 本质上是一个变量，数据类型为对象
2. 函数的调用方式不同 `this` 变量的值也不同
3. 【谁调用 `this` 就是谁】是判断 `this` 值的粗略规则
4. 函数直接调用时实际上 `window.sayHi()` 所以 `this` 的值为 `window`

### 回调函数

如果将函数 A 做为参数传递给函数 B 时，我们称函数 A 为回调函数。

```html
<script>
  // 声明 foo 函数
  function foo(arg) {
    console.log(arg);
  }

  // 普通的值做为参数
  foo(10);
  foo('hello world!');
  foo(['html', 'css', 'javascript']);

  function bar() {
    console.log('函数也能当参数...');
  }
  // 函数也可以做为参数！！！！
  foo(bar);
</script>
```

函数 `bar` 做参数传给了 `foo` 函数，`bar` 就是所谓的回调函数了！！！

我们回顾一下间歇函数 `setInterval` 

```html
<script>
	function fn() {
    console.log('我是回调函数...');
  }
  // 调用定时器
  setInterval(fn, 1000);
</script>
```

`fn` 函数做为参数传给了 `setInterval` ，这便是回调函数的实际应用了，结合刚刚学习的函数表达式上述代码还有另一种更常见写法。

```html
<script>
  // 调用定时器，匿名函数做为参数
  setInterval(function () {
    console.log('我是回调函数...');
  }, 1000);
</script>
```

结论：

1. 回调函数本质还是函数，只不过把它当成参数使用
2. 使用匿名函数做为回调函数比较常见

## 事件流

事件流是对事件执行过程的描述。

任意事件被触发时总会经历两个阶段：【捕获阶段】和【冒泡阶段】。

简言之，捕获阶段是【从父到子】的传导过程，冒泡阶段是【从子向父】的传导过程。

![event](C:\Users\Lenovo\Desktop\Notes\assets_WEB APIs\event.png)

### 捕获和冒泡

```html
<body>
  <h3>事件流</h3>
  <p>事件流是事件在执行时的底层机制，主要体现在父子盒子之间事件的执行上。</p>
  <div class="outer">
    <div class="inner">
      <div class="child"></div>
    </div>
  </div>
  <script>
    // 获取嵌套的3个节点
    const outer = document.querySelector('.outer');
    const inner = document.querySelector('.inner');
    const child = document.querySelector('.child');
		
    // html 元素添加事件
    document.documentElement.addEventListener('click', function () {
      console.log('html...')
    })
		
    // body 元素添加事件
    document.body.addEventListener('click', function () {
      console.log('body...')
    })

    // 外层的盒子添加事件
    outer.addEventListener('click', function () {
      console.log('outer...')
    })
    
    // 中间的盒子添加事件
    outer.addEventListener('click', function () {
      console.log('inner...')
    })
    
    // 内层的盒子添加事件
    outer.addEventListener('click', function () {
      console.log('child...')
    })
  </script>
</body>
```

现象：当单击事件触发时，其祖先元素的单击事件也【相继触发】。

如果事件是在冒泡阶段执行的，我们称为冒泡模式（默认）：

它会先执行子盒子事件再去执行父盒子事件。

如果事件是在捕获阶段执行的，我们称为捕获模式：

它会先执行父盒子事件再去执行子盒子事件。

```html
<body>
  <h3>事件流</h3>
  <p>事件流是事件在执行时的底层机制，主要体现在父子盒子之间事件的执行上。</p>
  <div class="outer">
    <div class="inner"></div>
  </div>
  <script>
    // 获取嵌套的3个节点
    const outer = document.querySelector('.outer')
    const inner = document.querySelector('.inner')

    // 外层的盒子
    outer.addEventListener('click', function () {
      console.log('outer...')
    }, true) // true 表示在捕获阶段执行事件
    
    // 中间的盒子
    outer.addEventListener('click', function () {
      console.log('inner...')
    }, true)
  </script>
</body>
```

1. **`addEventListener` 第3个参数决定了事件是在捕获阶段触发还是在冒泡阶段触发**
2. **`addEventListener` 第3个参数为  `true` 表示捕获阶段触发，`false` 表示冒泡阶段触发，默认值为 `false`**
3. **事件流只会在父子元素具有相同事件类型时才会产生影响**
4. **绝大部分场景都采用默认的冒泡模式（其中一个原因是早期 IE 不支持捕获）**

### 阻止冒泡

阻止冒泡是指阻断事件的流动，保证事件只在当前元素被执行，而不再去影响到其对应的祖先元素。

事件对象中的 `ev.stopPropagation` 方法，专门用来阻止事件冒泡。



```html
<body>
  <h3>阻止冒泡</h3>
  <p>阻止冒泡是指阻断事件的流动，保证事件只在当前元素被执行，而不再去影响到其对应的祖先元素。</p>
  <div class="outer">
    <div class="inner">
      <div class="child"></div>
    </div>
  </div>
  <script>
    // 获取嵌套的3个节点
    const outer = document.querySelector('.outer')
    const inner = document.querySelector('.inner')
    const child = document.querySelector('.child')

    // 外层的盒子
    outer.addEventListener('click', function () {
      console.log('outer...')
    })

    // 中间的盒子
    inner.addEventListener('click', function (ev) {
      console.log('inner...')

      // 阻止事件冒泡
      ev.stopPropagation()
    })

    // 内层的盒子
    child.addEventListener('click', function (ev) {
      console.log('child...')

      // 借助事件对象，阻止事件向上冒泡
      ev.stopPropagation()
    })
  </script>
</body>
```

### 事件委托

事件委托是利用事件流的特征解决一些现实开发需求的知识技巧

大量的事件监听是比较耗费性能的，所以事件委托主要的作用是提升程序效率。

```html
/*耗费性能版本*/
<script>
  // 假设页面中有 10000 个 button 元素
  const buttons = document.querySelectorAll('table button');

  for(let i = 0; i <= buttons.length; i++) {
    // 为 10000 个 button 元素添加了事件
    buttons.addEventListener('click', function () {
      // 省略具体执行逻辑...
    })
  }
</script>
```

```html
/*优化版本*/
<script>
  // 假设页面中有 10000 个 button 元素
  let buttons = document.querySelectorAll('table button');
  
  // 假设上述的 10000 个 buttom 元素共同的祖先元素是 table
  let parents = document.querySelector('table');
  parents.addEventListener('click', function () {
    console.log('点击任意子元素都会触发事件...');
  })
  /*事件的的冒泡模式总是会将事件流向其父元素的，如果父元素监听了相同的事件类型，那么父元素的事件就会被触发并执行*/
</script>
```

问题：如果table里面还包含其他的标签元素呢？我们要确保是在点击button元素时才触发事件

```html
<script>
  // 假设页面中有 10000 个 button 元素
  const buttons = document.querySelectorAll('table button')
  
  // 假设上述的 10000 个 buttom 元素共同的祖先元素是 table
  const parents = document.querySelector('table')
  parents.addEventListener('click', function (ev) {
    // console.log(ev.target);
    // 只有 button 元素才会真正去执行逻辑
    if(ev.target.tagName === 'BUTTON') {
      // 执行的逻辑
    }
  })
</script>
```

## 元素尺寸与位置

获取元素的自身宽高、包含元素自身设置的宽高、padding、border

offsetWidth和offsetHeight  

获取出来的是数值，方便计算

注意: 获取的是可视宽高，如果盒子是隐藏的，获取的结果是0

## 日期对象

掌握 Date 日期对象的使用，可以动态获取当前计算机的时间。

```javascript
//1.实例化
// const date = new Date(); // 系统默认时间
const date = new Date('2020-05-01') // 指定时间
// date 变量即所谓的时间对象
console.log(typeof date)
```

```javascript
// 2. 调用时间对象方法，通过方法分别获取年、月、日，时、分、秒
const year = date.getFullYear(); // 四位年份
const month = date.getMonth(); // 获取月份，0 ~ 11
const day = date.getDate(); //获取月份中的每一天，不同月份取值也不相同
const week = date.getDay(); //获取星期，取值为 0 ~ 6
const hour = date.getHours(); //获取小时，取值为 0 ~ 23
const minute = date.getMinutes(); //获取分钟，取值为 0 ~ 59
const second = date.getSeconds(); //获取秒，取值为 0 ~ 59
```

```javascript
//3.时间戳（时间戳是指1970年01月01日00时00分00秒起至现在的总秒数或毫秒数，它是一种特殊的计量时间的方式。）
//注：ECMAScript 中时间戳是以毫秒计的。
const date = new Date()
console.log(date.getTime())
console.log(+new Date())
console.log(Date.now())
```

## DOM节点

### 插入节点

**两个关键因素：首先要得到新的 DOM 节点，其次在哪个位置插入这个节点。**

```html
<body>
  <h3>插入节点</h3>
  <p>在现有 dom 结构基础上插入新的元素节点</p>
  <hr>
  <!-- 普通盒子 -->
  <div class="box"></div>
  <!-- 点击按钮向 box 盒子插入节点 -->
  <button class="btn">插入节点</button>
  <script>
    // 点击按钮，在网页中插入节点
    const btn = document.querySelector('.btn')
    btn.addEventListener('click', function () {
      // 1. 获得一个 DOM 元素节点
      const p = document.createElement('p')
      p.innerText = '创建的新的p标签'
      p.className = 'info'
      
      // 复制原有的 DOM 节点
      const p2 = document.querySelector('p').cloneNode(true)
      p2.style.color = 'red'

      // 2. 插入盒子 box 盒子
      document.querySelector('.box').appendChild(p)
      document.querySelector('.box').appendChild(p2)
    })
  </script>
</body>
```

- `createElement` 动态创建任意 DOM 节点
- `cloneNode` 复制现有的 DOM 节点，传入参数 true 会复制所有子节点
- `appendChild` 在末尾（结束标签前）插入节点

```html
<body>
  <h3>插入节点</h3>
  <p>在现有 dom 结构基础上插入新的元素节点</p>
	<hr>
  <button class="btn1">在任意节点前插入</button>
  <ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
  </ul>
  <script>
    // 点击按钮，在已有 DOM 中插入新节点
    const btn1 = document.querySelector('.btn1')
    btn1.addEventListener('click', function () {

      // 第 2 个 li 元素
      const relative = document.querySelector('li:nth-child(2)')

      // 1. 动态创建新的节点
      const li1 = document.createElement('li')
      li1.style.color = 'red'
      li1.innerText = 'Web APIs'

      // 复制现有的节点
      const li2 = document.querySelector('li:first-child').cloneNode(true)
      li2.style.color = 'blue'

      // 2. 在 relative 节点前插入
      document.querySelector('ul').insertBefore(li1, relative)
      document.querySelector('ul').insertBefore(li2, relative)
    })
  </script>
</body>
```

- `insertBefore` 在父节点中任意子节点之前插入新节点

### 删除节点

**两个因素：首先由父节点删除子节点，其次是要删除哪个子节点。**

```html
<body>
  <!-- 点击按钮删除节点 -->
  <button>删除节点</button>
  <ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>Web APIs</li>
  </ul>

  <script>
    const btn = document.querySelector('button')
    btn.addEventListener('click', function () {
      // 获取 ul 父节点
      let ul = document.querySelector('ul')
      // 待删除的子节点
      let lis = document.querySelectorAll('li')

      // 删除节点
      ul.removeChild(lis[0])
      /*`removeChild` 删除节点时一定是由父子关系。*/
    })
  </script>
</body>
```

### 查找节点

DOM 树中的任意节点都不是孤立存在的，它们要么是父子关系，要么是兄弟关系。

因此，我们可以依据节点之间的关系查找节点。

#### 父子关系

```html
<body>
  <button class="btn1">所有的子节点</button>
  <!-- 获取 ul 的子节点 -->
  <ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript 基础</li>
    <li>Web APIs</li>
  </ul>
  <script>
    const btn1 = document.querySelector('.btn1')
    btn1.addEventListener('click', function () {
      // 父节点
      const ul = document.querySelector('ul')

      // 所有的子节点
      console.log(ul.childNodes)
      // 只包含元素子节点
      console.log(ul.children)
    })
  </script>
</body>
```

- `childNodes` 获取全部的子节点，回车换行会被认为是空白文本节点
- `children` 只获取元素类型节点

```html
<body>
  <table>
    <tr>
      <td width="60">序号</td>
      <td>课程名</td>
      <td>难度</td>
      <td width="80">操作</td>
    </tr>
    <tr>
      <td>1</td>
      <td><span>HTML</span></td>
      <td>初级</td>
      <td><button>变色</button></td>
    </tr>
    <tr>
      <td>2</td>
      <td><span>CSS</span></td>
      <td>初级</td>
      <td><button>变色</button></td>
    </tr>
    <tr>
      <td>3</td>
      <td><span>Web APIs</span></td>
      <td>中级</td>
      <td><button>变色</button></td>
    </tr>
  </table>
  <script>
    // 获取所有 button 节点，并添加事件监听
    const buttons = document.querySelectorAll('table button')
    for(let i = 0; i < buttons.length; i++) {
      buttons[i].addEventListener('click', function () {
        // console.log(this.parentNode); // 父节点 td
        // console.log(this.parentNode.parentNode); // 爷爷节点 tr
        this.parentNode.parentNode.style.color = 'red'
      })
    }
  </script>
</body>
```

- `parentNode` 获取父节点，以相对位置查找节点，实际应用中非常灵活。

#### 兄弟关系

```html
<body>
  <ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript 基础</li>
    <li>Web APIs</li>
  </ul>
  <script>
    // 获取所有 li 节点
    const lis = document.querySelectorAll('ul li')

    // 对所有的 li 节点添加事件监听
    for(let i = 0; i < lis.length; i++) {
      lis[i].addEventListener('click', function () {
        // 前一个节点
        console.log(this.previousSibling)
        // 下一下节点
        console.log(this.nextSibling)
      })
    }
  </script>
</body>
```

- `previousSibling` 获取前一个节点，以相对位置查找节点，实际应用中非常灵活。
- `nextSibling` 获取后一个节点，以相对位置查找节点，实际应用中非常灵活。

## 定时器-延迟函数

1. **语法：**

```
setTimeout(回调函数, 延迟时间)
清除延时函数：clearTimeout(timerId)
```

2. setTimeout 仅仅只执行一次，所以可以理解为就是把一段代码延迟执行, 平时省略window
3. 延时函数需要等待，所以后面的代码先执行
4. 返回值是一个正整数，表示定时器的编号

```html
<body>
  <script>
    // 定时器之延迟函数

    // 1. 开启延迟函数
    let timerId = setTimeout(function () {
      console.log('我只执行一次')
    }, 3000)

    // 1.1 延迟函数返回的还是一个正整数数字，表示延迟函数的编号
    console.log(timerId)

    // 1.2 延迟函数需要等待时间，所以下面的代码优先执行

    // 2. 关闭延迟函数
    clearTimeout(timerId)

  </script>
</body>
```

## BOM

**BOM** (Browser Object Model ) 是浏览器对象模型

![1676047436362](C:\Users\Lenovo\Desktop\Notes\assets_WEB APIs\1676047436362.png)

### windows对象

- window对象是一个全局对象，也可以说是JavaScript中的顶级对象
- 像document、alert()、console.log()这些都是window的属性，基本BOM的属性和方法都是window的
- 所有通过var定义在全局作用域中的变量、函数都会变成window对象的属性和方法
- window对象下的属性和方法调用的时候可以省略window

### location对象

location (地址) 它拆分并保存了 URL 地址的各个组成部分， 它是一个对象

| 属性/方法 |                         说明                         |
| :-------: | :--------------------------------------------------: |
|   href    |   属性，获取完整的 URL 地址，赋值时用于地址的跳转    |
|  search   |     属性，获取地址中携带的参数，符号 ？后面部分      |
|   hash    |      属性，获取地址中的啥希值，符号 # 后面部分       |
| reload()  | 方法，用来刷新当前页面，传入参数 true 时表示强制刷新 |

```html
<body>
  <form>
    <input type="text" name="search"> <button>搜索</button>
  </form>
  <a href="#/music">音乐</a>
  <a href="#/download">下载</a>

  <button class="reload">刷新页面</button>
  <script>
    // location 对象  
    // 1. href属性 （重点） 得到完整地址，赋值则是跳转到新地址
    console.log(location.href)
    // location.href = 'http://www.itcast.cn'

    // 2. search属性  得到 ? 后面的地址 
    console.log(location.search)  // ?search=笔记本

    // 3. hash属性  得到 # 后面的地址
    console.log(location.hash)

    // 4. reload 方法  刷新页面
    const btn = document.querySelector('.reload')
    btn.addEventListener('click', function () {
      // location.reload() // 页面刷新
      location.reload(true) // 强制页面刷新 ctrl+f5
    })
  </script>
</body>
```

### navigator对象

navigator是对象，该对象下记录了浏览器自身的相关信息.

```javascript
// 通过 userAgent 检测浏览器的版本及平台
(function () {
  const userAgent = navigator.userAgent
  // 验证是否为Android或iPhone
  const android = userAgent.match(/(Android);?[\s\/]+([\d.]+)?/)
  const iphone = userAgent.match(/(iPhone\sOS)\s([\d_]+)/)
  // 如果是Android或iPhone，则跳转至移动站点
  if (android || iphone) {
    location.href = 'http://m.itcast.cn'
  }})();
```

### history对象

history (历史)是对象，主要管理历史记录， 该对象与浏览器地址栏的操作相对应，如前进、后退等.

history对象一般在实际开发中比较少用，但是会在一些OA 办公系统中见到。

| history对象方法 |                             作用                             |
| :-------------: | :----------------------------------------------------------: |
|     back()      |                             后退                             |
|    forward()    |                             前进                             |
|    go(参数)     | 前进后退功能 参数如果是1就前进一个页面 如果是-1就后退一个页面 |

```html
<body>
  <button class="back">←后退</button>
  <button class="forward">前进→</button>
  <script>
    // histroy对象

    // 1.前进
    const forward = document.querySelector('.forward')
    forward.addEventListener('click', function () {
      // history.forward() 
      history.go(1)
    })
    // 2.后退
    const back = document.querySelector('.back')
    back.addEventListener('click', function () {
      // history.back()
      history.go(-1)
    })
  </script>
</body>
```

### 本地储存

作用：将数据存储在本地浏览器中，页面刷新数据不丢失，实现数据持久化。

容量较大，sessionStorage和 localStorage 约 5M 左右

#### localStorage（重点）

将数据以键值对的形式存储，并且存储的是字符串，省略了window，及时刷新页面或者关闭页面，数据也不会丢失。

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>本地存储-localstorage</title>
</head>

<body>
  <script>
    // 本地存储 - localstorage 存储的是字符串 
    // 1. 存储
    localStorage.setItem('age', 18)

    // 2. 获取
    console.log(typeof localStorage.getItem('age'))

    // 3. 删除
    localStorage.removeItem('age')
  </script>
</body>

</html>
```

#### sessionStorage（了解）

用法和localStorage基本相同。

区别是：当页面浏览器被关闭时，存储在sessionStorage的数据会被清除

```
存储：sessionStorage.setItem(key,value)
获取：sessionStorage.getItem(key)
删除：sessionStorage.removeItem(key)
```

#### localStorage 存储复杂数据类型

存储过程

**问题：**本地只能存储字符串,无法存储复杂数据类型.

**解决：**需要将复杂数据类型转换成 JSON字符串,在存储到本地

**语法：**JSON.stringify(复杂数据类型)

提取过程

**问题：**因为本地存储里面取出来的是字符串，不是对象，无法直接使用

**解决： **把取出来的字符串转换为对象

**语法：**JSON.parse(JSON字符串)

```
<body>
  <script>
    // 本地存储复杂数据类型
    const goods = {
      name: '小米',
      price: 1999
    }
    // localStorage.setItem('goods', goods)
    // console.log(localStorage.getItem('goods'))

    // 1. 把对象转换为JSON字符串  JSON.stringify
    localStorage.setItem('goods', JSON.stringify(goods))
    // console.log(typeof localStorage.getItem('goods'))

    // 2. 把JSON字符串转换为对象  JSON.parse
    console.log(JSON.parse(localStorage.getItem('goods')))

  </script>
</body>
```

补充：JSON字符串

- 首先是1个字符串
- 属性名使用双引号引起来，不能单引号
- 属性值如果是字符串型也必须双引号

## 正则表达式

**正则表达式**（Regular Expression）是一种字符串匹配的模式（规则）。

在VScode里使用需要先安装插件。

![1676080548639](C:\Users\Lenovo\Desktop\Notes\assets_WEB APIs\1676080548639.png)

**使用场景：**

- 例如验证表单：手机号表单要求用户只能输入11位的数字 (匹配)
- 过滤掉页面内容中的一些敏感词(替换)，或从字符串中获取我们想要的特定部分(提取)等 

![1676079666366](C:\Users\Lenovo\Desktop\Notes\assets_WEB APIs\1676079666366.png)

### 正则表达式的基本使用

```javascript
/*第一步：定义规则*/
const reg =  /web/  //  /  /里面填正则表达式字面量，即表达式，这是个对象
/*第二部：使用规则*/
const str = 'web前端开发'
console.log(reg.test(str))  // true  如果符合规则匹配上则返回true
console.log(reg.test('java开发'))  // false  如果不符合规则匹配上则返回 false
```

### 元字符（特殊字符）

元字符是一些具有特殊含义的字符，可以极大提高了灵活性和强大的匹配功能。

#### 边界符

| 边界符 | 说明                           |
| ------ | ------------------------------ |
| ^      | 表示匹配行首的文本（以谁开始） |
| $      | 表示匹配行尾的文本（以谁结束） |
| ^$     | 精准匹配                       |

```html
<body>
  <script>
    // 元字符之边界符
    // 1. 匹配开头的位置 ^
    const reg = /^web/
    console.log(reg.test('web前端'))  // true
    console.log(reg.test('前端web'))  // false
    console.log(reg.test('前端web学习'))  // false
    console.log(reg.test('we'))  // false

    // 2. 匹配结束的位置 $
    const reg1 = /web$/
    console.log(reg1.test('web前端'))  //  false
    console.log(reg1.test('前端web'))  // true
    console.log(reg1.test('前端web学习'))  // false
    console.log(reg1.test('we'))  // false  

    // 3. 精确匹配 ^ $
    const reg2 = /^web$/
    console.log(reg2.test('web前端'))  //  false
    console.log(reg2.test('前端web'))  // false
    console.log(reg2.test('前端web学习'))  // false
    console.log(reg2.test('we'))  // false 
    console.log(reg2.test('web'))  // true
    console.log(reg2.test('webweb'))  // flase 
  </script>
</body>
```

#### 量词

| 量词  | 说明             |
| ----- | ---------------- |
| *     | 重复零次或更多次 |
| +     | 重复一次或更多次 |
| ？    | 重复零次或一次   |
| {n}   | 重复n次          |
| {n,}  | 重复n次或更多次  |
| {n,m} | 重复n次到m次     |

```html
<body>
  <script>
    // 元字符之量词
    // 1. * 重复次数 >= 0 次
    const reg1 = /^w*$/
    console.log(reg1.test(''))  // true
    console.log(reg1.test('w'))  // true
    console.log(reg1.test('ww'))  // true
    console.log('-----------------------')

    // 2. + 重复次数 >= 1 次
    const reg2 = /^w+$/
    console.log(reg2.test(''))  // false
    console.log(reg2.test('w'))  // true
    console.log(reg2.test('ww'))  // true
    console.log('-----------------------')

    // 3. ? 重复次数  0 || 1 
    const reg3 = /^w?$/
    console.log(reg3.test(''))  // true
    console.log(reg3.test('w'))  // true
    console.log(reg3.test('ww'))  // false
    console.log('-----------------------')


    // 4. {n} 重复 n 次
    const reg4 = /^w{3}$/
    console.log(reg4.test(''))  // false
    console.log(reg4.test('w'))  // flase
    console.log(reg4.test('ww'))  // false
    console.log(reg4.test('www'))  // true
    console.log(reg4.test('wwww'))  // false
    console.log('-----------------------')

    // 5. {n,} 重复次数 >= n 
    const reg5 = /^w{2,}$/
    console.log(reg5.test(''))  // false
    console.log(reg5.test('w'))  // false
    console.log(reg5.test('ww'))  // true
    console.log(reg5.test('www'))  // true
    console.log('-----------------------')

    // 6. {n,m}   n =< 重复次数 <= m
    const reg6 = /^w{2,4}$/
    console.log(reg6.test('w'))  // false
    console.log(reg6.test('ww'))  // true
    console.log(reg6.test('www'))  // true
    console.log(reg6.test('wwww'))  // true
    console.log(reg6.test('wwwww'))  // false

    // 7. 注意事项： 逗号两侧千万不要加空格否则会匹配失败

  </script>
```

#### 范围

| 范围   | 说明                                                |
| ------ | --------------------------------------------------- |
| [abc]  | 匹配包含的单个字符，即 a\|\|b\|\|c。（多选一模式）  |
| [a-z]  | 连字符，用来指定单词范围，该式表示 a-z 26个英文字母 |
| [^abc] | 取反符，匹配除了abc以外的其它字符                   |

```html
<body>
  <script>
    // 元字符之范围  []  
    // 1. [abc] 匹配包含的单个字符， 多选1
    const reg1 = /^[abc]$/
    console.log(reg1.test('a'))  // true
    console.log(reg1.test('b'))  // true
    console.log(reg1.test('c'))  // true
    console.log(reg1.test('d'))  // false
    console.log(reg1.test('ab'))  // false

    // 2. [a-z] 连字符 单个
    const reg2 = /^[a-z]$/
    console.log(reg2.test('a'))  // true
    console.log(reg2.test('p'))  // true
    console.log(reg2.test('0'))  // false
    console.log(reg2.test('A'))  // false
    // 想要包含小写字母，大写字母 ，数字
    const reg3 = /^[a-zA-Z0-9]$/
    console.log(reg3.test('B'))  // true
    console.log(reg3.test('b'))  // true
    console.log(reg3.test(9))  // true
    console.log(reg3.test(','))  // flase

    // 用户名可以输入英文字母，数字，可以加下划线，要求 6~16位
    const reg4 = /^[a-zA-Z0-9_]{6,16}$/
    console.log(reg4.test('abcd1'))  // false 
    console.log(reg4.test('abcd12'))  // true
    console.log(reg4.test('ABcd12'))  // true
    console.log(reg4.test('ABcd12_'))  // true

    // 3. [^a-z] 取反符
    const reg5 = /^[^a-z]$/
    console.log(reg5.test('a'))  // false 
    console.log(reg5.test('A'))  // true
    console.log(reg5.test(8))  // true

  </script>
</body>
```

#### 字符类

某些常见模式的简写方式，区分数字和字母

| 字符类 | 说明                                                   |
| ------ | ------------------------------------------------------ |
| \d     | [0-9]                                                  |
| \D     | [^0-9]                                                 |
| \w     | 匹配任意的字母数字和下划线：[A-Za-z0-9_]               |
| \W     | [^A-Za-z0-9_]                                          |
| \s     | 匹配空格（包括换行符，制表符，空格符等）：[\t\r\n\v\f] |
| \S     | [^ \t\r\n\v\f]                                         |

![1676080372325](C:\Users\Lenovo\Desktop\Notes\assets_WEB APIs\1676080372325.png)

### 替换和修饰符

```
字符串.replace(/正则表达式/,'替换的文本')
```

```html
<body>
  <script>
    // 替换和修饰符
    const str = '欢迎大家学习前端，相信大家一定能学好前端，都成为前端大神'
    // 1. 替换  replace  需求：把前端替换为 web
    // 1.1 replace 返回值是替换完毕的字符串
    // const strEnd = str.replace(/前端/, 'web') 只能替换一个
  </script>
</body>
```

```html
<body>
  <script>
    // 替换和修饰符
    const str = '欢迎大家学习前端，相信大家一定能学好前端，都成为前端大神'
    // 1. 替换  replace  需求：把前端替换为 web
    // 1.1 replace 返回值是替换完毕的字符串
    // const strEnd = str.replace(/前端/, 'web') 只能替换一个

    // 2. 修饰符 g 全部替换
    const strEnd = str.replace(/前端/g, 'web')
    console.log(strEnd) 
  </script>
</body>
```

修饰符约束正则执行的某些细节行为，如是否区分大小写、是否支持多行匹配等

- i 是单词 ignore 的缩写，正则匹配时字母不区分大小写
- g 是单词 global 的缩写，匹配所有满足正则表达式的结果