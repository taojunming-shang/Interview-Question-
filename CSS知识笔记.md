#  CSS知识笔记

> 层叠样式表    用来实现网页布局，美化网页
>
> 常用css的几种方式：
>
> 内联样式：直接在标签的style属性里写样式代码  优点：优先级最高  缺点：复用性不高  文档臃肿，看着混乱 不方便样式的修改和管理。
>
> 外联样式：样式代码写在一个单独的文件里，通过一定方式与文件建立联系后使用    优点：便于管理，复用性高，优先级居中  缺点：复用性仅限当前文档，也会让文档变得臃肿。
>
> 内嵌样式：在HTML文档的style里写样式代码  优点：复用性最高，可多个网页使用，便于样式代码的修改，管理、扩展。  缺点：优先级最低。

特点：

> 层叠性：样式可以层叠使用 
>
> 继承性：子标签继承父标签的样式，并不是全部都可继承只能继承如 text、font-、line-这些开头的都可以继承
>
> 优先级：解决元素应用样式有冲突时，有限考虑使用哪个样式，级别越高，越优先

语法：

> 选择器 {属性名：属性值;}    一个属性名与属性值单独成行，便于阅读

### ID选择器

> #id选择器为该id选择器名的HTML元素指定该id选择器定义的样式

### 类选择器

> 它是组织样式代码的一种方式，该方式可以在一个页面中被多次使用

### 标签选择器

> 对应标签元素的显示样式

#### ID选择器>类选择器>标签选择器>通配符

### 伪类选择器

#### 链接伪类

> link、hover、visited、active：可以和基础选择器中的任何一个配合使用，但一定具有链接属性，否则没有效果，和其他属性使用的时候需满足所有条件才有效果
>
> 书写顺序：link、 visited、hover、active

#### 目标选择器

> target  
>
> 定义描点链接过去的样式
>
> 可以和基础选择器中的任何一个配合使用，但一定具有链接属性，否则没有效果，和其他属性使用的时候需满足所有条件才有效果

#### 状态伪类

> checked :
>
> 主要是与radio、CheckBox控件使用，可以和基础选择器中的任何一个配合使用，组合使用时需要满足所有条件。

> enabked选择器与disabled选择器：一般用于表单元素。可以和基础选择器中的任何一个配合使用，组合使用时需要满足所有条件。

#### 否定伪类

> :not(选择器){}
>
> 定义除开括号里定义的选择器外其他元素的样式

#### 范围伪类

> :in-range{} 定义的值在指定区域内时显示  :out-of-range{} 定义的变量在不在指定区域内时显示

#### 必选非必选选择器

> :optional{}   :required{}
>
> 只适用于input select 和textarea

#### 仅读或读写伪类

> :read-only{}  :read-write{}

#### 结构伪类

##### :nth-child选择器

> 定义父元素中的第n个子元素的样式
>
> 



### 颜色表达方式

