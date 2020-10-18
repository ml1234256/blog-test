### [HTML简介]
HTML（Hyper Text Markup Language，超文本标记语言）是由李爵士发明的，他还写了第一个浏览器与服务器，发明了WWW, URL , HTTP 
```HTML
<!DOCTYPE html> <!--表示文档类型为html-->
<html lang="ch-CN">  <!-- "lang"表示语言，"en"为英语， "ch-CN"为中国大陆中文 -->
<head>
    <meta charset="UTF-8"> <!--文字的编码类型-->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  <!--禁用缩放，兼容手机-->
    <meta http-equiv="X-UA-Compatible" content="ie=edge"> <!--使用最新的IE内核-->
    <title>html</title> <!--页面的标题-->
</head>
<body>
    
</body>
</html>
```
### [HTML章节标签]
* 标题 h1~h6： 块级元素
* 段落 p： 块级元素
* 盒子 div：块级元素
* span： 行级元素
* 头部 header：代表页面的顶部，可以放广告
* 脚部 footer：代表网页的页脚，包含作者、版权等信息
* 主要内容 main：页面的主要内容
* 章节 section
* 旁支内容 aside：与正文无关的内容，如参考资料等

### [HTML全局属性]
* class
* id：具有唯一性，但是如果出现多个相同的id不会被检测
* contenteditable ：可在页面中编写html文档内容
* hidden: 隐藏标签
* style ：行内css样式
* tabindex：按tab键选定的次序，>0按顺序选中，=0最后选中，-1永远不选中
* title：文字溢出隐藏时，鼠标放在元素上显示的完整内容

### [HTML内容标签]
* 有序列表 ol + li (ordered list)：块级元素
    ```HTML
    <ol type="A" start="5">  <!-- type: 1, A, a, I, i -->
	    <li> E </li>
	    <li> F </li>
	    <li> G </li>
    </ol>
    ```
* 无序列表 ul + li (unordered list)：块级元素
    ```HTML
    <ul type="square">  <!-- type: square, disc, circle -->
	    <li> a </li>
	    <li> a </li>
	    <li> a </li>
    </ul>
    ```
* dl + dt + dd ( description list, term, data)
* hr: 分割线
    ```HTML 
    <hr style="background-color:#ddd;height:1px;border:none"/> <!--需要设置height与border才有颜色-->
    ```
* br (break)： 换行
* a (anchor锚点): 行级元素
	* 超链接：
    ```HTML
	<a href="http://www.baidu.com" target="_self"> 百度 </a>
	<!-- target: _self 默认值，在当前页面打开；_blank 在空白页面打开--> 
    ```
	* 锚点：页面内跳转
    ```HTML
		<div id="a1"> a1 </div>
        <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
    <div id="a2"> a2 </div>
        <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
    <a href="#a1"> find a1 </a>
    <a href="#a2"> find a2 </a>
    ```
	* 打电话(移动端常用):
    ```HTML
	<a href="tel:6666666"> 给猪猪打电话 </a>
    ```
	* 发邮件:
    ```HTML
	<a href="mailto:zhuzhu@qq.com"> 给猪猪发邮件 </a>
    ```
	* 协议限定符：
    ```HTML
	<a href="javascript:while(1){alert('猪猪不腻你')}"> 点一下猪猪 </a>
    ```
* em (emphasis)： 斜体，行级元素
* strong： 加粗，行级元素
* pre (preview): pre标签内的内容保留空格、回车、tag等
* code：code标签内的是等宽的，用来标记代码
    ```HTML
    <!--使用pre标签来保留code标签内的格式-->
    <pre>
      <code>
        print('你好猪猪')
        ptint('猪猪你好')
      </code>
    </pre>
    ```
* q (quote): 引用， 行级元素
* blockquote： 换行引用，块级元素

### [HTML标签默认样式]

标签自带的样式，通过Chrome开发者工具查看（styles -> user agent stylesheet）
css重置默认样式：

```CSS
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
*::after, *::before {
    box-sizing: border-box;
}
h1, h2, h3, h4, h5, h6 {
    font-weight: normal;
}
a {
    color: inherit;
    text-decoration: none;
}
ul, ol {
    list-style: none;
}
table {
    border-collapse: collapse;
    border-spacing: 0;
}
```

### [文字溢出处理]

```CSS
div{
    white-space: nowrap; /* 不换行 */
    overflow: hidden;  /* 溢出隐藏 */
    text-overflow: ellipsis;  /* 省略处用...代替 */
```