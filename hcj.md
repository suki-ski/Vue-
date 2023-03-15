# HTML

| 标签         | 表示        |
| ------------ | ----------- |
| **标题标签** | `<h1>-<h6>` |
| **段落标签** | `<p></p>`   |
| **换行标签** | `<br/>`     |

**文件格式化标签**

| 语义   | 标签                          |
| ------ | ----------------------------- |
| 加粗   | `<strong></strong>` `<b></b>` |
| 倾斜   | `<em></em>` `<i></i>`         |
| 删除线 | `<del></del>` `<s></s>`       |
| 下划线 | `<ins></ins>` `<u></u>`       |

**div和span**

`<div></div>`标签：独占一行

`<span></span>`标签：一行可以放多个

**图像标签：**

`<img src="图像URL" alt="图片失效之后显示" title="鼠标放在图片上显示">`

**超链接标签：**

`<a href="跳转目标" target="目标窗口的弹出方式"></a>`

| 属性     | 作用                                        |
| -------- | ------------------------------------------- |
| `href`   | 连接目标的`url`地址                         |
| `target` | \_self为默认值，\_blank为在新窗口中打开方式 |

**base标签：**

总结：

1. base可以设置整体链接的打开状态
2. 写到`<head></head>`之间
3. 给所有的连接都默认添加`target="_blank"`

**预格式化文本pre标签：**

`<pre></pre>`

保留文本的空格和换行

**表格：**

表格标签：`<table></table>`

行标签：`<tr></tr>`

单元格标签：`<td></td>`

~~~html
<table>
    <tr>
    	<td></td>
    </tr>
</table>
~~~

`<thead></thead>`

`<tbody></tbody>`

写在table标签里面

| 属性名        | 属性值            | 描述                            |
| ------------- | ----------------- | ------------------------------- |
| `align`       | left,center,right | 表单的对齐方式                  |
| `cellpadding` | 像素值            | 单元格与内容之间的空白，默认1   |
| `cellspacing` | 像素值            | 单元格与单元格之间的空白，默认2 |

**合并单元格方式：**

* 跨行合并：`rowspan="个数"`
* 跨列合并：`colspan="个数"`



**列表标签：**

| 标签名      | 定义       | 注意               |
| ----------- | ---------- | ------------------ |
| `<ul></ul>` | 无序标签   | 里面只能包含li     |
| `<ol><ol>`  | 有序标签   | 里面只能包含li     |
| `<dl></dl>` | 自定义标签 | 里面只能包含dt和dd |

~~~html
<dl>
    <dt>名词1</dt>
    <dd>名词1解释1</dd>
</dl>
~~~



**表单：**`<form></form>`

~~~html
<form action="url地址" method="提交方式" name="表单域名称">
    各种表单元素控件
</form>
~~~

| 属性     | 属性值    | 作用                                             |
| -------- | --------- | ------------------------------------------------ |
| `action` | `url`地址 | 用于指定接收并处理表单数据的服务器程序的地址     |
| `method` | get/post  | 用于设置表单数据的提交方式                       |
| name     | 名称      | 用于指定表单的名称，以区分一个页面中的多个表单域 |

**表单控件：**

1. `input`输入表单元素
2. `select`下拉表单元素
3. `textarea`文本域元素(可以自由拖拉的文本框)

`<input>`type属性的属性值描述：

| 属性值   | 描述                             |
| -------- | -------------------------------- |
| button   | 按钮                             |
| checkbox | 复选框                           |
| file     | 输入字段和"浏览"按钮，供文件上传 |
| hidden   | 隐藏的输入字段                   |
| image    | 图像形式的提交按钮               |
| password | 密码字段，会被遮挡               |
| radio    | 单选按钮                         |
| reset    | 重置按钮，重置表单内的各种数据   |
| submit   | 提交按钮，发送给服务器           |
| text     | 用于输入文本                     |

**select下拉表单标签**

~~~html
<select>
    <option>选项1</option>
    <option>选项2</option>
    <option>选项3</option>
</select>
~~~

<select>
    <option>选项1</option>
    <option>选项2</option>
    <option>选项3</option>
</select>

**`textarea`文本域元素**

rows：行数

cols：列数

~~~html
<textarea row="3" cols="20">
	文本内容
</textarea>
~~~

<textarea row="3" cols="20">
	文本内容
</textarea>





# CSS

**内嵌式：**在head标签内，用style标签定义	

~~~html
<style>
    div{
		color: red;
        font-size: 12px
    }
</style>
~~~

**外链式：**在另外一个文件内被引用到当前文件

~~~html
<head>
    <link rel="stylesheet" type="text/css" href="css文件路径">
</head>
~~~

**行内式：**写在需要被修饰的标签内

~~~html
<div style="color: red; font-size: 12px">
    青春不常在
</div>
~~~



**font-family:**定义字体

~~~
p{font-family:"微软雅黑","宋体","Microsoft Yahei"}
~~~

常见字体：宋体，微软雅黑，黑体



**选择器：**

**标签选择器：**

~~~html
标签名 {
	属性1：属性值1;
	属性2：属性2;
	...
}
~~~

**类选择器：**

标签：

~~~html
<p class="类名"></p>
~~~

类选择器：

~~~html
.类名 {
	属性1:属性值1;
	属性2:属性值2;
	属性3:属性值3;
}
~~~

**id选择器：**

标签：

~~~html
<p id="id名"></p>
~~~

id选择器：

~~~html
#id名 {
	属性1:属性值1;
	属性2:属性值2;
	属性3:属性值3;
}
~~~

**通配符选择器：**匹配页面内所有的元素

~~~html
* {
	margin: 0;
	padding: 0;
}
~~~