> 颜色名(red、green) 、十六进制(#f0f0f0)、 RGB(rgb(0,18,123))

### CSS背景色

#### 背景颜色 

> background-color：设置背景颜色

#### 背景图片

##### background-image 

> 设置元素的背景图片
>
> 常用值：url(图片的路径)       linear-gradient() 图片的线性渐变        radial-gradient() 图片的径性渐变  repeating-gradient() 图片的重复线性渐变      repeating-radial-gradient() 图片的重复径性渐变

##### background-position

> 设置背景图片显示的位置

一、值表达方式：

方式一：left top  center  right  bottom  日常中我们常常只写一个方位词，默认为方位词 center。

方式二：x% y%  第一个为水平方向，第二个为垂直

方式三：xpos ypos  左上角是0 单位可以为像素或者任何其他css单位 。只指定一个值的时候，其他的值为50%；

#### background-size

> 定义图片大小
>
> 值表达：固定值  设置背景图片宽高 只设置一个值是，另一个自动设为auto
>
> 百分比：计算相对于背景定位区域的百分比
>
> cover：此时会保持图片的纵横比并将图片缩放成将完全覆盖背景定位区域的最大或最小
>
> contain：此时会保持图片的纵横比并将图片缩放成将适合背景区域的最大或最小

#### background-repeat

> 设置背景图片平铺
>
>  repeat ：背景图片沿水平和垂直方向重复
>
> repeat-x： 沿水平方向重复
>
> repeat-y：沿垂直方向重复
>
> no-repeat:不重复

#### background-attachment

> 定义背景图片是固定或移动跟随页面的其余部分滚动   fixed 固定    scroll 滚动

简写：background：跟所有属性，可只有部分属性

### CSS文本

#### color

> 定义字体颜色

#### letter-spacing

> 定义字符间距  值可为正值或负值的数字

#### line-height

> 定义行高   如果行高高度大于字体大小，该文本将在指定的行高内，以垂直居中的方式显示， 纯文本的垂直对齐，不能用vertical-align 必须要line-height

#### text-align

> 定义文本对齐的方式   justify  文本两端对齐

#### text-decoration

> 定义文本修饰 
>
> underline 文本下划线     overline 文本上划线    line-through  文本横穿线    blink  文本闪烁(当前无效)

#### text-indent

> 文本首行缩进

#### text-shadow

> 文本阴影 h-shadow 水平阴影位置 允许负值   v-shadow 垂直阴影位置 允许负值    blur 可选，模糊的距离    color可选，阴影颜色

#### text-transform

> 定义文本的大小写
>
> capitalize：每个单词首字母大写     lowercase：文本全部小写   uppercase：文本首字母大写

#### white-space

> 定义文空白的处理方式
>
> nowrap 让文本不换行。 

#### text-align-last

> 当text-align设置为justify时，定义最后一行的对齐方式

#### text-overflow

> 文本溢出时显示的样式

### CSS字体

#### font-family

> 定义字体的类型
>
> 可以多个字体名称，是防止某个字体失效时有其他字体效果

#### font-size

> 设置文字大小

#### font-style

> 定义字体样式
>
> 值：nomal  标准字体样式    italic   字体为斜体    oblique  字体倾斜
>
> 说明：italic和oblique表现出来的效果一样，不同的是：italic是使用字体的倾斜，oblique让没有倾斜的文字做倾斜处理

#### font-weight

> 定义文本的粗细
>
> 值：normal  标准   bold 粗体   bolder  更粗一点   lighter    比标准更细一点   
>
> 100~900

#### font-variant

> 定义以小型大写字母的字体显示文本

#### font

> 字体样式的简写
>
> 顺序为  style、variant、weight、size、line-height、family   其中size和family是必须的

### CSS列表相关属性

#### list-style-type

> 定义标签的符号

#### list-style-image

>定义列表标记图片

#### list-style-position

>定义列表标记的位置

#### list-style

> 在一个声明中设置所有的属性
>
> 顺序：type-> position ->image

### CSS表格相关属性

#### border-collapse

> 定义是否合并表格

#### border-spacing

>定义相邻单元边框之间的距离
>
>值：有px、em等单位，不允许负值
>
>该属性值在border-collapse:collapse;无效

#### caption-side

>定义表格标题的位置  top  、bottom

#### empty-cells

>定义是否显示表格中的空单元格上的边框和背景    hide  show
>
>该属性值在border-collapse:collapse;无效

#### table-layout

>表格的布局算法  automatic 默认 由内容设定   fixed  由表格宽度和列宽度设定

### CSS盒子模型

> HTML中所有标签都可以看成一个盒子

#### CSS尺寸：width、height  

> 只有块级元素或行内块元素才能设置宽高，其余需要使用display来设定

#### CSS边距

> 外边距：margin  margin设置相邻盒子上下边距的时候，间距会是其中最大的间距，而不是上下间距之和。
>
> margin 简写时顺序为上右下左

> 内边距：padding   和margin用法一致

#### CSS边框

> border简写的时候不能定义四个边框的样式，只能统一定义，不可以对四个边设置不同的值

#### 边框角 radius

> 设置边框对应角的样式

#### 图片边框样式

1.border-image-source

> 定义边框图片的路径
>
> 值  none 没有   url 路径

2.border-image-slice

> 图像边框的向内偏移
>
> 值     位置值：数字或百分比   fill：是否保留图像的中间部分 设置了值则保留中间部分，不设置该值则不保留中间值，作透明处理

#### 轮廓样式 outline

> 与border用法一样  width、style、color

#### 框阴影样式

> box-shadow  定义框阴影样式   
>
> h-shadow(水平阴影，正值向下，负值向上)、v-shadow(垂直阴影，正值向下，负值向上)、blur(模糊距离)、 spread(阴影大小)、color

### CSS定位

#### display 

> 定义元素生产的框的类型
>
> 值：  none—此元素不会被显示     block— 显示为块级元素    inline—内联元素    inline-block—行内块元素     marker—css中有值marker   table—块级表格显示     inline-table—内联表格显示

#### position

> 元素定位方式
>
> 默认—>static 没有定位  relative：相对定位的元素，相对定位常被用来作为绝对定位元素的容器快      absolute：绝对定位元素，绝对定位的元素位置相对与最近的已定位的父元素，脱离文档流       fixed：固定定位      sticky：粘性定位 设置用户滚动的位置，

#### top等方位

> 定义一个定位元素的对应外边距边界与其包含块对应界之间的偏移  

> 高度塌陷：在需要移动元素前加 br 、行内块元素、

#### float

> 定义元素浮动  left、right、none

#### clear

> 定义元素的那一侧不允许其他元素浮动      

#### overflow

> 如何处理内容溢出元素框的方式
>
>  visible：默认值呈现在元素框之外   hidden：超出元素框意外的不可见     scroll：内容会被修剪，但浏览器会系那是滚动条以便查看其余的内容     auto：内容被修剪，则浏览器会显示滚动条以便查看其余内容

#### z-index

> 定义元素的层叠顺序，层叠顺序高的元素都会处于层叠顺序较低的元素上面

#### visibility

>定义元素是否可见
>
>visible：元素可见     hidden：元素不可见     collapse：表格中使用时，此值可以删除一行或一列，但不影响布局被占用的空间会留给其他内容使用，如果用在其他元素上会呈现hidden

#### cursor

>鼠标样式

#### clip

> 裁剪绝对定位元素 

### CSS渐变

#### 线性渐变 

> linear-gradient
>
> 从一个方向向另一个方向的颜色渐变
>
> 值 ： 
>
> 方向：    to top(渐变从下到上)  to botoom(渐变从上到下) to top left(从右下角到左上角)   to top right(从左下角到右上角) ....
> 
> 角度：
> 
> 颜色：
> 
> 颜色位置：固定值   百分比   
重复线性渐变
> repeating-linear-gradient
>
> 使用方法和线性渐变一致  
>
> 说明：1.重复线性渐变位置不能设置为100%，否则就不会有重复效果
>
> 2. 颜色值如果使用rgba，可创建减弱变淡的效果
> 3. 如果使用了颜色位置，则颜色在前，中间空格隔开，后面是颜色线位置

#### 径向渐变

> radial-gradient
>
> 从一个点到四周的颜色渐变
>
> 值
>
> 渐变形状： Circle   ellipse(椭圆 ，默认)
>
> 渐变大小：
>
> 预定值：closest-side (最近的边)  closest-Corner(最近的叫)   farthest-side、farthest-corner (意思相反)
>
> 固定值：
>
> 百分比：
>
> 说明：
>
> 1.无论固定值还是百分比，正规写法都是两个值
>
> 2.百分比和固定值可以混用
>
> 3.当一个值或者两个值相等是其形状为圆，而两个值不一样的时候则是椭圆
>
> 4.若渐变而圆形，则渐变大小不能为百分比，椭圆可以使用百分比
>
> 圆心位置：方位值，固定值，百分比



### 伪类选择器

 #### 格式验证伪类

> invalid{}(非法)   :valid{}(合法)    定义表单元素

### 结构伪类

##### :nth-child

> 定义父元素中第n个子元素样式

##### :nth-last-child

>定义父元素中倒数第n个子元素样式

##### :nth-of-type

> 定义父元素中顺数第n个子元素的样式

##### :nth-last-of-type

> 定义父元素中倒数第n个子元素的样式

##### :first-child

> 父元素中第一个子元素

##### :last-child

> 父元素中倒数第一个子元素

##### :root

> 根节点选择器  HTML

##### :empty 

> 定义空元素样式

##### :only-child

> 设置父级元素下有且只有一个元素

##### first-of-type

>父元素下相同元素中的第一个元素

##### last-of-type

>父元素下相同元素中的最后一个元素

##### only-of-type

> 父元素中有且只有一个子元素的样式

### 属性选择器

> 定义所有设置了某属性的元素的样式

常用表达方式：

1.[属性=属性值]

2.[属性~=属性值]：包含属性值

3.[属性|=属性值]：设置了某属性且值仅包含给定的值或以给定值加- 符号开头的元素的样式  注 属性值必须是单独的单词或以这个值加 - 开头

4.[属性^=属性值]：以属性值开头的

5.[属性$=属性值]：以属性值结尾的

6.[属性*=属性值]：只要存在属性值即可

### 伪元素选择器

##### :after

> 在某选择器后面加入内容或设置样式
>
> 常与content配合使用

##### :before

>在某选择器前面加入内容或设置样式

##### :first-letter

> 设置第一个字符的样式

##### :first-line

>设置元素下的第一行的样式

##### ::selection

> 设置文字被选中状态下的样式

### 组合选择器

#### 后代选择权

> 定义父元素下所有满足条件的后代元素应用的样式

##### 子选择器 

> 定义父元素下所有满足条件的直接子元素应用的样式

#### 兄弟选择器

> 兄选择器~弟选择器{}
>
> 定义兄元素下所有满足所有条件弟元素应用的样式

#### 相邻兄弟选择器

> 兄选择器+弟选择器{ }
>
> 兄元素下紧挨着的第一个满足所有条件弟元素应用的样式

### transform  变形

> 用于实现元素转换的关键字

##### transform-origin

> 定义变形的原点
>
> 值： 预定值：（ x ->left、center、right     y->top、 center、bottom  ）   固定值、百分比

##### translate() 平移函数

> 1.translateX() 用于元素的水平移动，正值向右移动，负值向左移动
>
> 2.translateY() 用于元素的垂直移动 正值向下，负值向上
>
> translate(x,y) 同一个值时，x、y一样

##### scale() 缩放函数

> 可以只设置一个值

##### rotate() 旋转函数

##### skew() 倾斜函数 deg

### 3D转换

##### transform-style

> 定义是2D还是3D

##### transform-origin

> 定义元素发生转换时的原点
>
> 值： 预定值：（ x ->left、center、right     y->top、 center、bottom     z->固定值 ）   固定值、百分比

##### perspective

> 定义3D的视距 
>
> 值：固定值

##### perspective-origin

> 定义观察到的物体的某点
>
> 值：（ x ->left、center、right     y->top、 center、bottom  ）  
>
> 必须与perspective配合

##### backface-visibility

> 定义元素背面向屏幕的时候是否可见

### CSS过度

> 元素从一个样式变换到另一个样式的中间过程  

##### transition-property

> 指定要应用过度的css属性
>
> 值 ：all

##### transition-delay

> 定义过度开始的时间

##### transition-duration

> 过度效果花费的时间

##### transition-timing-function

> 1.ease 快到慢     2.linear  匀速   3.ease-in  渐快   4.ease-out  减慢    5.ease-in-out  先加速在减速(渐显渐隐)   6.cubic-bezie(n,n,n,n) 自定义贝尔赛曲线效果

### CSS动画

> 使元素从一种样式逐渐变化为另一种样式的效果

##### @keyframes 

##### animation-name

> 指定@keyframes  动画的名称

##### animation-duration

> 完成动画一个周期所花费的时间

##### animation-timing-function

> 定义动画的曲线 1.ease 快到慢     2.linear  匀速   3.ease-in  渐快   4.ease-out  减慢    5.ease-in-out  先加速在减速(渐显渐隐)   6.cubic-bezie(n,n,n,n) 自定义贝尔赛曲线效果

##### animation-delay

> 定义动画延迟多久开始

##### animation-iteration-count

> 定义播放的次数    infinite(动画重复播放)

##### animation-direction

>定义是否循环交替反向播放动画
>
>值：1.normal（正常播放） 2.reverse（反向播放）  3.alternate（动画在奇数次为正向播放 ，偶数次为反向播放）  4.alternate-reverse（动画在奇数次为反向播放 ，偶数次为正向播放）

##### animation-play-state

> 动画是否正在运行或暂停
>
> 值：paused  暂停动画    running   运行动画

##### animation-fill-mode

> 动画停之后，留在位置，不会到最初状态
>
> forwards 停止后，就停留，不会到原始状态
>
> backwards  有动画推迟的情况下，把画面定个在动画的第一帧等待，当推迟结束后继续动画
>
> both  两者兼具

##### animation

> 简写属性
>
> 除了推迟时间和动画运行时间外，没有顺序要求



### CSS多列

##### column-count

> 定义需要的分割的列数

##### column-gap

> 定义列与列之间的间隙

##### column-rule-color

> 定义两列间边框颜色

##### column-rule-style

> 定义两列间的样式

##### column-rule-width

> 定义两列间的宽度

##### column-rule

> 简写 样式、宽度、颜色  样式不可缺，

##### column-span

> 定义元素跨越多少列
>
> 值：  1、all

##### column-width

> 定义列的宽度                                            

##### columns

> column-width与column-count 的简写属性

##### column-fill

> 定义填充列  （该值在大多数浏览器一下无效 ）



### CSS弹性盒子

> 是一种当页面需要适应不同屏幕大小及设备类型确保元素能适当的布局

> 弹性盒子有弹性容器和弹性子项目组成
>
> main  axis  主轴   
>
> cross axis  交叉轴

#### 容器属性

##### flex-direction

> 定义主轴的方向(即内容排列方向)应用咋容器元素上
>
> 值：1.row 主轴为水平方向 ，从左到右  2.row-reverse  主轴为水平方向，从右到左  3.column：主轴为垂直方向，从上到下   4.column-reverse  主轴为垂直方向，从下到上

##### flex-wrap

> 定义容器内项目是否换行
>
> 值：1. nowrap：子项目打死不换行  2.wrap 子项目超出容器时从上到下   3. wrap-reverser  子项目主轴尺寸超出容器时从下到上换行

##### flex-flow

> flex-wrap与flex-direction的综合属性
> 

##### justify-content
> 定义项目在主轴的对齐方式，应用在弹性容器上
> 值：1.flex-start  主轴开始点对齐  2. flex-end  主轴结束点对齐  3.center  居中对齐  4.space-between 两端对齐  5.space-around  每个项目两侧的间隔相等

##### align-items
> 定义项目在交叉轴上的对齐方式 应用在弹性容器上
> 值：1.flex-start  交叉轴开始点对齐  2. flex-end  交叉轴结束点对齐  3.center  交叉点对齐  4.stretch  如果项目未设置高度或者设置为auto，将占满整个容器高度，设置了高度则以高度为主 5. baseline 项目的第一行文字的基线对齐

##### align-content
> 定义多根轴线的对齐方式，
>
> 值：1.flex-start    2. flex-end    3.center    4.space-between 5.space-around  6.stretch  

### 子项目属性
##### order
> 定义项目在容器中的排列顺序
> 说明：值越小越靠前，可以为负值，值相同时按从下到上出场顺序，值不符合规定时视为0，

##### align-self

> 设置子项目自身在交叉轴方向上的对齐方式
> 值：1.flex-start    2. flex-end    3.center    4.stretch   5. baseline   6.auto  如果值为auto，则其计算值为元素的父元素的align-items 值，如果父元素也没有align-items，则值为stretch

##### flex-basis

> 设置main size 的大小
>
> 值：auto 默认值自适应     百分比：相对父元素的宽或高（主轴决定）  固定值
>
> 说明：1.主轴方向决定该属性，如果为x轴，该属性等同于width，主轴为Y ，则该属性等同于height   2.同时设置该属性的宽高 则 宽高无效   3.该属性支持简写的flex 如果用用width、height 则没办法简写只能分开设置  该属性只会在flex上生效，  也只对（非绝对定位）flex项目生效

##### flex-grow

> 设置项目的发大率，让项目放大至填充整个父元素
>
> 说明：项目中的main size 总和大于等于父元素的则失效   ，值为无效是，视为0  同一时间与flex-shrink只有一个有效。

##### flex-shrink

> 设置项目缩小率
>
> 说明：项目中的main size 总和大于等于父元素的则失效   ，值为无效是，视为0  同一时间与flex-shrink只有一个有效。

##### flex

> flex-grow  flex-shrink  flex-basis简写属性
>
> 值： auto：等同于flex: 1 1 auto        none：等同于flex: 0 0 auto

### CSS媒体查询

> 涉及内容：1.meta标签：  在头部需要添加  width=device-width：网页宽度等于设备宽度    initial-scale=1.0  初始化缩放比例是1.0   maxmum-scale=1.0  最大缩放的比例为1.0 
>
> minimun-scale=1.0   最小的比例为1.0     user-scalable=yes|no(1)|0 是否允许用户缩放

### Bootstrap框架

