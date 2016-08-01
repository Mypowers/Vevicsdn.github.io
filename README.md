# mycsdn.github.io
Vevi的CSDN博客
#关于 CSS 的一些属性问题
##display
###display 是CSS中最重要的用于控制布局的属性。每个元素都有一个默认的 display 值，这与元素的类型有关。对于大多数元素它们的默认值通常是 block 或 inline 。一个 block 元素通常被叫做块级元素。一个 inline 元素通常被叫做行内元素

###**inline**

span 是一个标准的行内元素。一个行内元素可以在段落中 <span> 像这样 
</span> 包裹一些文字而不会打乱段落的布局。 a 元素是最常用的行内元素，它可以被用作链接。

**none**

另一个常用的display值是 none 。一些特殊元素的默认 display 值是它，例如 script 。 display:none 通常被 JavaScript 用来在不删除元素的情况下隐藏或显示元素。

**它和 visibility 属性不一样。把 display 设置成 none 不会保留元素本该显示的空间，但是 visibility: hidden; 还会保留。**

**flex**
display：flex 这个属性很强大，在父容器中加入 display:flex(考虑浏览器兼容可以加上前缀例如-webkit-flex),然后在子元素中加入 flex:1（-webkit-flex:1）就会将剩余的宽度或者高度都给这子元素，当多个子元素使用此属性时，则按照数字分配;
在之前的一篇文章里我讲过居中的方法，使用的是定位的方法，学到这里我们可以学到更加简单的方法，只需要在父元素添加以下的三个属性就可以实现

###display: flex;

###align-items: center;

###justify-content: center;

额外加分点

就像我之前讨论过的，每个元素都有一个默认的 display 类型。不过你可以随时随地的重写它！虽然“人工制造”一个行内元素可能看起来很难以理解，不过你可以把有特定语义的元素改成行内元素。常见的例子是：把 li 元素修改成 inline，制作成水平菜单。
#width 与 max-width
当我们使用块级元素，比如 div 时通常一开始会给一定的 width 和 height，这也是为了避免占满整个浏览器，然而当缩小化浏览器时，浏览器的宽高可能就没有我们设置的元素宽高这么大了，要想我们的元素也随着浏览器的缩小而缩小，我们就需要使用 max-width.

#文本超出显示省略号
#box-sizing
当设置该属性的值为border-box,此属性的用途主要为我们带来的便利是可以忽略边框的宽度和内边距对我们的宽度计算带来的干扰

#清除浮动clear
属性值有 left ，right 和 both.顾名思义就是清除上层 float 属性，比如在图片周围文字环绕我们使用 float 属性的时候，如果想要动态取消文字环绕效果则可以使用该属性
#分列显示文本
H5 新增了一个 section 可以用于表达文章文本，但是当我们想要实现分列显示呢，同样我们可以有column-count(指定列数) column-gap(列与列之间的距离)，当然了也要指定好宽度才行，需要注意的是该属性是新标准，在IE9和Opera Mini暂不支持，所以使用时需要加上前缀
#单选按钮radio
对于经常不写 name属性的我来说，有一次被 radio 给气死，原因就是我没有写 name 属性，从而不管我怎么把鼠标点烂还是无法实现单选
