# HTML初级知识
#### h1~h6相关知识
> 1.h1~h6标签字体由大到小  2.h1~h6标签字体都是加粗  3.h1~h6标签默认为块级元素  4.文字上下之间有垂直空白间距

#### 注释

> 1.注释在浏览器中不会显示  2.注释可用于代码说明，提高代码可读性 3.注释标签里面不能嵌套注释标签

#### P标签

> 1.属于块级标签，单独一行，2.文段上下之间有间距

在HTML中标签尽量语义

#### 插入文本标签 ins

#### 内联样式 style 

#### base 标签

> 放在head第一个元素位置， 使用base标签必须具备href属性或者target属性或者两者都具备，在同一个文档中只有一个 base元素并且位于head元素内部

#### noscript 标签

> 当前浏览器不支持JavaScript脚本

#### a标签

> 进行页面跳转，发生邮件，进行下载，执行脚本

#### img

> src:相当于URL，路径地址。 alt:文字说明。 title:鼠标移上显示信息。loading：1.lazy：懒加载 ，2.eager：立即加载图片

#### map

> 不能单独使用，进行划分，常与area一起使用

#### area

> shape: circle(圆形)，rect（矩形）
>
> coords:定位坐标

#### audio标签

> 主要有MP3、WAV、Ogg格式
>
> autoplay：自动播放，loop：循环播放  muted：静音 。preload：预加载方式。

#### video标签

> 主要有MP4
>
> autoplay：自动播放，loop：循环播放  muted：静音 。preload：预加载方式。poster：播放之前指定一个画面

#### ul 无序标签  ol有序标签

加入reversed会变成倒叙，srart:开始序列  type：a、A、i

#### div 块级元素

> 属于一个容器标签

#### span 行内标签 可以理解为小容器

#### main 语义标签 放于boby中

##### aside旁白

#### 特殊符号

> &nbsp 空格，&lt 小于符号  &gt 大于符号 &times 叉号  &radic 对号 &Reg 已注册商标    & copy 版权  &Trade 商标 &yen 人民币符号   

#### 表格

##### colgroup 用于对表格中的列进行组合以便进行格式化

####  表单

> 提供可视化的数据控件，收集用户输入的数据并提交给服务器。
>
> 两部分组成：前端、后端。 后端：在服务器上处理前端提交的数据。前端：form表单 和其他一些前端控件组成

##### form标签

> 以表单形式提交数据，form标签是不可缺少的

1.accept-charset ：设置当前使用的编码

2.action：提交数据到服务器的URL

3.autocomplete：记忆功能，记录以往输入的信息，默认打开(true)

4.method：向后台提交数据的方式  [get(相对小数据)、post(相对数据大一点)]

5.enctype：

6.novalidate:如果使用这个属性在原表单需要验证，则不需要验证。

7.name：表单的名称，后台通过它来访问，JS也是通过它来进行一些事件

8.target：

#### `常用按钮`

1.input 空标签，只有属性

2.button按钮

3.CheckBox复选框按钮 可以多选

4.color 颜色控件

5.date日期控件

6.file文件控件

7.hidden 隐藏按钮

8.image图片按钮

9.month 日期按钮

10.number 数字按钮

11.password 密码按钮

12. radio 单选按钮
13. range 滑动控件
14. reset 重置按钮
15. search 搜索框
16. submit 提交按钮
17. text 普通文本输入框
18. time 时间分钟输入框
19. Tel 电话输入框 和text一样
20. url: url输入框
21. week 年周选择输入框



##### 属性

1.accept：常用类型 image/*，audio/*   video/*

2.alt: 只能与类型是img、iamge一起使用

3.autocomplete：只适用于text、search、url、tel、email、password、datepickers、range、color。

4.autofocus：自动获取焦点

5.checked：结合单选框

6.disabled：禁用控件

7.form：用于与表单建立联系

8.formaction：

9.formenctype：

10.formmethod：

11.max最大值 规定input元素的最大值，合法取值范围  适用于number、range、date、month、time、week、

12.min 最小值 规定input元素的最小值，合法取值范围 适用于number、range、date、month、time、week、

13.mexlength:限制字符数

14.multiple：一般和上传控件一起使用，可以多选，允许上传多个文件

15.name：规定控件的名称，在表单提交以后引用表单数据。只有设置了name属性的表单才能在提交表单时使用

16.pattern：属性规定用于验证定义的正则表达式，用于验证输入值的格式验证2. 一般用于URL 、src、email。3.请使用table属性来帮助用户

17.placeholder：在输入框中展示提示，该提示会在用户输入前提示，该属性适用于text、search、URL、email、Tel、password

18.readonly：只读

19.require：必填字段，适用于一下input类型，text、search、email、password，number、chekbox、file

20.src：图片提交按钮使用 对于input，且只能与该控件使用。他是定义图片按钮的URL

21.step：属性规定input元素的合法数字间隔，可以与max、min使用创建合法的值，该属性适用于number、range、date、datetime、month、week、time

22.value：对于类型为button、reset、submit 定义文本，对于text、password、hidden定义字段的初始值，对于CheckBox、radio、image用于固定其值

##### textarea  

> 多行文本框 常用 cols与rows

##### button

> 定义一个按钮 

##### select 下拉框 

> 下拉列表 常与option配合使用  	 size 控制下拉列表中可见选项的数目   	multiple 可以选择多个选项(Windows下按住Ctrl实现多选，Mac按住command实现多选)

##### option 定义下拉框中的一个选项

> 定义下拉列表的选项，不能单独使用配合select使用。
>
> value是为选项提供值	
>
> selected 设置该选项被选中 设置多个选项被选中是，会选择最后一个作为选择项	
>
> label  定义简短、简称 

##### optgroup 

> 对相关的选项进行分组   、其中label就是定义分组的名称

##### label 标签

> 为input元素定义标注或说明  for跟着要服务的ID  form是和表单建立连接

##### fieldset

> 表单元素分组      

##### legend 给fieldset设置分组名称

##### datalist  为input提供可能的选项，在input下利用list属性和要建立关系的dataliset连接

#### 元素的显示方式

##### 块级元素

> 在网页中单独成行的元素都是块级元素，送上至下排列  h1~h6 、div、p、pre、......
>
> 特点： 支持align，不设置宽度，默认占父元素宽度100%

##### 行内元素

> 在网页中可以多个标签在同一行中显示，从左到右排列。行内元素设置宽高上下边距均无效。

##### 行内块元素 

> 具有块级元素特征的行内元素

##### table元素

> 表格的宽高由内容来决定，注意：很多时候也就table理解为一种特殊的块级元素