**后代选择器：**

~~~css
.class h3 {
    color: red;
    font-size: 16px;
}
~~~

**子代选择器：**

~~~css
.class>h3 {
    color: red;
    font-size: 16px;
}
~~~

**交集选择器：**

~~~css
p.red {
    color: red;
}
~~~

**并集选择器：**

~~~css
        p,
        span,
        .red {
            color: red;
        }
~~~

**链接伪类选择器：**

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>链接伪类选择器</title>
    <style>
        /* 未访问过的链接的状态，正常状态 */
        a:link {
            color:#333;
            /* 取消下划线 */
            text-decoration: none;
        }
        /* 已经访问过的链接 我们点击过 */
        a:visited {
            color: orange;
        }
        /* 鼠标经过链接时候的状态 */
        a:hover {
            color: red;
        }
        /* 当我们点击的时候(按下鼠标，别松开的时候) */
        a:active {
            color: green;
        }
    </style>
</head>
<body>
    <a href="http://www.xiaomi.com">小米手机</a>
    <a href="http://www.dami.com">大米手机</a>
</body>
</html>
~~~

**通用兄弟选择器**

同层级，位置无需相邻

~~~css
p~span {
	color: red;
}
//与p同层级的所有span元素
~~~

**相邻兄弟选择器：**

同层级，紧接着的元素

~~~css
/* 图片后面紧跟着的段落将被选中 */
img + p {
  font-weight: bold;
}
~~~



**CSS属性：**

**font字体**

| 属性                                                         | 含义     |
| ------------------------------------------------------------ | -------- |
| `font-size: 大小`                                            | 字体大小 |
| `font-family: 字体`                                          | 字体样式 |
| `font-weight: 字体粗细`(normal(默认400)，bold(加粗700)，100-900) | 字体粗细 |
| `font-style：字体风格`                                       | 字体风格 |

综合写法：`font: font-style font-weight font-size font-family`

==font-size和font-family必须写==

**外观属性：**

| 属性                       | //////////                                                   |
| -------------------------- | ------------------------------------------------------------ |
| `color: 文本颜色`          | `(red,green,...)`，`(#FF0000,#FF6600)`，`(rgb(255,0,0),rgb(100%,0%,0%))`,`rgba(255,0,0,100%)` |
| `text-align: 文本对齐方式` | `left,right,center`                                          |
| `line-height: 行间距`      | 跟字体有关                                                   |
| `text-indent: 首行缩进`    | 跟`<p></p>`有关                                              |
| `text-decoration:文本装饰` | `none: 默认` `underline:下划线` `overline:上划线` `line-through: 删除线` |



**CSS背景：**

| 属性                                                         | /////                                                        |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `background-color:颜色`                                      | 背景颜色,默认是`transparent`                                 |
| `background-image: none|url`                                 | 背景图片                                                     |
| `background-repeat: repeat|no-repeat|repeat-x|repeat-y`      | `repeat:x和y轴平铺` `no-repeat:不平铺` `repeat-x:x轴方向平铺` `repeat-y:y轴上平铺` |
| `background-position: length||length` `background-position: position||position` | top\|center\|bottom\|left\|center\|right 访问名词            |
| `background-attachment: fixed|scroll`                        | 规定背景图片是固定的还是滑动的                               |



**权重：**

| 标签选择器           | 计算权重公式 |
| -------------------- | ------------ |
| 继承或者*            | 0000         |
| 每个元素(标签选择器) | 0001         |
| 每个类，伪类         | 0010         |
| 每个ID               | 0100         |
| 行内样式             | 1000         |
| !important           | 无穷大       |



**三种模式**

| display                   |                                                              |
| ------------------------- | ------------------------------------------------------------ |
| block(块级元素)           | 一行只能放一个，可以设置宽度和高度，容器的100%，容器可以包括任何标签 |
| inline(行内元素)          | 一行可以放多个，不可以设置宽度和高度，本身内容宽度，只能容纳文本或其他行内元素 |
| inline-block(行内块元素） | 一行可以放多个，可以设置宽度和高度，本身内容宽度             |



**盒子模型：**

![image-20230315195755731](C:\Users\sukiski\Desktop\CODE\hcj.assets\image-20230315195755731.png) 

**盒子边框(border)：**

| 属性                     | 作用                                                     |
| ------------------------ | -------------------------------------------------------- |
| `border-width: 单位长度` | 边框粗细(px)                                             |
| `border-style: 样式`     | `none(默认)`,`solid(实线)`,`dashed(虚线)`,`dotted(点线)` |
| `border-color`           | 边框颜色                                                 |

border-方位(top-bottom-left-right)-功能
可以修改各边的边框



`transition: all 时间`,`transform:translate,rotate,scale`

**animation**

| 属性                      | 描述                                                         |
| ------------------------- | ------------------------------------------------------------ |
| @keyframes                | 规定动画                                                     |
| animation                 | 所有动国属性的简写属性，除了animation-play-state属性         |
| animation-name            | 规定@keyframes动画的名称。（必须的）                         |
| animation-duration        | 规定动画完成一个周期所花费的秒或毫秒，默认是0。（必须的）    |
| animation-timing-function | 规定动画的速度曲线，默认是“ease”                             |
| animation-delay           | 规定动画何时开始，默认是0                                    |
| animation-iteration-count | 播放次数，默认是1                                            |
| animation-direction       | 规定动画是否在下一周期逆向播放，默认是normal,alternate逆播放 |
| animation-play-state      | 规定动画是否正在运行或暂停。默认是'running",还有'pause",     |
| animation-fill-mode       | 规定动画结束后状态，保特forwards回到起始backwards            |

