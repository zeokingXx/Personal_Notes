# HTML（于2025.1.1更新）

> *基于VScode开发*
>
> 第一步：
>
> 下载vscode
>
> [Visual Studio Code - Code Editing. Redefined](https://code.visualstudio.com/)
>
> 笔记软件：Typora
>
> [Typora 官方中文站](https://typoraio.cn/)
>
> 第二步：安装插件
>
> - Chinese插件
> - 安装插件open in browser
> - 安装live server
>
> 通过网盘分享的文件：黑马一整套
> 链接: https://pan.baidu.com/s/1Z2jAe3_Oee_qQ59on38YUw?pwd=tadi 提取码: tadi
>
> 
>
> HTML（HyperText Markup Language）是一种用于创建网页的标记语言。
>
> 它通过标记符号来描述网页的结构和内容，是万维网（World Wide Web）的基础语言。
>
> HTML可以用来创建静态网页，也可以与JavaScript和CSS等技术结合，创建动态交互式的网页。
>
> HTML文档由各种元素（elements）组成，如标题、段落、列表、链接、图片等。

## 附：快捷键：

Ctrl+B 隐藏侧栏

Ctrl+S 保存文件

Ctrl+/ 添加/删除注释

Ctrl+Enter（Shift+小键盘的2） 切换下一行

Ctrl+A 全选

Ctrl+Z 撤销/回退

Ctrl+Y 恢复

Shift+英文状态的- 打出下划线

Alt+L+O 运行

Alt+Z 选中文段后自动换行

快速选择某行：在VScode中点击最前面的行号

多行缩进：选中多行 + Tab

取消多行缩进：选中多行 + Shift + Tab

F12：打开网页调试工具（谷歌浏览器）

## 附：路径的概念

相对路径：以当前文件位置为节点

绝对路径：以盘符或根目录为节点

**相对路径的表达方式：**

- .当前文件夹

- ..上级文件夹

- /进入当前文件夹

**绝对路径的表达方式：**

用/或者\来连接，为了windows系统的兼容性，往往选择/来分隔

在之后的标签学习中，将会反复用到相对路径

## 一.HTML骨架

HTML骨架一般不需要我们记住

在VScode中，在英文模式下使用快捷键！＋ Enter/Tab 可快速生成HTML骨架

细节解释：

- `<!DOCTYPE html>` ：称为 DTD (文档类型定义)，描述当前的文件是一个 HTML5 的文件。

- `<html lang="en">`：其中 lang 属性表示当前页面是一个 "英语页面"， 这里暂时不用管。(有些浏览器会根据此处的声明提示是否进行自动翻译)

- `<meta charset="UTF-8">`：描述页面的字符编码方式，没有这一行可能会导致中文乱码。

- `<meta name="viewport" content="width=device-width, initial-scale=1.0">`：

  其中 viewport 指的是设备的屏幕上能用来显示我们的网页的那一块区域，content="width=device-width, initial-scale=1.0" 在设置可视区和设备宽度等宽，并设置初始缩放为不缩放。(这个属性对于移动端开发更重要一些)

```html
<!DOCTYPE html>
<html lang="en">
    <!-- <html></html>是整个网站的骨架 -->
<head>
    <!-- <head></head>网页头部，用于存放给浏览器看的代码，如CSS -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
    <!-- <title></title>网页标题，即在浏览器导航栏中显示的内容 -->
</head>

<body>
  <!-- 在这里写下你任何想要写下的内容，记得使用Ctrl+S保存哦！ -->
  <!-- <body></body>网页主题，用来存放给用户看的代码，例如图片文字 -->
  <!-- 书写完毕后鼠标右键，Open in Browser，即可在浏览器中查看你的成果！ -->
</body>

</html>
```

## 二.标题标签`<h？></h？>`

特点：

- 双标签

- 字体加粗且独占一行

- h1-h6 字体依次变小

**注意：在网页开发中，h1标签往往只使用一次！！！**

```html
<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>
<h4>四级标题</h4>
<h5>五级标题</h5>
<h6>六级标题</h6>
```

![](https://i-blog.csdnimg.cn/blog_migrate/93dfacea9677eb841a3e7e2a0900d34c.png)

## 三.段落标签 `<p></p>`

在html中输入换行之后不会真的换行，而是产生一个空格。

在html中输入多个空格之后，在网页上显示的时候不会有多个空格，而是只有一个空格。

在html中，如果需要有一段特别长的文字，但是这段文字在网页上显示的时候并没有产生段落，而是全在一起。这样可读性就会很差，所以需要用到段落标签。

特点：

- 双标签


- 独占一行


- 段落（paragraph）之间有空隙

**注意：如果要在处于段落标签内部文字串中间加嵌套标签的话，先打一个空格把一段文字分割成两段，这样再输入嵌套标签时才会出现快捷输入**

```html
<h1>换行标签和段落标签</h1>
<p>这是段落1。</p>
<p>这是段落2。</p>
<p>这是段落3。</p>
```

![](https://i-blog.csdnimg.cn/blog_migrate/606b4b492a73ab6a3166deb3b095455a.png)

## 四.换行标签`<br>`

特点：

- 单标签

- 可以起到换行的作用，但不会像段落标签那样产生很大的空隙。

- 可叠加使用，有几个`<br>`就换几行

## 五.水平线标签`<hr>`

特点：

- 单标签

- 往往和标题标签在表头一同使用，用于分割网页的布局


## 六.文本格式标签

### 加粗 `<strong> 或 <b>`

### 倾斜`<em> 或 <i>`

### 下划线`<ins> 或 <n>`

### 删除线`<del> 或 <s>`

**注意：在网页开发中一般使用前者！！！**

```html
<body>
    <Strong>加粗</Strong>
    <b>加粗</b>
 
    <em>倾斜</em>
    <i>倾斜</i>
 
    <del>删除线</del>
    <s>删除线</s>
    
    <ins>下划线</ins>
    <u>下划线</u>
 
</body>
```

![](https://i-blog.csdnimg.cn/blog_migrate/2a711803ea0300118c0275d9246706fd.png)

## 七.图像标签 `<img>`

作用：用于在网页中插入照片

```html
<img src="./image.jpg" alt="示例图片" title="这是一张照片" width="" height="" >
```

参数解释：

- src：img标签的必需属性，属性值为图片的位置和名称，用相对路径或者绝对路径来表示。

  **需要注意的是，我们可以在其他网页直接复制展示的照片的地址，网址也属于绝对路径，这个操作常用于制作友情链接**

- alt：图片无法正常显示时替换的照片，常用于网速慢照片无法及时加载的情况

- title：鼠标停在图片上时显示的文字

- width和height：都是控制图片大小的参数，在网页中，动了其中一个参数的属性值，另一个也会改变，实现等比例缩放。**一般在HTML不用这两个参数，照片的大小往往是在CSS中进行设计的**


## 八.超链接标签`<a></a>`

超链接标签默认有字体为蓝，有下划线的样式！

参数解释：

- herf：超链接标签的必需属性。作用是指向跳转地址，可以是其他网址（外部链接），也可以使用相对路径（内部链接）来跳转到本地的文件
- target="_blank"：加上这个参数后，可以控制新窗口的打开，原窗口保留

```html
<a href="http://scpc.fun/home" target="_blank">滚去学习</a>
<a href="./index.html" target="_blank">我的网页</a>
```

超链接标签在实际运用中可以和其他标签嵌套使用来实现丰富的功能：

```html
<h1>点击图片跳转链接</h1>
<a href="http://scpc.fun/home"><img src="./assert/1.png" alt=""></a>
<h1>按钮跳转</h1>
<a href="http://scpc.fun/home"><button>你猜跳到哪</button></a>
<h1>点击下载文件</h1>
<a href="OIP.zip">点击下载</a>

<h1>描点链接</h1>
<a href="#1">跳转到1</a>
<a href="#2">跳转到2</a>
<p id="1">
    abc <br>
    def <br>
</p>
<p></p>
<p></p>
<p id="2">
    hhh <br>
    mooo <br>
</p>
```

**注意：在实际开发中，网页建立初期，往往在使用超链接标签时，对跳转地址不确定，这时可以将href的属性值设置为"#"，称为空链接！！！**

## 九.音频标签`<audio></audio>`

参数解释：

- src：音频标签的必需属性，用来输入音频的URL（支持.MP3，.Ogg，.Wav）
- controls：显示音频控制面板（播放，暂停等）
- loop：循环播放
- autoplay：自动播放（一些浏览器会禁用这一功能，需要手动打开）

```html
<h1>音频示例</h1>
<audio src="./assert/music.mp3" controls loop muted autoplay></audio>
```

**注意有如下规则：**

**在HTML代码中，如果属性名和属性值完全一样，可以简写成一个单词（学习所有标签都适用）！！！**

## 十.视频标签`<video></video>`

参数解释：

- src：和音频标签的属性相似

- controls：和音频标签的属性相似

- loop：和音频标签的属性相似

- muted：静音播放

- autoplay：和音频标签中autoplay的功能一样，

  **但要注意的是，自动播放视频这一功能在浏览器中是可以实现的，需要和muted一同使用才可以达到这一效果，否则无效！！！**

```html
<video src="./assert/movie.mp4" controls loop muted autoplay></video>
```

## 十一.列表标签

作用：布局内容排列整齐的区域

拓展：去掉列表的项目符号写法：

```css
li {
    list-style:none;
}
```

### 无序列表`<ul></ul>`

特点：不需要规定顺序

```html
<ul><h1>水果</h1>
    <li>1</li>
    <li>2</li>
    <li>3</li>
    <li>4</li>
</ul>
<!-- Emmet写法：ul>li{$}*4 -->
```

```html
<h1>无序标签示例</h1>
<ul><h1>水果</h1>
<!-- <ul>代表无序列表 -->
    <li>苹果</li>
    <li>香蕉</li>
    <li>橘子</li>
    <li>西瓜</li>
    <!-- <li>代表列表条目 -->
</ul>
<!-- <ul>和<li>是嵌套关系 -->
```

**注意：`<ul></ul>`标签只能包裹`<li></li>`标签，`<li></li>`标签可以嵌套任何标签**

### 有序列表`<ol></ol>`

特点：需要规定顺序

```html
<h1>有序标签示例</h1>
<ol><h1>动物</h1>
<!-- <ol>代表有序列表 -->
    <li>大象</li>
    <li>老虎</li>
    <li>狮子</li>
    <li>猫</li>
    <!-- <li>代表列表条目 -->
</ol>
<!-- <ol>和<li>是嵌套关系 -->
```

**注意：`<ol></ol>`标签只能包裹`<li></li>`标签，`<li></li>`标签可以嵌套任何标签**

### 定义列表`<dl></dl>`

常用于页面底部，一个标题对应多行内容（帮助中心栏）

```html
<h1>自定义标签</h1>
    <dl>
    <!-- <dl></dl>标签用来代表定义列表 -->
        <dt><p>你是谁</p></dt>
        <!-- <dt>内容1</dt> -->
        <!-- <dt></dt>标签用来定义列表的标题 -->
        <dd>我是王肖磊</dd>
        <!-- <dd>描述1</dd> -->
        <!-- <dd>描述2</dd> -->
        <!-- <dd></dd>标签用来定义列表的描述/详情 -->
        <!-- <dd></dd>标签内的内容会自动向前缩进，形成一个类似列表的层级效果 -->
        <dt>你是个什么人</dt>
        <dd>我是一个前端工程师</dd>
    </dl>
```

**注意：`<dl></dl>`标签只能包裹`<dt></dt>`标签和`<dd></dd>`标签，`<dt></dt>`标签和`<dd></dd>`标签可以嵌套任何标签**

## 十二.表格标签`<table></table>`

与excel表格相似，用来展示数据

|       标签        |          描述          |
| :---------------: | :--------------------: |
| `<table></table>` |       表格框架。       |
|    `<tr></tr>`    |  用于定义表格的一行。  |
|    `<td></td>`    | 用于定义表格的单元格。 |
|    `<th></th>`    |  用于定义表头单元格。  |

参数解释

border：为表格添加边框线，一开始的表格是默认没有边框线的，属性值代表n像素的边框线粗细，一般设为1

width/height：设置表格大小的，一般不常用，表格具有自适应能力（根据所填内容的长度自动变换大小）

```html
<h1>表格标签示例</h1>
<table border="1" width="400px">
<!-- <table></table>表格框架 -->
    <tr>
    <!-- <tr></tr>行标签，有几行就是几个<tr></tr>标签 -->
        <th>姓名</th>
        <th>年龄</th>
        <th>性别</th>
        <!-- <th></th>表头标签，显示的内容加粗且居中 -->
    </tr>

    <tr>
        <td>王肖磊</td>
        <!-- <td></td>内容单元格标签 -->
        <td>20</td>
        <td>男</td>
    </tr>
</table>
```

### 合并单元格操作

1. 明确目标

2. 对于多项同类信息的单元格，保留最左最上的单元格，为这个单元格添加属性，对应的属性值为数字，表示需要合并的单元格数量

   跨行合并：保留最上面的单元格，`<td rowspan='2'>要合并的内容</td>`

   跨列合并：保留最上面的单元格，`<td colspan='2'>要合并的内容</td>`

   ![](https://i-blog.csdnimg.cn/blog_migrate/d05755584fa4f640210c083f247355fa.png)

3. 删除其他单元格

实现该操作的代码如下：

```html
<table width="300px" height="200px" border="1px" align="center" cellspacing="0px" cellpadding="2px">
    <tr>
        <th>姓名</th>
        <th colspan="2">属性</th>
		<!--<th>技能</th>-->
    </tr>
    
    <tr>
        <td rowspan="2">葫芦娃</td>
        <td>6</td>
        <td>喷火</td>
    </tr>
    
    <tr>
		<!--<td>三娃</td>-->
        <td>5</td>
        <td>喷水</td>
    </tr>
</table>

```

![](https://i-blog.csdnimg.cn/blog_migrate/56922c35ed6f0f009a60e2ca7fba5160.png)

**注意：不能跨结构标签进行合并！！！**

## 十三.表格结构标签

|    标签     |                        描述                        |
| :---------: | :------------------------------------------------: |
| `<caption>` |                 用于定义表格标题。                 |
|  `<thead>`  | 用于定义表格的头部。一般包含列名、行号等表头信息。 |
|  `<tbody>`  |       用于定义表格的主体。一般包含数据内容。       |
|  `<tfoot>`  |                用于定义表格的脚注。                |

以上标签是对浏览器进行说明（但是是写在`<body></body>`内的），对实际显示效果无影响

![](https://i-blog.csdnimg.cn/blog_migrate/66182db872c56e31e5f3a2dcb66cec1c.png)

```html
<h1>表格结构标签</h1>
<table>
    <caption>
        <h2>商品信息表</h2>
        <p>制表：2023/07/13</p>
    </caption>
    
    <thead>
        <tr>
            <th>ID</th>
            <th>品类</th>
            <th>品名</th>
            <th>数量</th>
            <th>单价</th>
            <th>金额</th>
        </tr>
    </thead>
    
    <tbody>
        <tr>
            <td>1</td>
            <td>衣服</td>
            <td>冬装</td>
            <td>1</td>
            <td>100</td>
            <td>100</td>
        </tr>
        
        <tr>
            <td>2</td>
            <td>衣服</td>
            <td>夏装</td>
            <td>1</td>
            <td>100</td>
            <td>100</td>
        </tr>
        
        <tr>
            <td>3</td>
            <td>饮料</td>
            <td>可口可乐</td>
            <td>1</td>
            <td>100</td>
            <td>100</td>
        </tr>
        
        <tr>
            <td>4</td>
            <td>饮料</td>
            <td>百事可乐</td>
            <td>1</td>
            <td>100</td>
            <td>100</td>
        </tr>
    </tbody>
</table>
```

![](https://i-blog.csdnimg.cn/blog_migrate/788d5974d1460a05b9ba85938bd0cc1c.png#pic_center)

## 十四.表单标签`<form></form>`

功能：用于收集用户信息，包含登录，查找，搜索功能

**注意：在本节中所有学习的标签都需要在`<form></form>`标签下使用才能发挥作用！！！**

```html
<form action="#" name="login" method="POST"></form>
```

![](https://i-blog.csdnimg.cn/blog_migrate/92f9290e3ff83a43ed816c38bc3fbfe9.png#pic_center)

### input标签类型

```html
<form action="https://www.baidu.com" method="get">
        <!-- form 中的数据-->
        姓名：<input type="text"><br> <!-- 文本框-->
        密码：<input type="password"><br>  <!-- 密码框-->
        性别：<input type="radio" name="sex" value="男">男&nbsp;&nbsp;&nbsp;&nbsp;<!-- 单选框-->
        <input type="radio" name="sex" value="女">女 &nbsp;&nbsp;&nbsp;&nbsp;
        <input type="radio" name="sex" value="第三性别">第三性别<br>
 
        爱好：<input type="checkbox">听音乐&nbsp;&nbsp; <!-- 复选框-->
        <input type="checkbox">看电视&nbsp;&nbsp;
        <input type="checkbox">打羽毛球 <br>
 
        头像：<input type="file"> <br> <!-- 选择文件标签-->
        日期：<input type="date">   <!-- 日期-->
        颜色：<input type="color">  <!--颜色-->
        提交：<input type="submit">  <!-- 提交按钮-->
</form>
```

![](https://i-blog.csdnimg.cn/blog_migrate/4123238a40e514b8b16500b610f4fd15.png)

参数解释：（常用的）

| type属性值 |                     说明                      |
| :--------: | :-------------------------------------------: |
|    text    |           文本框，用于输入单行文本            |
|  password  | 密码框，输入的内容会显示为*号，能保护用户隐私 |
|   radio    |                  单选框（⭕）                  |
|  checkbox  |                  多选框（▢）                  |
|    file    |                 上传本地文件                  |

**注意：这些属性值使用的时候不会自动换行，需要搭配`<br>`一起使用**

#### 文本框 text

```html
<label>输入框：</label><input type="text" name="username" id="username" placeholder="这是输入框"><br>
<!--输入框：<input type="text" name="username" id="username" placeholder="这是输入框">-->
<!--两种方法都可以，加<lable></lable>标签是为了规范性-->
```

参数解释：

placeholder：用来显示文本框/密码框中的提示文本（占位文本）

name 和 id：后期与JS配合使用

![](https://i-blog.csdnimg.cn/blog_migrate/c3cd7d981143392c2e420e625bd7df09.png#pic_center)

#### 密码框 password

```html
<label>密码框：</label><input type="password" placeholder="这是密码框"><br>
```

![](https://i-blog.csdnimg.cn/blog_migrate/ef231aed5f218211d21a3fb98d138338.png#pic_center)

#### 单选框 radio

**注意：系统默认没有单选这个功能，如果想要实现单选功能，则必须将所有单选框都加上name属性值（name的属性值可以自定义，最好见名知意）。名字一样的单选框分为一组，同组只能选择一个！！！**

```html
<label>单选框：</label><input type="radio" name="gender">男<input type="radio" name="gender">女<br>
```

如果想要设置默认选择则必须添加checked属性值，页面打开后就会默认选中一个选项

**注意：如果添加了多个checked属性值，默认选中最后的（背后是代码覆盖问题，后的覆盖前的）！！！**

```html
<label>单选框：</label><input type="radio" name="gender" >男<input type="radio" name="gender" checked>女<br>
```

![](https://i-blog.csdnimg.cn/blog_migrate/a3b9540af197eb76495dacb769d969d9.png#pic_center)

#### 多选框 checkbox

和单选框一样，如果想要设置默认选中需要添加checked属性值

```html
<label>多选框：</lable><input type="checkbox" checked></label><br>
```

![](https://i-blog.csdnimg.cn/blog_migrate/a069b0129ff5ec2a1b6841d1af2017fe.png#pic_center)

#### 上传文件 file

系统默认一次只能选择一个文件，如果想要一次选择多个文件，则必须添加multiple属性值

```html
<label>上传文件：</lable><input type="file" multiple></label><br>
```

![](https://i-blog.csdnimg.cn/blog_migrate/0ea36b8520cea878ddaaf2e5ba75bffd.png#pic_center)

### 下拉菜单标签`<select></select>`

**注意： 如果需要设置默认选中，则需要添加selected属性值！！！**

（或者直接把需要默认选中的一个选项放在第一个显示也可以）

如果设置多个selected属性值，默认选中最后的（背后是代码覆盖问题，后的覆盖前的）

```html
<h1>下拉框标签示例</h1>
    <select name="" id="">
    <!--<select></select>表示下拉菜单整体-->    
    <!--id和name属性暂时不要求掌握-->
        <option value="">请选择</option>
        <option value="">宁波</option>
        <option value="">温州</option>
        <!--<option></option>是下拉菜单的每一项-->
        <option value="">杭州</option>
        <option value="">绍兴</option>
        <option value="">湖州</option>
        <!--<option value="" selected>湖州</option>-->
        <option value="">金华</option>
        <option value="">衢州</option>
        <option value="">舟山</option>
    </select>
```

value的作用：（等学到JS再要求掌握，初学可以不写这个参数，简单点来说就是有后台的时候用来发送数据用的）

- 预先填充表单中的字段值，方便用户进行编辑或提供默认值。
- 方便以后以将这些值传递给服务器进行处理。

### 文本域标签`<textarea></textarea>`

**注意：实际开发时，应该禁用右下角的拖拽功能！！！**

```html
<label>评论：<br></label>
    <textarea name="" id="" cols="30" rows="10">默认提示文字</textarea>
```

参数解释：

name和id参数用来发送数据

cols（column列）和rows（row行）用来设置文本框尺寸

**注意：当文本超过文本域一行能容纳的字符数时可以实现自动换行！！！**

### label标签`<label></label>`

![](https://i-blog.csdnimg.cn/blog_migrate/76e95c76147fefe3f3adac8c2bf3ad78.png#pic_center)

解释：label标签其实就是标签的说明文本

作用：用label标签绑定文字和表单控件的关系，增大表单控件的点击范围

运用范围：文本框、密码框、文件、单选框、多选框、下拉菜单、文本域等

```html
<label>用户名：<input type="text" placeholder="请输入用户名"></label>
<label>密码：<input type="password" placeholder="请输入密码"></label>
<!--还有一种不常用写法，需要用到id和for属性：-->
<!--注意：千万不要弄混了name和id的作用！！！-->
<input type="radio" name="gender" id="man">
<label for="man">男</label>
```

![](https://i-blog.csdnimg.cn/blog_migrate/67995b2b7130b9dc7905f4194e02dfd7.gif#pic_center)

### 按钮标签`<button></button>`

```html
<form>
	<button type="submit">提交</button>
	<button type="reset">重置</button>
	<button type="button">普通按钮</button>
	<button type="button" disabled>普通按钮</button>
    <!--disabled：表示禁用该按钮-->
</form>
```

| type属性值 |                            说明                             |
| :--------: | :---------------------------------------------------------: |
|   submit   | 提交按钮，点击后可以提交数据到后台（默认功能不用写type=""） |
|   reset    |            重置按钮，点击后将表单控件恢复默认值             |
|   button   |           普通按钮，默认没有功能，一般配合JS使用            |

## 十五.无语义的布局标签`<div></div>` & `<span></span>`

无语义标签就是没有特定含义，可以用在各种场景

作用：布局网页，划分网页区域和摆放内容

### div 标签（大盒子）

division 的缩写，含义是分割，默认是独占一行，称为块级元素

用于定义文档中的分区或节，通常用于布局和样式化。

```html
<div>
    <h1>Title 1</h1>
    <p>content</p>
</div>

<div>
    <h1>Title 2</h1>
    <p>content</p>
</div>
```

### span 标签（小盒子）

含义是跨度，默认是不独占一行，称为行内元素

标签用于对文本的一部分进行分组，通常用于样式化。

```html
<div>
    <span>龙曜</span>
    <span>龙曜</span>
    <span>龙曜</span>
</div>
<div>
    <span>奥丁</span>
    <span>奥丁</span>
    <span>奥丁</span>
</div>
<div>
    <span>猫校长</span>
    <span>猫校长</span>
    <span>猫校长</span>
</div>
```

![](https://i-blog.csdnimg.cn/blog_migrate/5f51cc0dabdfc28f504fcaaf8cd3d07d.png)

## 十六.字符实体

|  含义  | 字符（分号别忘） |
| :----: | :--------------: |
|  空格  |     &nbsp；      |
| 小于号 |      &lt；       |
| 大于号 |      &gt；       |



# CSS（于2025.1.1更新）

> Css (层叠样式表)是种格式化网页的标准方式， 用于控制设置网页的样式，并且允许CSS样式信息与网页内容(由HTML语言定义)分离的一种技术。
>
> 优势如下
>
> - 格式和结构分离：有利于格式的重用以及网页的修改与维护。
> - 精确控制页面布局：对网页实现更加精确的控制，如网页的布局，字体，颜色，背景等。
> - 实现多个网页同时更新。

## 一.CSS引入方式

### 内部样式表（学习使用）

将CSS代码写在style标签中，head标签内部，title标签下面

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        p {
            color: red;
            font-size: 12px;
        }
        .red {
            color: red;
        }
    </style>
</head>

<body>
    <p>我要变红色</p>
    <div class="red">我也想变红色</div>
</body>

</html>
```

### 外部样式表（开发使用）

将CSS代码写在单独的CSS文件中（.css）

在HTML中使用link标签引入

引用的位置和style标签的位置相同，但不需要style标签

```html
<link rel="stylesheet" href="对应的URL或者路径">
/*rel 关系   stylesheet 样式表*/
```

### 行内样式表格（配合JS使用）

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <!-- 行内样式表 修改样式简单的时候-->
    <p style="color: red;font-size : 20px;">给我一个粉红色的回忆</p>
</body>
    
</html>
```

## 二.选择器的引用

### 标签选择器

缺点：无法差异化同名标签的样式

```HTML
<style>
    p {
        color:red;
        font-size:40px;
    }
</style>

<p>欢迎来到星斗大森林</p>
```

**实际开发中，尽量避免直接用标签选择器，不然对网页里所有相同标签的内容都会生效造成混乱，建议多用复合选择器和后代关系，直接选中对应的标签。**

### 类选择器

特点：差异化设置同名标签的样式，一个类选择器可以给多个标签使用

注意：一个标签可以使用多个类名，class属性值写多个类名即可，类名中间用空格隔开

```html
<!--后选择-->
<style>
    .basic {
        color:red;
        font-size:40px;
    }
    .style {
        font.family：font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    }
</style>
<!--先定义-->
<div class="basic style">欢迎来到星斗大森林</div>
<!--多类名的使用-->
```

大括号内遵循以下书写规则

属性名：属性值；（一个键值对）

### id选择器

和类选择器的效果一样，一般配合JS使用，很少用来设置CSS样式

同一个id选择器在一个页面只能使用一次

id选择器权重最大，被多个选择器选中的话，后者代码控制前者代码

id选择器的口诀：样式#定义，结构id调用，只能调用一次，别人切勿使用 

```html
<style>
    #pink {
        color: pink;
    }
</style>

<div id="pink">迈克尔杰克逊</div>
```

### 通配符选择器

*。不需要调用，浏览器自动查找页面所有的标签，设置相同的形式

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      * {
        color: red;
        font-size: 12px;
      }

      /* * 这里把html body div span li都改成红色 */
    </style>
  </head>

  <body>
    <div>红色</div>
  </body>
</html>
```

### 复合选择器

由两个或者多个基础选择器通过不同的方式组合而成

#### 后代选择器

选中某元素的所有后代元素（包含儿子，孙子，重孙子......）

写法：

父选择器 子选择器 {CSS属性}

父子选择器用空格隔开 

#### 子代选择器

选中某元素的子代元素（最近的子级）

写法：

父选择器>子选择器 {CSS属性}

父子选择器中用大于号隔开

#### 并集选择器

选中多组标签设置相同的格式

写法：

选择器1，选择器2，...，选择器N {CSS属性}

#### 交集选择器

写法：

选择器1选择器2 {CSS属性}

选择器之间连写，没有任何符号

如果交集选择器中有标签选择器，标签选择器必须书写在最前面

### 伪类选择器

伪类表示元素状态，选中元素的某个状态设置样式

任何标签都可以设置手表悬停状态

鼠标悬停状态：

选择器：hover{CSS属性}

#### 伪类-超链接

| 选择器   | 作用                               |
| -------- | ---------------------------------- |
| :link    | 访问前的状态                       |
| :visited | 访问后的状态（默认样式显示为紫色） |
| :hover   | 鼠标悬停状态                       |
| :active  | 点击时（激活）                     |

如果要给超链接设置以上四个状态，需要按照LVHA的顺序书写

实际工作中，其实只需要用a标签选择器设置超链接的样式，hover状态特殊设置

### 结构伪类选择器

作用：根据元素的结构关系查找元素

|     选择器     |                说明                |
| :------------: | :--------------------------------: |
| E:first-child  |          查找第一个E元素           |
|  E:last-child  |         查找最后一个E元素          |
| E:nth-child(N) | 查找第N个E元素（第一个元素N值为1） |

#### E:nth-child(公式)写法：

|         功能         |    公式    |
| :------------------: | :--------: |
|       偶数标签       |     2n     |
|       奇数标签       | 2n+1；2n-1 |
|  找到五的倍数的标签  |     5n     |
| 找到第五个以后的标签 |    n+5     |
| 找到第五个以前的标签 |    -n-5    |

### 伪元素选择器

作用：创建虚拟元素（伪元素），**用来摆放装饰性的内容**

|  选择器   |              说明               |
| :-------: | :-----------------------------: |
| E::before | 在E元素里面最前面添加一个伪元素 |
| E::after  | 在E元素里面最后面添加一个伪元素 |

注意点：

- 必须设置content:" "属性，用来设置伪元素的内容，如果没有内容，则引号留空即可
- 没写content:" "属性，伪元素选择器中的所有内容都不生效
- 伪元素默认是行内显示模式
- 权重和标签选择器相同

## 三.画盒子

其实本质就是，div标签独占一行，有自己的宽高。

我们所做的，就是把这个标签的宽高改变，然后加上背景颜色，这样就是一个盒子了。

涉及到的属性为width，height，background-color

width是盒子的宽，单位是px。

height是盒子的高，单位也是px。

background-color是背景色，直接写颜色名字就好了。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .red {
            width: 100px;
            height: 100px;
            background-color: brown;
        }
 
        .orange {
            width: 200px;
            height: 200px;
            background-color: orange;
        }
    </style>
</head>
<body>
    <div class="red">div1</div>
    <div class="orange">div2</div>
</body>

```

**注：在开发时，为了网页加载更快，一般CSS书写顺序为：**

1. **盒子模型属性**
2. **文字样式**
3. **圆角，阴影等修饰属性**

## 四.文字控制属性

### 字体大小 font-size

pc端最常用的单位是px（像素），单位不打该属性不生效。

谷歌浏览器默认字体大小为16px（要记 有用）

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body {
            font-size: 20px;
        }

        /* 标题标签比较特殊，需要单独指定文字大小 */
        h2 {
            font-size: 20px;
        }
    </style>
</head>

<body>
    <h2>pink老师的秘密</h2>
    <p>那一抹众人中最漂亮的颜色</p>
    <p>优雅淡然又那么心中清澈</p>
    <p>前端总是伴随的困难和犯错</p>
    <p>静心淡然功克一个又一个</p>
    <p>拼死也要克服它</p>
    <p>这是pink老师的秘密也是老师最终的嘱托</p>
</body>
```

### 字体粗细 font-weight

两种属性值写法：

1. 数字型（实际开发中，我们更提倡使用数字）

   400正常  700加粗

2. 关键字

   normal正常  bold加粗

**注意点**

- font-weight: bold;   等价于   font-weight: 700;

- font-weight: 400;

​        /* 只变大不变粗 写了跟没写一样 */

- 400这个数值是分水岭。
- 这里的数字都莫得单位

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      .bold {
        font-weight: 700;
      }

      h2 {
        font-weight: 400;
      }
        
      .bold1 {
        font-weight: 400;
      }
    </style>
  </head>

  <body>
    <h2>pink老师的秘密</h2>
    <p>那一抹众人中最漂亮的颜色</p>
    <p>优雅淡然又那么心中清澈</p>
    <p class="bold1">前端总是伴随的困难和犯错</p>
    <p>静心淡然功克一个又一个</p>
    <p class="bold">拼死也要克服它</p>
    <p>这是pink老师的秘密也是老师最终的嘱托</p>
  </body>
</html>
```

### 字体风格（倾斜） font-style

属性值：

normal正常       italic 倾斜

italic不常用，在css中使用字体倾斜属性的目的是为了清除原标签的文字显示效果

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      p {
        font-style: italic;
      }

      /* 让倾斜的字体不倾斜 */
      em {
        font-style: normal;
      }
    </style>
  </head>

  <body>
    <p>同学上课时候的你</p>
    <em>下课时候的你</em>
  </body>
</html>
```

### 字体颜色 color

|                 表示方式                 |                        属性值                        |
| :--------------------------------------: | :--------------------------------------------------: |
|        预定义的颜色值（学习测试）        |                red，green，blue......                |
| 十六进制（开发中最常用）（从设计稿复制） |            #FF6600（简写：#F60），#29D794            |
|             RGB代码（了解）              |            rgb(255,0,0)或rgb(100%,0%,0%)             |
|         rgba表示法（实现透明色）         | rgba(r,g,b,a) 其中a表示透明度，取值0-1（可以取小数） |

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div {
            /* color: pink; */
            color: #3700ff;
            /* color: rgb(rgb(0, 255, 119), rgb(52, 120, 101), rgb(7, 7, 70)); */
        }
    </style>
</head>

<body>
    <div>听说喜欢pink颜色的男人都是喜欢男人</div>
</body>

</html>
```

### 字体行高（行间距） line-height

行高的测量方法：从一行文字的最顶端（最底端）量到下一行文字的最顶端（最底端）

两种属性值写法：

1. 数字+px

2. 数字（当前标签font-size属性值的倍数）

   （谷歌浏览器默认字体大小为16px）

**行高应用：垂直居中**

**方法：行高属性值等于盒子高度属性值即可，但只适用于单行文字**

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div {
            line-height: 16px;
        }

        .height {
            line-height: 25px;
        }
        
        .height1 {
            line-height:2;
            /*如果来谷歌浏览器打开的话 这句话的功能等价于 line-height：32px*/
        }
    </style>
</head>

<body>
    <div>中国人</div>
    <p class="height">打开北京、上海与广州的地铁地图,你会看见三张纵横交错的线路网络,这代表了中国最成熱的三套
        城市轨道交通系统。</p>
    <p class="height1">可即使这样,在北上广生活的人依然少不了对地铁的抱怨,其中谈及最多的问题便是拥挤一对很多人
        而言,每次挤地铁的过程,都像是一场硬仗。更何况,还都是败仗居多。</p>
    <p>那么,当越来越多的二线甚至三线城市迎接来了自己的地铁,中国哪里的地铁是最拥挤的呢?</p>
</body>

</html>
```

### 字体族 font-family

属性值：字体名

拓展：font-family属性值可以写多个字体名，各个字体名用逗号隔开，执行顺序是从左向右依次查找

font-family属性最后设置一个字体族名，网页开发建议使用无衬线字体。（衬线字体带有修饰，无衬线字体看起来更加规整）

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      h2 {
        font-family: "微软雅黑";
      }

      p {
        font-family: "Microsoft YaHei", Arial, Helvetica, sans-serif;
          /*sans-serif 无衬线字体*/
      }
    </style>
  </head>

  <body>
    <h2>pink老师的秘密</h2>
    <p>那一抹众人中最漂亮的颜色</p>
    <p>优雅淡然又那么心中清澈</p>
    <p>前端总是伴随的困难和犯错</p>
    <p>静心淡然功克一个又一个</p>
    <p>拼死也要克服它</p>
    <p>这是pink老师的秘密也是老师最终的嘱托</p>
  </body>
</html>
```

### 文本对齐 text-align

属性值：

- left  左对齐（默认）

- **center  居中对齐**（Emmet：tac）

- right  右对齐

**文本对齐的本质：居中的是文字内容而不是标签**

在了解text-align的本质是控制内容的对齐方式之后，不仅可以实现文字居中，也可以令其他标签所显示的内容居中，只需要将需要居中的内容放置在盒子中，并给盒子添加文本对齐属性即可（原则：属性设置给内容的父级）

**注意：text-align对块元素不起作用，但会发生继承，对块元素里面的文本等内容起作用！！！**

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      * {
        margin: 0;
        padding: 0;
      }
      p {
        text-align: center;
        line-height: 200px;
        display: block;
      }
      div {
        height: 200px;
        width: 100%;
        border: 1px solid black;
      }
    </style>
  </head>

  <body>
    <div>
      <p>你好ss</p>
      <img src="./images/1.jpg" alt="">
    </div>
  </body>
    
</html>
```

### 装饰文本（修饰线） text-decoration

|    属性值    |       效果       |
| :----------: | :--------------: |
|     none     | 无（去掉修饰线） |
|  underline   |      下划线      |
| line-through |      删除线      |
|   overline   |      上划线      |

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div{
            text-decoration: underline;
        }
 
        p{
            text-decoration: line-through;
        }
        h2{
            text-decoration: overline;
        }
        a{
            text-decoration: none;
        }
    </style>
</head>
<body>
    <div>div</div>
    <p>ppp</p>
    <h2>h2</h2>
    <a href="#">我是超链接,点呀</a>
</body>
</html>
```

### 文本缩进 text-indent

使用场景：新闻，文章的段落开头缩进

属性值：

- 数字 + px

- **数字 + em**（更加常用）  （1em = 当前标签的字号大小）

  ```html
  <!DOCTYPE html>
  <html lang="en">
  
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Document</title>
      <style>
          /* em是相对于font-size的1给字体 */
          p {
              text-indent: 2em;
              font-size: large;
          }
      </style>
  </head>
  
  <body>
      <p>打开北京、上海与广州的地铁地图,你会看见三张纵横交错的线路网络,这代表了中国最成熱的三套
          城市轨道交通系统。</p>
      <p>可即使这样,在北上广生活的人依然少不了对地铁的抱怨,其中谈及最多的问题便是拥挤一对很多人
          而言,每次挤地铁的过程,都像是一场硬仗。更何况,还都是败仗居多。</p>
      <p>那么,当越来越多的二线甚至三线城市迎接来了自己的地铁,中国哪里的地铁是最拥挤的呢?</p>
  </body>
  
  </html>
  ```

### 字体复合属性 font

使用场景：设置网页文字公共样式（网页搭建的前期对所有的标签生效，后续需要特殊化处理时再用选择器单独修改）

font:是否倾斜 是否加粗 字号/行高 字体  （必须按照顺序书写）

**注意：字号和字体值必须书写，否则font属性不生效**

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width">
    <title>Document</title>
    <style>
        div {
            font-style: italic;
            font-weight: 700;
            font-family: "MSYH";
            font-size: 16px;
            /* 符合属性有要求 */
            /* font: font-style font-weight font-size/line-height font-family; */
            font: italic 700 16px/2 "MSYH";
            font: 20px "MSYH";
        }
    </style>
</head>

<body>
    <div>三生三世十里桃花,一心一意百行代码</div>
</body>

</html>
```

这些代码可以从其他网页中截取，不需要自己写

## 五.CSS特性

### 继承性

子级默认继承父级的文字控制属性

注意：如果子级中的标签自己有样式，则生效自己的样式，不继承

### 层叠性

对相同的标签设置多组不同的CSS属性时

相同的属性会覆盖：后面的CSS属性覆盖前面的CSS标签

相同的属性会叠加

### 优先级

#### 选择器生效优先级

规则：选择器优先级高的样式生效，与代码的先后没有关系

公式：通配符选择器<标签选择器<类选择器<id选择器<行内样式<！important

**（选中标签的范围越大，优先级越低）**

！important代表提权功能，用来提高权重/优先级到最高，实际开发中，慎用！！！

#### 叠加计算规则

如果是复合选择器，则需要权重叠加计算

公式：（行内样式，id选择器个数，类选择器个数，标签选择器个数）

每一级之间不存在进位

规则：

- 从左向右依次比较选个数，同一级个数多的优先级高，如果个数相同，则向后比较
- ！important权重最高
- 继承权权重最低
- 如果某标签的CSS属性带有！important，但却发生了继承关系，仍然是权重最低的

步骤：

1.观察标签内有无！important

2.判断有无发生继承（选择器是否选择到了文字所在的标签）

3.排除两种特殊情况后，按照公式进行比较即可

## 六.Emmet写法

代码的简写方式，输入缩写VScode会自动生成对应的代码

### HTML

|     说明     |                   标签结构                   |    Emmet    |
| :----------: | :------------------------------------------: | :---------: |
|   类选择器   |          `<div class="box"></div>`           | 标签名.类名 |
|   id选择器   |            `<div id="box"></div>`            | 标签名#id名 |
|   同级标签   |             `<div></div><p></p>`             |    div+p    |
|  父子级标签  |             `<div><p></p></div>`             |    div>p    |
| 多个相同标签 | `<span>1</span><span>2</span><span>3</span>` |   span*3    |
| 有内容的标签 |              `<div>内容</div>`               |  div{内容}  |

### CSS

大多数简写方式为属性单词的首字母

w500+h200+bgc#fff

| Emmet |        含义         |
| :---: | :-----------------: |
| tac： | text-align: center; |
|       |                     |
|       |                     |

## 七.背景属性

该小节的所有属性使用之前都必须划定一个盒子

### 背景色 background-color

在画盒子那节里面有介绍

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div {
            width: 200px;
            height: 200px;
            /* background-color: transparent; 透明的 */
            background-color: pink;

        }
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

### 背景图 background-image

网页中使用背景图实现装饰性的图片效果

属性名：background-image（Emmet：bgi）

属性值：url（背景图url）

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* 背景图片用于常见的logo或者一些装饰性的小图片
        或者是超大的背景图片，优点是非常便于控制位置 */
        div {
            width: 300px;
            height: 300px;
            /* 必须要加url */
            background-image: url(img.jpg);
            /*背景图默认效果为平铺 大小不够会将照片复制*/
        }
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

### 背景图平铺方式 background-repeat

属性名：background-repeat（Emmet：bgr）

属性值：

|  属性值   |             说明             |
| :-------: | :--------------------------: |
| no-repeat | 不平铺（贴着左上角显示图片） |
|  repeat   |       平铺（默认效果）       |
| repeat-x  |         水平方向平铺         |
| repeat-y  |         垂直方向平铺         |

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div {
            width: 300px;
            height: 300px;
            background-image: url(img.jpg);
            background-repeat:no-repeat ;
            /* 页面元素可以添加背景颜色也可以添加背景图片 */
            /* 只不过背景图片压住背景颜色 */
        }
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

### 背景图位置 background-position

属性名：background-position（Emmet：bgp）

属性值：水平方向位置 垂直方向位置  

表示方法一：

关键字：

| 关键字 | 位置 |
| :----: | :--: |
|  left  | 左侧 |
| right  | 右侧 |
| center | 居中 |
|  top   | 顶部 |
| bottom | 底部 |

表示方法二：

坐标：数字+px，正负都可以（如果是0 0的话是不需要加单位的）（0 0就是左上角的意思）

**注意：两种方式可以混用！！！**

注意：关键字取值方式写法，可以颠倒取值顺序

注意：只写一个关键字，另一个方向默认居中，数字只写一个值表示水平方向，垂直方向默认为居中

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div {
            width: 300px;
            height: 300px;
            background-color: pink;
            /*画盒子*/
            background-image: url(logo.jpg);
            background-repeat: no-repeat;
            /*设置不平铺，默认是平铺*/
            
            background-position: 20px 50px;
            /* 20px是指图片距离左侧，50px是图片距离上边 */
            /*正数向右向下移动，负数向左向上移动*/
            background-position：bottom left；
            /*等效于background-position：left bottom；*/
            /* position top/center/bottom/left/center/right 方位名词 */
            /* 两个都是方位词，前后顺序没有关系 */
            
            /* length 百分数，由浮点数或者单位标识符组成的长度值 精准单位 */
            
            /* 垂直居中 */
            /* background-position: top; */
            /* 水平居右 */
            /*background-position: right;*/
            /* 只有一个参数的前提下，如果该参数是水平方向的方位名词，则省略的就是垂直的，反之同理 */
            /* 如果是精准单位参数，只可能是水平方向上的 */
        }
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

### 背景图缩放 background-size

作用：设置背景图大小

属性名：background-size（Emmet：bgz）

常用属性值：

方法一：关键字写法

| 关键字  | 说明                                                       |
| ------- | ---------------------------------------------------------- |
| cover   | 等比例缩放背景图片以完全覆盖背景区，可能背景图片部分看不见 |
| contain | 等比例缩放背景图片以完全装入背景区，可能背景区部分空白     |

**注意：contain关键字使用时，如果图的宽高跟盒子尺寸相等则停止缩放，可能导致盒子有露白！！！而cover是保证全部填满盒子，不保证长宽都能适应盒子，可能导致部分图片的长或者宽超出盒子尺寸范围！！！**

方法二：数字%

根据盒子尺寸计算图片大小

**注意：background-size：100%：总是x轴百分百铺满整个容器，y轴可能被剪裁或者出现填不满的部分，图片不变形！！！（等比例缩放）**

方法三：数字+单位（px）（不常用）

**注意：在实际开发中，盒子的尺寸和图片的尺寸一般是匹配的，在这种情况下，cover，contain，100%的效果是相同的！！！**

### 背景图固定 background-attachment

作用：背景不会随着元素的内容滚动

属性名：background-attachment（Emmet：bga）

属性值：

fixed 固定  scoll 滑动

默认是滑动的 

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body {
            background-image: url(img.jpg);
            background-repeat: no-repeat;
            background-position: center top;
            background-attachment: fixed; 
        }
    </style>
</head>

<body>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
    <p>天王盖地虎，pink老师一米五</p>
</body>

</html>
```

### 背景符合属性 background

属性名：background（Emmet：bg）

属性值：背景颜色 背景图片地址 背景平铺 背景图位置/背景图缩放 （背景图像固定）

**注意：空格隔开每个属性值，不区分顺序！！！**

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body {
            background: black url(img.jpg) no-repeat fixed center top;
        }
    </style>
</head>

<body>
    <p>测试背景复合属性</p>
</body>

</html>
```

### 透明度 opacity

作用：设置整个元素的透明度（包含背景和内容）

属性值：0-1

- 0：完全透明（元素不可见）
- 1：不透明（完全可见）
- 0-1之间的小数：半透明

### 光标类型 cursor

作用：鼠标悬停在元素上时指针显示样式

属性值：

| 属性值  |             效果             |
| :-----: | :--------------------------: |
| default |      默认值，通常是箭头      |
| pointer |  小手效果，提示用户可以点击  |
|  text   | 工字形，提示用户可以选择文字 |
|  move   |  十字光标，提示用户可以移动  |



## 八.显示模式

### 块级元素 block

独占一行

宽度默认是父级的100%

添加宽高属性生效

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div {
            /* width: 200px; */
            height: 200px;
            background-color: pink;
        }
    </style>
</head>

<body>
    <!-- h1~h6 p div ul ol li  -->
    <!-- 比较霸道，自己独占一行 -->
    <!-- 高度，宽度，外边距及内边距都控制 -->
    <!-- 宽度默认是容器的100% -->
    <!-- 是一个容器及盒子，里面放行内或者块级元素 -->
    <div>比较霸道，自己独占一行</div>
</body>

</html>
```

### 行内元素 inline（不常用）

一行共存多个

尺寸由内容撑开

加宽高属性不生效

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <!-- 相邻行内元素在一行上.一行可以显示多个 -->
    <!-- 高度和宽度设置是无效的 -->
    <!-- 默认宽度是本身内容宽度 -->
    <!-- 行内宽度可以容纳文本和其他行内元素 -->
    <span>pink老师</span> <strong>品如的衣服</strong>
    <!-- a里面可以放块级元素但是转换一下最安全 -->
</body>

</html>
```

### 行内块元素 inline-block

一行共存多个

默认尺寸由内容撑开

加宽高生效

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>

  <body>
    <img src="" alt="" />
    <td></td>
    <input type="text" />
    <!-- 行内块元素，可以设置宽度，一行放多个 -->
  </body>
</html>
```

### 转换显示模式

属性名：display

属性值：

|      属性值      |   效果   |
| :--------------: | :------: |
|      block       |   块级   |
|   inline-block   |  行内块  |
| inline（不常用） |   行内   |
|       flex       | 弹性盒子 |
|       grid       |  抽屉型  |

### 标准流

标准流又叫文档流，指的是标签在页面中默认的排布规则。

例如前面讲到的：块元素独占一行，行内元素一行可以显示多个

### float浮动（了解）

因为对于div标签独占整行的特点，我们需要对这些盒子的位置重排，实现布局效果

而浮动的本质作用是实现图文混排效果

#### 基本使用与布局

浮动属性float，left表示左浮动，right表示右浮动

一般在css中放在文字属性之前提高加载效率

**特点**

- 浮动后的盒子顶对齐，同时该盒子具备行内块特点

- 父级宽度不够，浮动的子级会换行

- **浮动后的盒子脱标（不再占用标准流的位置，脱离标准流的控制，浏览器眼中脱标的盒子不存在）**

  **因此，对于一个父级下的几个盒子需要布局的情况，如果一个盒子设置了浮动，那么所有盒子都要设置浮动**

#### 清除浮动

情况：子级浮动，父级无法撑开父级高度，影响布局效果

**方法：**

- 单伪元素法

```css
.clearfix::after {
    /*在父元素内容的最后添加一个块级元素，本质原理和额外标签法相同*/
    content:"";
    /*不加这句伪元素选择器不生效*/
    display:block;
    /*变成块级元素*/
    clear:both;
}
```

- 额外标签法

  在父元素内容的最后添加一个块级元素，设置CSS属性clear：both

- 双伪元素法（推荐）

```css
.clearfix::before,
/*before解决外边距塌陷问题*/
.clearfix::after {
	content:"";
    display:table;
}
.clearfix::after {
    clear:both;
}
```

- overflow属性

  父元素添加CSS属性 overflow：hidden即可

### flex弹性布局（重点）

**flex弹性布局介绍：**

- 弹性布局是一种现代的CSS布局方式，是浏览器提倡的布局模型，非常适合结构化布局，提供了强大的空间分布能力和对齐能力。
- Flex模型不会产生浮动布局中脱标现象，布局网页更简单更灵活。
- 通过使用display: flex属性来创建一个弹性容器，并在其中使用灵活的盒子模型来进行元素的排列和定位。

**设置方式**：

给父元素设置display：flex（Emmat：df），子元素可以自动挤压或拉伸

**组成部分：**

- 弹性容器（父级）
- 弹性盒子（子级）
- 主轴
- 侧轴/交叉轴

**弹性布局具有以下特点：**

- 主轴与交叉轴：弹性容器具有主轴（main axis）和交叉轴（cross axis）。

  **默认情况下，主轴是水平方向，交叉轴是垂直方向。**

- 弹性容器：通过将父元素的display属性设置为flex或inline-flex来创建弹性容器。

- 子元素的弹性项目（弹性盒子）：弹性容器中的每个子元素都成为弹性项目（弹性盒子）。

  弹性盒子默认沿着主轴方向排列。

  弹性盒子可以指定各自在主轴和交叉轴上的大小、顺序以及对齐方式等。

  子元素拥有自动挤压拉伸的特性

- 主轴对齐：弹性项目可以在主轴上按照一定比例分配空间，也可以使用justify-content属性定义主轴的对齐方式。

- 交叉轴对齐：弹性项目可以在交叉轴上进行对齐，包括顶部对齐、底部对齐、居中对齐等，使用align-items属性定义交叉轴对齐方式。

- 换行与自动调整：可控制弹性项目是否换行，并且具备自动调整元素大小的能力。

#### 主轴与交叉轴对齐方式

##### 主轴 justify-content

```css
.box {
  justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
}
```

- flex-start（默认值）：左对齐（）
- flex-end：右对齐
- center： 居中
- space-between：两端对齐，项目之间的间隔都相等。（空白间距均分布在弹性盒子之间，原理是将父级剩余的尺寸分配成间距）
- space-around：每个项目两侧的间隔相等，盒子之间的间隔比盒子与边框的间隔大一倍。（空白间距均分布在弹性盒子两侧）
- space-evenly：弹性盒子与容器之间的间距相等。（各个间距严格相等，between和around融合版本）

![](https://i-blog.csdnimg.cn/blog_migrate/e29a1dc5985667b5bf1c4bfdc868a5bf.png)

##### 交叉轴 align-items&align-self

```css
.box {
  align-items: flex-start | flex-end | center | baseline | stretch;
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}
```

- align-items：当前弹性容器内所有的弹性盒子的侧轴对齐方式，是弹性容器的属性。
- align-self：单独控制某个弹性盒子的侧轴对齐方式，是弹性盒子的属性。
- flex-start：交叉轴的起点对齐。
- flex-end：交叉轴的终点对齐。
- center：交叉轴的中点对齐。
- baseline: 项目的第一行文字的基线对齐。（不常用）
- stretch（默认值）：如果盒子未设置高度或设为auto，将占满整个容器的高度。
- auto：令盒子高度拉伸至占满容器

注：align-self属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch。

![](https://i-blog.csdnimg.cn/blog_migrate/2117d67e94a6ca317b307907fd115fdb.png)

![](https://i-blog.csdnimg.cn/blog_migrate/f7252f9d1ee1f045c7e4ee311c8b6db7.png)

#### 修改主轴方向 flex-direction

注意：当主轴发生变化时，侧轴会自动变换。

```css
.box {
  flex-direction: row | row-reverse | column | column-reverse;
}
```

- row（默认值）：主轴为水平方向，从左到右。
- row-reverse：主轴为水平方向，从右到左。
- **（重点）column：主轴为垂直方向，从上到下**
- column-reverse：主轴为垂直方向，从下到上。

![](https://i-blog.csdnimg.cn/blog_migrate/34fdff162c84ce7295e8cd7e4b5b5308.png)

#### 弹性伸缩比

##### flex属性

作用：控制弹性盒子的主轴方向的尺寸

属性值：整数数字，表示占用父级剩余尺寸的份数

默认情况下，主轴方向尺寸是靠内容撑开，侧轴在没有设置高度的情况下默认拉伸

> flex属性是flex-grow, flex-shrink 和 flex-basis的简写，默认值为0 1 auto。后两个属性可选。
>
> 该属性有两个快捷值：auto (1 1 auto) 和 none (0 0 auto)。
>
> 建议优先使用这个属性，而不是单独写三个分离的属性，因为浏览器会推算相关值。

#### 弹性换行与行对齐方式

##### 弹性换行 flex-wrap

弹性盒子可自动挤压或拉伸，默认情况下，所有弹性盒子都在一行显示

```css
.box{
  flex-wrap: nowrap | wrap | wrap-reverse;
}
```

- nowrap（默认）：不换行
- wrap：换行，第一行在上方。
- wrap-reverse：换行，第一行在下方。（不常用）

![](https://i-blog.csdnimg.cn/blog_migrate/abf2d8c36fcd14743b61926fb9e930b6.png)

#####  行对齐方式 align-content

align-content属性值和功能和主轴对齐方式一模一样，可以简便记忆。

**注：align-content属性对单行弹性盒子不生效。**

```css
.box {
  align-content: flex-start | flex-end | center | space-between | space-around | stretch;
}
```

- flex-start：与交叉轴的起点对齐。
- flex-end：与交叉轴的终点对齐。
- center：与交叉轴的中点对齐。
- space-between：与交叉轴两端对齐，轴线之间的间隔平均分布。
- space-around：每根轴线两侧的间隔都相等，轴线之间的间隔比轴线与边框的间隔大一倍。
- space-evenly：轴线之间的间隔和轴线与边框的间隔都相等。（无代码提示）
- stretch（默认值）：轴线占满整个交叉轴。

![](https://i-blog.csdnimg.cn/blog_migrate/566719964e7f24336a0b478dab2f8fef.png)

##### order属性（了解即可）

order属性定义项目的排列顺序。数值越小，排列越靠前，默认为0。

```css
.item {
  order: <integer>;
}
```

![](https://i-blog.csdnimg.cn/blog_migrate/8536f76875395248b53a0d8eb8d2900e.png)

#### 垂直对齐方式 vertical-align

谁高度大给谁加属性

|  属性值  |           效果           |
| :------: | :----------------------: |
| baseline |         基线对齐         |
|   top    | 顶部对齐，最高内容的顶部 |
|  middle  |         居中对齐         |
|  bottom  | 底部对齐，最高内容的底部 |

##### 基线的概念

行内块、行内标签当成文字处理，在浏览器中默认所有的文字都按基线对齐。

由于有些英文字母的书写需要到基线以下位置，比如p，所以会在基线以下部分留出一小块空白间距。

把显示模式转成块级元素或者使用vertical-align属性可以间接消除这一小块空白间距。

![Snipaste_2025-01-01_21-16-01](C:\Users\Lenovo\Desktop\Snipaste_2025-01-01_21-16-01.png)

#### 定位 position

作用：灵活的改变盒子在网页中的位置

实现方式：

1. position：定位模式

2. 边偏移：设置盒子的位置，属性值如下

   - left

   - right

   - top

   - bottom

##### 定位模式之相对定位 relative（单独使用的情况较少）

特点：

- **改变位置的参照物是自己原来的位置**

- 不脱标，占位

##### 定位模式之绝对定位 absolute

使用场景：子级绝对定位，父级相对定位（子绝父相）

特点：

- 脱标不占位
- 参照物的判定为**先找最近的已经定位的祖先元素**，如果所有祖先元素都没有定位，**参照浏览器可视区改位置**
- 显示模式特点改变，行内元素会变为行内块元素，具备行内块元素的所有特点

#### 定位居中 （两种方式）

实现方式：

1. 绝对定位
2. 水平，垂直偏移为50%
3. 子级向左，上移动自身尺寸的一半
   - 左，上的外边距为盒子尺寸的一半
   - transfrom：translate（-50%，-50%）

```css
* {
    position:absolute;
    left:50%;
    top:50%;
    margin-left:/*对应尺寸*/;
    margin-top:/*对应尺寸*/;
    /*transform: translate(-50%, -50%);*/
}
```

#### 固定定位 

场景：**元素的位置在网页滚动时不会改变**

写法：

position: fixed

特点：

1. 脱标，不占位

2. 参照物是浏览器窗口
3. 显示模式具有行内块特点

#### 堆叠层级 z-index

默认效果：按照标签书写顺序，后来者居上

作用：设置定位元素的层级顺序，改变定位元素的显示顺序

写法：

z-index：属性值

注：属性值是整数，默认是0，取值越大显示顺序级别越高。

#### CSS Sprites（CSS精灵）

一种网页图片应用处理方式，把网页中一些背景图片整合到一张图片文件中，再用background-position精确定位出背景图片的位置。

优点：减少服务器被请求次数，减轻服务器的压力，提高页面加载速度。

实现步骤：

1. 创建盒子，盒子尺寸和小图尺寸相同
2. 设置盒子背景图为精灵图 background-image: url(img.jpg);
3. 添加background-position属性，改变背景图位置
   - 使用PxCook测量小图片左上角坐标
   - 取负数坐标为background-position的属性值（向左上移动图片）

## 九.CSS辅助软件

### PxCook（像素大厨）

一款切图设计工具软件。支持PSD文件的文字，颜色，距离自动智能识别。

也可以用figma软件。

两种模式：

- 开发面板（自动智能识别）
- 设计面板（手动测量尺寸和颜色）

## 十.盒子模型

作用：布局网页，摆放盒子和内容

### 盒子模型的组成

- 内容区域：width&height
- 内边距：padding（出现在内容与盒子边缘之间，四个方向都有）（会把盒子撑大）
- 边框线：border（Emmet：bd）

| 属性值 | 线条样式 |
| :----: | :------: |
| solid  |   实线   |
| dotted |   点线   |
| dashed |   虚线   |

属性值：边框线粗细 线条样式 颜色（不区分顺序）

（属性值：1px solid #000 表示1像素的黑色边框细实线）

- 外边距：margin（出现在盒子外面，用于拉开两个盒子之间的距离）

### 盒子模型-边框线 border

允许设置单方向边框线

属性名：border+方位名词（Emmet：bd+方位名词首字母）

（top；bottom；right；left）

属性值：边框线粗细 线条样式 颜色（不区分顺序）

**注意：在开发中，一般属性值个数为1的情况居多，先整体设置，再取消某些方向的边框线！！！**

取消的方法：

```css
border： 1px solid #FFFFFF;
border-left: 0;
border-right: none;
```

### 盒子模型-内边距 padding

作用：设置内容与盒子边缘之间的距离

属性名：padding/padding-方位名词

属性值：数字+px

**注意：padding有多值写法，类似于复合属性！！！**

| 取值个数 |             示例              |              含义              |
| :------: | :---------------------------: | :----------------------------: |
|  一个值  |        padding: 10px;         |          上下左右10px          |
|  四个值  | padding: 10px 20px 30px 40px; | 上10px；右20px；下30px；左40px |
|  三个值  |   padding: 10px 40px 80px;    |    上10px；左右40px；下80px    |
|  两个值  |      padding:10px 80px;       |       上下10px；左右80px       |

记忆方法：从上开始，按顺时针方向转一圈，如果当前方向没有数值，取值跟对面一样。

### 盒子模型-尺寸计算

已知：盒子尺寸=内容尺寸+border尺寸+内边距尺寸

结论：给盒子加border或padding会撑大盒子

解决方法：

- 手动做减法，减去border/padding的尺寸
- 内减模式：box-sizing：border-box（自动去掉撑大的尺寸，之后加padding/border都不会撑大盒子）

### 盒子模型-外边距 margin

作用：拉开两个盒子之间的距离

提示：与padding属性值写法，含义相同

margin属性不会撑大盒子，多值写法和padding属性相同

#### 外边距问题-合并现象

场景：垂直排列的兄弟元素，上下margin会合并

现象：取两个margin中的较大值生效

#### 外边距问题-塌陷现象

场景：父子级的标签，子级添加上外边距标签会产生塌陷问题

现象：导致父级一起向下移动

解决方法：

- **取消子级margin，父级设置padding**

- 父级设置 overflow：hidden

- 父级设置 border-top

  原理：让浏览器找到盒子的正确边缘

#### 行内元素-内外边距问题

场景：行内元素添加margin和padding，无法改变元素垂直位置，只能改变水平位置

解决方法：给行内元素添加line-height可以改变垂直位置

### 盒子模型-圆角 border-radius

作用：设置元素的外边框为圆角

属性值：数字+px/百分比

提示：属性值的数字是圆角半径

#### 多值写法

| 取值个数 |                示例                 |                  含义                  |
| :------: | :---------------------------------: | :------------------------------------: |
|  一个值  |        border-radius: 10px;         |        左上+右上+右下+左下10px         |
|  四个值  | border-radius: 10px 20px 30px 40px; | 左上10px；右上20px；右下30px；左下40px |
|  三个值  |   border-radius: 10px 40px 80px;    |   左上10px；右上+左下40px；右下80px    |
|  两个值  |      border-radius:10px 80px;       |      左上+右下10px；右上+左下80px      |

记忆：从左上角顺时针赋值，没有取值的角与对角取值相同

#### 常见应用

正圆：给正方形盒子设置圆角属性值为宽高的一半/**50%**，百分比写法最大值为50%，超过50%是没有任何效果的

胶囊形：给**长方形盒子**设置圆角属性值为**盒子高度的一半**

### 盒子模型-阴影 box-shadow

作用：给元素设置阴影效果

属性值：X轴偏移量 Y轴偏移量 模糊半径 扩散半径 颜色 内外阴影 

举例：box-shadow: 2px 5px 10px 1px rgba(0,0,0,0.5);

注意：

- 该属性是复合属性，X轴偏移量和Y轴偏移量必须书写
- 内外阴影这个属性默认是外阴影，内阴影需要添加inset

### 版心居中

margin: 0 auto;

前面的数字是上下距离，可以自行设置数值，后面是左右距离，设置为auto，可以自动计算左右两边距离相同，达到版心居中的效果

**注意：版心居中的要求是盒子要有宽度，否则版心居中属性不生效！！！**

### 清除默认样式

有些标签自带样式，在网页开发初期，需要对这些标签统一清楚默认样式，后续再根据设计稿进行修改和美化设计

```css
*{
	margin：0；
	padding：0；
	box-sizing： border-box；
}
li {
    list-style: none;
}
a {
    text-decoration: none;
}
```

### 元素溢出

控制溢出元素的内容的显示方式

属性名：overflow

属性值：

| 属性值 | 效果                                                 |
| ------ | ---------------------------------------------------- |
| hidden | 溢出影藏                                             |
| scroll | 无论是否溢出，都显示滚动条位置，水平和竖直都有滚动条 |
| auto   | 只有溢出的时候才显示滚动条位置，没有水平滚动条       |

## 十一.移动Web

### 字体图标`<i></i>`

字体图标：展示的是图标，本质是字体

作用：在网页中添加简单的，颜色单一的小图标

优点：

- 灵活性：灵活地修改样式，例如：尺寸，颜色等
- 轻量级：体积小，渲染快，降低服务器请求次数
- 兼容性：几乎兼容所有的主流服务器
- 使用方便：先下载后使用

建立字体图标顺序

- https://www.iconfont.cn/进入网站选取字体图标
- 使用link标签关联该图标对应的.CSS文件
- 创建i标签，设置class值承载字体图标的名字

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <link rel="stylesheet" href="https://at.alicdn.com/t/c/font_4794936_oxf39p47su.css">
    <!-- 要用https协议，不然打不开哦 -->
  <style>
       /*.iconfont表示字体图标 后面的属性和i标签中class的属性值相同*/
  	.iconfont.icon-christmassock {
        /*如果要调整字体大小要保证选择器的优先级大于.iconfont类选择器，在这里如果设置i选择器的话对字体大小属性的操作是不生效的*/
    	color: red;
      	font-size: 50px;
    }
  </style>
  <!-- 对字体图标设置样式 -->
</head>

<body>
  <i class="iconfont icon-christmassock"></i>
  <!-- Iconfont：https://www.iconfont.cn/ -->
</body>

</html>
```

在实际开发中，可以将项目特有的图标（格式为svg）上传到iconfont图标库，生成字体（去除颜色提交）

### 平面转换

#### 平面转换-位移 transform:translate();

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    .box {
      width: 100px;
      height: 100px;
      background-color: red;
      /*画盒子*/
      transform: translateY(100px);
      /*上下移动 垂直位移*/
      transform: translateX(100px);
      /*左右移动 水平位移*/
      transform: translateZ(100px);
      /*用的不多*/
      transform: translate3d(100px, 100px, 100px);
      /*用的不多*/
      margin-bottom: 100px;
      transform: translate(100px, 100px);
      /*transform: translate(x,y);上下左右同时位移，属性值可以是正数也可以是负数*/
    }
  </style>
</head>

<body>
  <div class="box"></div>
</body>

</html>
```

#### 平面转换-位移-绝对居中定位

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    .box {
      background-color: pink;
      width: 500px;
      height: 500px;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      /*绝对居中*/
      /*固定写法，记住就可以了*/
    }
  </style>
</head>

<body>
  <div class="box"></div>
</body>

</html>
```

#### transition过渡属性

作用：可以为一个元素再不同状态之间切换的时候添加过渡效果

特点：是个复合属性

属性值：过渡的属性 花费的时间（单位为秒）

提示：

- 过渡的属性可以是具体的css属性
- 也可以为all（两个状态属性值不同的所有属性，都产生过渡效果）
- transition设置给元素本身

#### 平面转换-缩放 transform: scale();

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    .box {
      width: 100px;
      height: 100px;
      background-color: red;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
    /*先居中*/
    .box:hover {
      transition: all 2s;
      /*动画执行时间 用于做过渡动画使用*/
      /* transform: scale(2,2); */
      /* transform: scaleX(2);*/
      /*transform: scaleY(2); */
      /*transform: scaleZ(2);*/
      /*transform: scale3d(2,2,2);*/
      transform: scale(2);
      /*x轴和y轴等呗放大两倍 等效于transform: scale(2,2);*/
    }
    /*缓慢变大效果*/
  </style>
</head>

<body>
  <div class="box"></div>
</body>

</html>
```

#### 平面转换-旋转 transform: rotate();

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    .box1 {
      width: 100px;
      height: 100px;
      background-color: red;
      transition: all 5s;
      /*旋转动画完成时间为五秒，此处transition的功能被和hover选择器的功能被叠加*/
    }
    .box1:hover {
      transform: rotate(360deg);
      /*deg是角度的意思*/
    }
    /*盒子一，旋转动画示例*/

    .box2 {
      width: 800px;
      height: 200px;
      border: 1px solid black;
      img {
      width: 200px;
      transition: all 8s;
      }
    }
    .box2:hover img {
      transform: translate(600px) rotate(360deg);
    }
    /*盒子二，实现轮胎动画的滚动效果*/
  </style>
</head>

<body>
  <div class="box1"></div>
  <div class="box2">
    <img src="../示例图片/tyre1.png" alt="">
  </div>
</body>

</html>
```

#### 渐变色 background-image: linear-gradient();

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    .box {
      width: 1000px;
      height: 100px;
      background-image: linear-gradient(to right, red, blue, green, orange);
      /*to right图谱状 竖着的*/
    }

    h1 {
      background-image: linear-gradient(red, blue, green, orange);
      /*默认是横向的*/
      background-clip: text;
      /*把颜色给字体而不是给背景图 实现文字渐变 不加这句变成背景渐变*/
      -webkit-text-fill-color: transparent;
      /*文字原本是黑的，导致彩色被覆盖，需要清除这个属性，transparent透明*/
    }
  </style>
</head>

<body>
  <div class="box">
  </div>
  <h1>欢迎来到今天下午的课堂</h1>
</body>

</html>
```

### 动画

**基础动画属性**

|           属性            |     说明     |
| :-----------------------: | :----------: |
|      animation-name       |   动画名称   |
|    animation-duration     |   动画时长   |
| animation-timing-function | 动画速度曲线 |
|      animation-delay      |   动画延迟   |
| animation-iteration-count |   动画次数   |
|    animation-direction    |   动画方向   |
|    animation-fill-mode    | 动画填充模式 |
|   animation-play-state    | 动画播放状态 |

**关键帧动画（@keyframes）**
from/to 写法
百分比写法
多状态动画设置
**高级动画特性**
steps() 步进动画
alternate 交替动画
infinite 无限循环
hover 触发动画
伪元素动画

#### 动画位移 animation+transform

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    /*单次运动动画示例*/
    .box {
      width: 100px;
      height: 100px;
      background-color: red;
      animation-name: active;
      animation-duration: 5s;
    }
    .box:hover {
      animation-name: active;
      /*属性名和关键帧后面的名字相对应*/
      animation-duration: 5s;
    }
    @keyframes active {
      /*@keyframes(关键帧) 动画名称*/
      from {
        transform: translateX(0);
      }

      to {
        transform: translateX(500px);
      }
    }
    /*写法一：from...to写法*/
   
      
      
    /*循环运动渐变动画示例*/
    .box2 {
      width: 100px;
      height: 100px;
      background-color: red;
      animation-name: color;
      animation-duration: 10s;
      /* animation-direction: alternate; */
      /*原路径返回*/
      animation-iteration-count: infinite;
      /*重复循环播放*/
      animation-timing-function: step(10);
      /*使得动画速度均匀*/
    }
    @keyframes color {
      /*@keyframes(关键帧) 动画名称*/
      0% {
        transform: translateX(0);
        background-color: red;
      }

      25% {
        transform: translateX(500px);
        background-color: yellow;
      }

      50% {
        transform: translateX(0);
        background-color: green;
      }

      75% {
        transform: translateX(500px);
        background-color: blue;
      }
      100% {
        transform: translateX(0);
        background-color: red;
      }
    }
    /*写法二，百分比写法*/
    

    /*多元素运动动画示例*/
    .box3 {
      width: 100px;
      height: 500px;
      background-color: black;
      .box4 {
        width: 100px;
      margin-bottom: 100px;
      height: 100px;
      background-color: red;
      animation-name: color;
      animation-duration: 5s;
      animation-iteration-count: infinite;
      animation-timing-function: step(10);
      animation-delay: 1s;
      /*延迟开始1秒*/
      }
      .box5 {
        width: 100px;
      margin-bottom: 100px;
      height: 100px;
      background-color: red;
      animation-name: color;
      animation-duration: 5s;
      animation-iteration-count: infinite;
      animation-timing-function: step(10);
      animation-delay: 2s;
      /*延迟开始2秒*/
      }
      .box6 {
      width: 100px;
      margin-bottom: 100px;
      height: 100px;
      background-color: red;
      animation-name: color;
      animation-duration: 5s;
      animation-iteration-count: infinite;
      animation-timing-function: step(10);
      animation-delay: 3s;
      /*延迟开始3秒*/
      }
    }
  </style>
</head>

<body>
  <div class="box"></div>
  <div class="box2"></div>
  <div class="box3">
    <div class="box4"></div>
    <div class="box5"></div>
    <div class="box6"></div>
  </div>
</body>

</html>
```

#### 动画变色 animation+background-color

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    .box {
      width: 100px;
      height: 100px;
      background-color: red;
    }

    .box:hover {
      animation-name: active;
      animation-duration: 5s;
    }

    @keyframes active {
      from {
        background-color: red;
      }

      to {
        background-color: green;
      }
    }
  </style>
</head>

<body>
  <div class="box"></div>
</body>

</html>
```

#### 动画复合属性

animation:动画名称 动画时间 动画速度 动画延迟 动画次数 动画方向 动画填充模式 动画是否暂停

顺序不能换！！！

#### 动画的其他属性

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="https://at.alicdn.com/t/c/font_4794597_psvmj8z6fss.css">
  <title>Document</title>
  <style>
    /* 设置图标的基础样式 */
    .iconfont {
      font-size: 30px;
      color: red;
      margin-top: 500px;
      position: relative;
    }

    /* 添加文字的伪元素 */
    .iconfont.icon-broken-heart::after {
      content: '';

      animation: textChange 5s 1s infinite alternate steps(10);
    }

    .iconfont.icon-broken-heart {
      display: inline-block;
      animation-name: active;
      animation-duration: 5s;
      animation-delay: 1s;
      animation-fill-mode: forwards;
      animation-timing-function: steps(10);
      animation-iteration-count: infinite;
      animation-direction: alternate;
    }

    .iconfont.icon-broken-heart:hover {
      animation-play-state: paused;
    }

    @keyframes active {
      0% {
        transform: translateX(0) scale(1);
      }

      20% {
        transform: translateX(100px) scale(1.5);
      }

      40% {
        transform: translateX(200px) scale(2);
      }

      60% {
        transform: translateX(300px) scale(2.5);
      }

      80% {
        transform: translateX(400px) scale(3);
      }

      100% {
        transform: translateX(500px) scale(3.5);
      }
    }

    /* 新增文字变化的动画 */
    @keyframes textChange {

      0%,
      39% {
        content: '';
      }

      40%,
      59% {
        content: '胡安雷，你真帅';
      }

      60%,
      100% {
        content: '你有啥实粒，牢弟';
      }
    }
  </style>
</head>

<body>
  <i class="iconfont icon-broken-heart"></i>
</body>

</html>
```

# 个人网站开发教程

本教程将指导你如何从零开始搭建一个简洁美观的个人网站，包括首页、登录页和注册页的开发。

## 项目准备

### 项目结构

在开始开发之前，我们需要先规划好项目的文件结构。一个典型的个人网站项目结构如下：

复制

```
my-personal-website/
│
├── index.html          # 首页
├── login.html          # 登录页面
├── register.html       # 注册页面
├── index.css           # 首页样式文件
├── auth.css            # 登录和注册页面样式文件
├── images/             # 图片资源文件夹
│   └── logo.jpg        # 网站Logo
└── tutorial.md         # 开发教程文档
```

### 技术栈

- **HTML5**：用于构建页面的基本结构。
- **CSS3**：用于美化页面样式，包括布局、颜色、字体等。
- **iconfont**：阿里巴巴图标库，用于在页面中使用矢量图标。
- **响应式设计**：确保网站在不同设备上都能良好显示。

### 开发工具

- **代码编辑器**：推荐使用 Visual Studio Code (VS Code)，它支持丰富的插件和扩展，适合前端开发。
- **浏览器**：推荐使用 Google Chrome，它提供了强大的开发者工具，方便调试和测试。
- **图标库账号**：注册一个阿里巴巴 iconfont 账号，用于获取所需的图标资源。

## 首页开发

### 1. 创建基础 HTML 结构

首先，我们创建一个名为 `index.html` 的文件，并设置基本的 HTML 结构：

html

复制

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>个人作品集</title>
  <link rel="stylesheet" href="index.css">
  <link rel="stylesheet" href="https://at.alicdn.com/t/c/font_4797758_nm146ej1hzb.css">
</head>
<body>
  <!-- 导航栏 -->
  <nav class="nav">
    <div class="nav-left">
      <img src="./images/logo.jpg" alt="个人logo">
    </div>
    <div class="nav-right">
      <ul>
        <li><i class="iconfont icon-shouye-zhihui"></i><a href="#home">首页</a></li>
        <li><i class="iconfont icon-gerenzhongxin-zhihui"></i><a href="#about">关于我</a></li>
        <li><i class="iconfont icon-fenxiang"></i><a href="#works">我的作品</a></li>
        <li><i class="iconfont icon-bianji"></i><a href="#skills">我的技能</a></li>
        <li><i class="iconfont icon-xiaoxi-zhihui"></i><a href="#contact">联系我</a></li>
      </ul>
    </div>
  </nav>

  <!-- 头部/首页区域 -->
  <header id="home" class="hero">
    <div class="hero-content">
      <h1>你好，我是小堇</h1>
      <p class="subtitle">前端开发工程师 / UI设计师</p>
      <a href="#contact" class="cta-button">联系我</a>
    </div>
  </header>

  <!-- 底部 -->
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-left">
        <img src="./images/logo.jpg" alt="logo">
      </div>
      <div class="footer-center">
        <div class="social-links">
          <a href="https://github.com/xiaojinyyds"><i class="iconfont icon-github"></i>My github</a>
          <a href="https://blog.csdn.net/2301_79539778?spm=1000.2115.3001.5343"><i class="iconfont icon-blogger"></i>My blog</a>
          <a href="https://space.bilibili.com/667961819?spm_id_from=333.1007.0.0"><i class="iconfont icon-vedio"></i>My video</a>
        </div>
      </div>
      <div class="footer-right">
        <p class="copyright">© 2024 版权所有</p>
      </div>
    </div>
  </footer>
</body>
</html>
```



运行 HTML

### 2. 添加导航栏

导航栏是网站的重要组成部分，通常位于页面的顶部。我们使用 `<nav>` 标签来创建导航栏，并通过 CSS 样式来美化它。

html

复制

```html
<nav class="nav">
  <div class="nav-left">
    <img src="./images/logo.jpg" alt="个人logo">
  </div>
  <div class="nav-right">
    <ul>
      <li><i class="iconfont icon-shouye-zhihui"></i><a href="#home">首页</a></li>
      <li><i class="iconfont icon-gerenzhongxin-zhihui"></i><a href="#about">关于我</a></li>
      <li><i class="iconfont icon-fenxiang"></i><a href="#works">我的作品</a></li>
      <li><i class="iconfont icon-bianji"></i><a href="#skills">我的技能</a></li>
      <li><i class="iconfont icon-xiaoxi-zhihui"></i><a href="#contact">联系我</a></li>
    </ul>
  </div>
</nav>
```



运行 HTML

### 3. 创建首页区域

首页区域通常包含一个欢迎语、个人简介以及一个行动按钮（如“联系我”）。我们使用 `<header>` 标签来定义首页区域，并通过 CSS 样式来设置背景、字体等。

html

复制

```html
<header id="home" class="hero">
  <div class="hero-content">
    <h1>你好，我是小堇</h1>
    <p class="subtitle">前端开发工程师 / UI设计师</p>
    <a href="#contact" class="cta-button">联系我</a>
  </div>
</header>
```



运行 HTML

### 4. 添加页脚

页脚通常包含版权信息、社交媒体链接等。我们使用 `<footer>` 标签来创建页脚，并通过 CSS 样式来美化它。

html

复制

```html
<footer class="footer">
  <div class="footer-content">
    <div class="footer-left">
      <img src="./images/logo.jpg" alt="logo">
    </div>
    <div class="footer-center">
      <div class="social-links">
        <a href="https://github.com/xiaojinyyds"><i class="iconfont icon-github"></i>My github</a>
        <a href="https://blog.csdn.net/2301_79539778?spm=1000.2115.3001.5343"><i class="iconfont icon-blogger"></i>My blog</a>
        <a href="https://space.bilibili.com/667961819?spm_id_from=333.1007.0.0"><i class="iconfont icon-vedio"></i>My video</a>
      </div>
    </div>
    <div class="footer-right">
      <p class="copyright">© 2024 版权所有</p>
    </div>
  </div>
</footer>
```



运行 HTML

### 5. 添加 CSS 样式

为了让页面看起来更加美观，我们需要为 HTML 元素添加 CSS 样式。创建一个名为 `index.css` 的文件，并将以下样式代码添加到文件中：

css

复制

```css
/* 全局样式重置 */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "PingFang SC", "Microsoft YaHei", sans-serif;
  line-height: 1.6;
  color: #333;
  background-color: #f8f9fa;
}

/* 导航栏样式 */
.nav {
  position: fixed;
  top: 0;
  width: 100%;
  padding: 1rem 5%;
  background: rgba(255, 255, 255, 0.98);
  backdrop-filter: blur(10px);
  box-shadow: 0 2px 15px rgba(0, 0, 0, 0.08);
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 1000;
}

.nav-left img {
  height: 45px;
  border-radius: 8px;
}

.nav-right ul {
  display: flex;
  list-style: none;
  gap: 2.5rem;
}

.nav-right li {
  display: flex;
  align-items: center;
  gap: 8px;
  position: relative;
}

.nav-right a {
  text-decoration: none;
  color: #555;
  font-weight: 500;
  font-size: 1.05rem;
  transition: all 0.3s ease;
}

.nav-right .iconfont {
  color: #555;
  font-size: 1.2rem;
  transition: all 0.3s ease;
}

/* 导航hover效果 */
.nav-right li::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background: #3b82f6;
  transition: width 0.3s ease;
}

.nav-right li:hover::after {
  width: 100%;
}

.nav-right li:hover .iconfont,
.nav-right li:hover a {
  color: #3b82f6;
  transform: translateY(-2px);
}

/* 头部/首页区域样式 */
.hero {
  height: 100vh;
  background: linear-gradient(135deg, #e0f2fe 0%, #dbeafe 50%, #e0e7ff 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 0 1rem;
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: '';
  position: absolute;
  width: 100%;
  height: 100%;
  background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="50" cy="50" r="40" fill="none" stroke="rgba(255,255,255,0.2)" stroke-width="2"/></svg>') repeat;
  opacity: 0.5;
  animation: rotate 60s linear infinite;
}

@keyframes rotate {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

.hero-content {
  position: relative;
  z-index: 1;
  max-width: 800px;
  padding: 2rem;
}

.hero-content h1 {
  font-size: 4rem;
  margin-bottom: 1.5rem;
  background: linear-gradient(to right, #3b82f6, #8b5cf6);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: fadeInUp 1s ease;
}

.subtitle {
  font-size: 1.8rem;
  color: #4b5563;
  margin-bottom: 2.5rem;
  animation: fadeInUp 1s ease 0.2s backwards;
}

.cta-button {
  display: inline-block;
  padding: 1rem 2.5rem;
  background: linear-gradient(135deg, #3b82f6, #8b5cf6);
  color: white;
  text-decoration: none;
  border-radius: 50px;
  font-weight: 500;
  font-size: 1.1rem;
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(59, 130, 246, 0.3);
  animation: fadeInUp 1s ease 0.4s backwards;
}

.cta-button:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 20px rgba(59, 130, 246, 0.4);
}

/* 页脚样式 */
.footer {
  background: #99c2eb;
  border-top: 1px solid #e5e7eb;
  padding: 3rem 5%;
  margin-top: 0;
  color: #fff;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
}

.footer-left img {
  height: 40px;
  border-radius: 4px;
}

.footer-center {
  flex-grow: 1;
  margin: 0 4rem;
}

.social-links {
  display: flex;
  justify-content: center;
  gap: 2rem;
}

.social-links a {
  display: flex;
  align-items: center;
  gap: 8px;
  color: #fff;
  text-decoration: none;
  transition: all 0.3s ease;
  font-size: 0.95rem;
}

.social-links .iconfont {
  font-size: 1.2rem;
}

.social-links a:hover {
  color: #e0e0e0;
  transform: translateY(-2px);
}

.footer-right .copyright {
  color: #fff;
  font-size: 0.9rem;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .nav {
    padding: 1rem 1.5rem;
  }
  
  .nav-right ul {
    position: fixed;
    top: 70px;
    left: 0;
    width: 100%;
    background: white;
    flex-direction: column;
    padding: 1rem 0;
    gap: 0;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    display: none;
  }
  
  .nav-right li {
    padding: 1rem 2rem;
  }
  
  .hero-content h1 {
    font-size: 2.5rem;
  }
  
  .subtitle {
    font-size: 1.3rem;
  }
  
  .footer-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  
  .social-links {
    align-items: center;
  }
  
  .social-links a {
    width: 100%;
    justify-content: center;
  }
}
```

### 6. 添加图标

我们使用阿里巴巴的 iconfont 图标库来为导航栏和页脚添加图标。首先，在 iconfont 上选择所需的图标，并生成一个 CSS 文件链接。然后，在 `index.html` 文件中引入该链接：

html

复制

```html
<link rel="stylesheet" href="https://at.alicdn.com/t/c/font_4797758_nm146ej1hzb.css">
```



运行 HTML

在 HTML 中，我们可以通过 `iconfont` 类来使用图标。例如：

html

复制

```html
<i class="iconfont icon-shouye-zhihui"></i>
```



运行 HTML

### 7. 响应式设计

为了确保网站在不同设备上都能良好显示，我们使用媒体查询来实现响应式设计。在 `index.css` 文件中，我们添加了针对小屏幕设备的样式调整：

css

复制

```css
@media (max-width: 768px) {
  .nav {
    padding: 1rem 1.5rem;
  }
  
  .nav-right ul {
    position: fixed;
    top: 70px;
    left: 0;
    width: 100%;
    background: white;
    flex-direction: column;
    padding: 1rem 0;
    gap: 0;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    display: none;
  }
  
  .nav-right li {
    padding: 1rem 2rem;
  }
  
  .hero-content h1 {
    font-size: 2.5rem;
  }
  
  .subtitle {
    font-size: 1.3rem;
  }
  
  .footer-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  
  .social-links {
    align-items: center;
  }
  
  .social-links a {
    width: 100%;
    justify-content: center;
  }
}
```

### 8. 测试与调试

完成首页的开发后，我们可以在浏览器中打开 `index.html` 文件，查看页面的效果。使用浏览器的开发者工具（F12）可以调试和调整样式，确保页面在不同设备上都能正常显示。

### 9. 完整源码 index.html：

```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>个人作品集</title>
  <link rel="stylesheet" href="index.css">
  <link rel="stylesheet" href="https://at.alicdn.com/t/c/font_4797758_nm146ej1hzb.css">
</head>

<body>
  <!-- 导航栏 -->
  <nav class="nav">
    <div class="nav-left">
      <img src="./images/logo.jpg" alt="个人logo">
    </div>
    <div class="nav-right">
      <ul>
        <li><i class="iconfont icon-shouye-zhihui"></i><a href="#home">首页</a></li>
        <li><i class="iconfont icon-gerenzhongxin-zhihui"></i><a href="#about">关于我</a></li>
        <li><i class="iconfont icon-fenxiang"></i><a href="#works">我的作品</a></li>
        <li><i class="iconfont icon-bianji"></i><a href="#skills">我的技能</a></li>
        <li><i class="iconfont icon-xiaoxi-zhihui"></i><a href="#contact">联系我</a></li>
      </ul>
    </div>
  </nav>

  <!-- 头部/首页区域 -->
  <header id="home" class="hero">
    <div class="hero-content">
      <h1>你好，我是小堇</h1>
      <p class="subtitle">前端开发工程师 / UI设计师</p>
      <a href="#contact" class="cta-button">联系我</a>
    </div>
  </header>

  <!-- 底部 -->
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-left">
        <img src="./images/logo.jpg" alt="logo">
      </div>
      <div class="footer-center">
        <div class="social-links">
          <a href="https://github.com/xiaojinyyds"><i class="iconfont icon-github"></i>My github</a>
          <a href="https://blog.csdn.net/2301_79539778?spm=1000.2115.3001.5343"><i class="iconfont icon-blogger"></i>My
            blog</a>
          <a href="https://space.bilibili.com/667961819?spm_id_from=333.1007.0.0"><i class="iconfont icon-vedio"></i>My
            video</a>
          <!-- 添加更多社交媒体链接 -->
        </div>
      </div>
      <div class="footer-right">

        <p class="copyright">© 2024 版权所有</p>
      </div>
    </div>
  </footer>

</body>

</html>
```

```css
/* 全局样式重置 */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: "PingFang SC", "Microsoft YaHei", sans-serif;
    line-height: 1.6;
    color: #333;
    background-color: #f8f9fa;
}

/* 导航栏样式 */
.nav {
    position: fixed;
    top: 0;
    width: 100%;
    padding: 1rem 5%;
    background: rgba(255, 255, 255, 0.98);
    backdrop-filter: blur(10px);
    box-shadow: 0 2px 15px rgba(0, 0, 0, 0.08);
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 1000;
}

.nav-left img {
    height: 45px;
    border-radius: 8px;
}

.nav-right ul {
    display: flex;
    list-style: none;
    gap: 2.5rem;
}

.nav-right li {
    display: flex;
    align-items: center;
    gap: 8px;
    position: relative;
}

.nav-right a {
    text-decoration: none;
    color: #555;
    font-weight: 500;
    font-size: 1.05rem;
    transition: all 0.3s ease;
}

.nav-right .iconfont {
    color: #555;
    font-size: 1.2rem;
    transition: all 0.3s ease;
}

/* 导航hover效果 */
.nav-right li::after {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 0;
    height: 2px;
    background: #3b82f6;
    transition: width 0.3s ease;
}

.nav-right li:hover::after {
    width: 100%;
}

.nav-right li:hover .iconfont,
.nav-right li:hover a {
    color: #3b82f6;
    transform: translateY(-2px);
}

/* 头部/首页区域样式 */
.hero {
    height: 100vh;
    background: linear-gradient(135deg, #e0f2fe 0%, #dbeafe 50%, #e0e7ff 100%);
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 0 1rem;
    position: relative;
    overflow: hidden;
}

.hero::before {
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="50" cy="50" r="40" fill="none" stroke="rgba(255,255,255,0.2)" stroke-width="2"/></svg>') repeat;
    opacity: 0.5;
    animation: rotate 60s linear infinite;
}

@keyframes rotate {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
}

.hero-content {
    position: relative;
    z-index: 1;
    max-width: 800px;
    padding: 2rem;
}

.hero-content h1 {
    font-size: 4rem;
    margin-bottom: 1.5rem;
    background: linear-gradient(to right, #3b82f6, #8b5cf6);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: fadeInUp 1s ease;
}


.subtitle {
    font-size: 1.8rem;
    color: #4b5563;
    margin-bottom: 2.5rem;
    animation: fadeInUp 1s ease 0.2s backwards;
}

.cta-button {
    display: inline-block;
    padding: 1rem 2.5rem;
    background: linear-gradient(135deg, #3b82f6, #8b5cf6);
    color: white;
    text-decoration: none;
    border-radius: 50px;
    font-weight: 500;
    font-size: 1.1rem;
    transition: all 0.3s ease;
    box-shadow: 0 4px 15px rgba(59, 130, 246, 0.3);
    animation: fadeInUp 1s ease 0.4s backwards;
}

.cta-button:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 20px rgba(59, 130, 246, 0.4);
}

/* 通用区块样式 */
section {
    padding: 5rem 10%;
}

section h2 {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 3rem;
}

/* 页脚样式 */
.footer {
    background: #99c2eb;
    border-top: 1px solid #e5e7eb;
    padding: 3rem 5%;
    margin-top: 0;
    color: #fff;
}

.footer-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
}

.footer-left img {
    height: 40px;
    border-radius: 4px;
}

.footer-center {
    flex-grow: 1;
    margin: 0 4rem;
}

.social-links {
    display: flex;
    justify-content: center;
    gap: 2rem;
}

.social-links a {
    display: flex;
    align-items: center;
    gap: 8px;
    color: #fff;
    text-decoration: none;
    transition: all 0.3s ease;
    font-size: 0.95rem;
}

.social-links .iconfont {
    font-size: 1.2rem;
}

.social-links a:hover {
    color: #e0e0e0;
    transform: translateY(-2px);
}

.footer-right .copyright {
    color: #fff;
    font-size: 0.9rem;
}

/* 响应式设计 - 合并所有媒体查询 */
@media (max-width: 768px) {
    /* 导航栏响应式 */
    .nav {
        padding: 1rem 1.5rem;
    }
    
    .nav-right ul {
        position: fixed;
        top: 70px;
        left: 0;
        width: 100%;
        background: white;
        flex-direction: column;
        padding: 1rem 0;
        gap: 0;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        display: none;
    }
    
    .nav-right li {
        padding: 1rem 2rem;
    }
    
    .hero-content h1 {
        font-size: 2.5rem;
    }
    
    .subtitle {
        font-size: 1.3rem;
    }
    
    /* 页脚响应式 */
    .footer-content {
        flex-direction: column;
        gap: 2rem;
        text-align: center;
    }
    
    .footer-center {
        margin: 1.5rem 0;
    }
    
    .social-links {
        flex-wrap: wrap;
        justify-content: center;
    }
    
    .social-links a {
        justify-content: center;
    }
}

/* 动画效果 */
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* 响应式设计 */
@media (max-width: 768px) {
    .nav {
        padding: 1rem 1.5rem;
    }
    
    .nav-right ul {
        position: fixed;
        top: 70px;
        left: 0;
        width: 100%;
        background: white;
        flex-direction: column;
        padding: 1rem 0;
        gap: 0;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        display: none;
    }
    
    .nav-right li {
        padding: 1rem 2rem;
    }
    
    .hero-content h1 {
        font-size: 2.5rem;
    }
    
    .subtitle {
        font-size: 1.3rem;
    }
    
    .footer-content {
        flex-direction: column;
        align-items: center;
        text-align: center;
    }
    
    .social-links {
        align-items: center;
    }
    
    .social-links a {
        width: 100%;
        justify-content: center;
    }
} 
```

## 登录页面开发

### 1. 创建基础 HTML 结构

首先，我们创建一个名为 `login.html` 的文件，并设置基本的 HTML 结构：

html

复制

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>登录</title>
  <link rel="stylesheet" href="auth.css">
  <link rel="stylesheet" href="https://at.alicdn.com/t/c/font_4797758_nm146ej1hzb.css">
</head>
<body>
  <div class="container">
    <div class="login-box">
      <h2>登录</h2>
      <form>
        <div class="input-group">
          <input type="text" required>
          <label>用户名</label>
        </div>
        <div class="input-group">
          <input type="password" required>
          <label>密码</label>
        </div>
        <button type="submit"><a href="index.html">登录</a></button>
        <div class="links">
          <a href="register.html">注册账号</a>
          <a href="#">忘记密码？</a>
        </div>
      </form>
    </div>
  </div>
</body>
</html>
```



运行 HTML

### 2. 添加登录表单

登录表单包含两个输入框：一个用于输入用户名，另一个用于输入密码。我们使用 `<form>` 标签来创建表单，并通过 CSS 样式来美化它。

html

复制

```html
<form>
  <div class="input-group">
    <input type="text" required>
    <label>用户名</label>
  </div>
  <div class="input-group">
    <input type="password" required>
    <label>密码</label>
  </div>
  <button type="submit"><a href="index.html">登录</a></button>
  <div class="links">
    <a href="register.html">注册账号</a>
    <a href="#">忘记密码？</a>
  </div>
</form>
```



运行 HTML

### 3. 添加 CSS 样式

为了让登录页面看起来更加美观，我们需要为 HTML 元素添加 CSS 样式。创建一个名为 `auth.css` 的文件，并将以下样式代码添加到文件中：

css

复制

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "PingFang SC", "Microsoft YaHei", sans-serif;
  background: linear-gradient(120deg, #a1c4fd 0%, #c2e9fb 100%);
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.container {
  width: 100%;
  padding: 20px;
}

.login-box {
  background: white;
  border-radius: 10px;
  padding: 40px;
  max-width: 400px;
  margin: 0 auto;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

h2 {
  text-align: center;
  margin-bottom: 30px;
  color: #333;
  font-size: 24px;
}

.input-group {
  position: relative;
  margin-bottom: 30px;
}

.input-group input {
  width: 100%;
  padding: 10px 0;
  font-size: 16px;
  color: #333;
  border: none;
  border-bottom: 1px solid #ddd;
  outline: none;
  background: transparent;
}

.input-group label {
  position: absolute;
  top: 10px;
  left: 0;
  font-size: 16px;
  color: #666;
  pointer-events: none;
  transition: 0.3s ease all;
}

.input-group input:focus ~ label,
.input-group input:valid ~ label {
  top: -20px;
  font-size: 14px;
  color: #3b82f6;
}

.input-group input:focus {
  border-bottom-color: #3b82f6;
}

button {
  width: 100%;
  padding: 12px;
  background: #3b82f6;
  color: white;
  border: none;
  border-radius: 5px;
  font-size: 16px;
  cursor: pointer;
  transition: background 0.3s;
}

button a {
  text-decoration: none;
  color: white;
}

button:hover {
  background: #2563eb;
}

.links {
  margin-top: 20px;
  display: flex;
  justify-content: space-between;
}

.links a {
  color: #3b82f6;
  text-decoration: none;
  font-size: 14px;
}

.links a:hover {
  text-decoration: underline;
}

@media (max-width: 480px) {
  .login-box {
    padding: 30px 20px;
  }
}
```

### 4. 添加交互效果

为了让登录页面更加动态，我们为输入框添加了交互效果。当用户点击输入框时，标签会向上移动，并且输入框的下划线颜色会发生变化。

css

复制

```css
.input-group input:focus ~ label,
.input-group input:valid ~ label {
  top: -20px;
  font-size: 14px;
  color: #3b82f6;
}

.input-group input:focus {
  border-bottom-color: #3b82f6;
}
```

### 5. 测试与调试

完成登录页面的开发后，我们可以在浏览器中打开 `login.html` 文件，查看页面的效果。使用浏览器的开发者工具（F12）可以调试和调整样式，确保页面在不同设备上都能正常显示。

### 6.完整源码 login.html：

```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>登录</title>
  <link rel="stylesheet" href="auth.css">
  <link rel="stylesheet" href="https://at.alicdn.com/t/c/font_4797758_nm146ej1hzb.css">
</head>

<body>
  <div class="container">
    <div class="login-box">
      <h2>登录</h2>
      <form>
        <div class="input-group">
          <input type="text" required>
          <label>用户名</label>
        </div>
        <div class="input-group">
          <input type="password" required>
          <label>密码</label>
        </div>
        <button type="submit"><a href="index.html">登录</a></button>
        <div class="links">
          <a href="register.html">注册账号</a>
          <a href="#">忘记密码？</a>
        </div>
      </form>
    </div>
  </div>
</body>

</html>
```

## 注册页面开发

### 1. 创建基础 HTML 结构

首先，我们创建一个名为 `register.html` 的文件，并设置基本的 HTML 结构：

html

复制

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>注册</title>
  <link rel="stylesheet" href="auth.css">
  <link rel="stylesheet" href="https://at.alicdn.com/t/c/font_4797758_nm146ej1hzb.css">
</head>
<body>
  <div class="container">
    <div class="login-box">
      <h2>注册</h2>
      <form>
        <div class="input-group">
          <input type="text" required>
          <label>用户名</label>
        </div>
        <div class="input-group">
          <input type="email" required>
          <label>邮箱</label>
        </div>
        <div class="input-group">
          <input type="password" required>
          <label>密码</label>
        </div>
        <div class="input-group">
          <input type="password" required>
          <label>确认密码</label>
        </div>
        <button type="submit">注册</button>
        <div class="links">
          <a href="login.html">返回登录</a>
        </div>
      </form>
    </div>
  </div>
</body>
</html>
```



运行 HTML

### 2. 添加注册表单

注册表单包含四个输入框：一个用于输入用户名，一个用于输入邮箱，两个用于输入密码和确认密码。我们使用 `<form>` 标签来创建表单，并通过 CSS 样式来美化它。

```html
<form>
  <div class="input-group">
    <input type="text" required>
    <label>用户名</label>
  </div>
  <div class="input-group">
    <input type="email" required>
    <label>邮箱</label>
  </div>
  <div class="input-group">
    <input type="password" required>
    <label>密码</label>
  </div>
  <div class="input-group">
    <input type="password" required>
    <label>确认密码</label>
  </div>
  <button type="submit">注册</button>
  <div class="links">
    <a href="login.html">返回登录</a>
  </div>
</form>
```

### 3. 添加 CSS 样式

注册页面与登录页面共享相同的 CSS 样式文件 `auth.css`，因此我们无需额外添加样式。注册页面的样式与登录页面保持一致，确保网站的整体风格统一。

### 4. 添加交互效果

注册页面的交互效果与登录页面相同。当用户点击输入框时，标签会向上移动，并且输入框的下划线颜色会发生变化。

css

复制

```css
.input-group input:focus ~ label,
.input-group input:valid ~ label {
  top: -20px;
  font-size: 14px;
  color: #3b82f6;
}

.input-group input:focus {
  border-bottom-color: #3b82f6;
}
```

### 5. 测试与调试

完成注册页面的开发后，我们可以在浏览器中打开 `register.html` 文件，查看页面的效果。使用浏览器的开发者工具（F12）可以调试和调整样式，确保页面在不同设备上都能正常显示。

### 6.完整源码 register.html：

```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>注册</title>
  <link rel="stylesheet" href="auth.css">
  <link rel="stylesheet" href="https://at.alicdn.com/t/c/font_4797758_nm146ej1hzb.css">
</head>

<body>
  <div class="container">
    <div class="login-box">
      <h2>注册</h2>
      <form>
        <div class="input-group">
          <input type="text" required>
          <label>用户名</label>
        </div>
        <div class="input-group">
          <input type="email" required>
          <label>邮箱</label>
        </div>
        <div class="input-group">
          <input type="password" required>
          <label>密码</label>
        </div>
        <div class="input-group">
          <input type="password" required>
          <label>确认密码</label>
        </div>
        <button type="submit">注册</button>
        <div class="links">
          <a href="login.html">返回登录</a>
        </div>
      </form>
    </div>
  </div>
</body>

</html>
```

### 7.CSS属性源码 auth.css：

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: "PingFang SC", "Microsoft YaHei", sans-serif;
    background: linear-gradient(120deg, #a1c4fd 0%, #c2e9fb 100%);
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
}

.container {
    width: 100%;
    padding: 20px;
}

.login-box {
    background: white;
    border-radius: 10px;
    padding: 40px;
    max-width: 400px;
    margin: 0 auto;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

h2 {
    text-align: center;
    margin-bottom: 30px;
    color: #333;
    font-size: 24px;
}

.input-group {
    position: relative;
    margin-bottom: 30px;
}

.input-group input {
    width: 100%;
    padding: 10px 0;
    font-size: 16px;
    color: #333;
    border: none;
    border-bottom: 1px solid #ddd;
    outline: none;
    background: transparent;
}

.input-group label {
    position: absolute;
    top: 10px;
    left: 0;
    font-size: 16px;
    color: #666;
    pointer-events: none;
    transition: 0.3s ease all;
}

.input-group input:focus ~ label,
.input-group input:valid ~ label {
    top: -20px;
    font-size: 14px;
    color: #3b82f6;
}

.input-group input:focus {
    border-bottom-color: #3b82f6;
}

button {
    width: 100%;
    padding: 12px;
    background: #3b82f6;
    color: white;
    border: none;
    border-radius: 5px;
    font-size: 16px;
    cursor: pointer;
    transition: background 0.3s;
}

button a {
    text-decoration: none;
    color: white;
}

button:hover {
    background: #2563eb;
}

.links {
    margin-top: 20px;
    display: flex;
    justify-content: space-between;
}

.links a {
    color: #3b82f6;
    text-decoration: none;
    font-size: 14px;
}

.links a:hover {
    text-decoration: underline;
}

@media (max-width: 480px) {
    .login-box {
        padding: 30px 20px;
    }
} 
```

