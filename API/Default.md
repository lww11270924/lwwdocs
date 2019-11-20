
[hc](hc.hcml).Default
---------------------

工具对象，包含hc默认的配置参数和一些工具函数  
  
不要直接修改这个对象的属性值，如果需要改变hc的默认配置，需要通过全局的hcconfig变量名指定，hc系统只在初始化时读取hcconfig的配置信息，因此hcconfig必须在引入hc.js包之前初始化好，运行状态时修改hcconfig变量不会再起作用，示例代码如下：
### Example

    <script>
      hcconfig = {
          Color: {
              label: '#000',
              highlighc: '#1ABC9C',
          },
          Default: {
              toolTipDelay: 100,
              toolTipContinual: true
          }
      };
    </script>
    <script src="hc.js"></script>

### Members

#### static accordionViewCollapseIcon :String

折叠组件关闭状态图标

#### static accordionViewExpandIcon :String

折叠组件展开状态图标

#### static accordionViewLabelColor :color

折叠组件文字颜色

Default Value:

*   #FFF

#### static accordionViewLabelFont :String

折叠组件文字字体

Default Value:

*   12px arial, sans-serif

#### static accordionViewSelectBackground :color

折叠组件选中背景

Default Value:

*   #1ABC9C

#### static accordionViewSelectWidth :Number

折叠组件选中宽度

Default Value:

*   3

#### static accordionViewSeparatorColor :color

折叠组件分隔条颜色

#### static accordionViewTitleBackground :color

折叠组件抬头背景

Default Value:

*   #2C3E50

#### static animEasing :function

默认动画效果函数

Default Value:

*   function (m){return m\*m}

#### static autoHideScrollBar :boolean

决定组件的滚动条默认是否自动隐藏，true为自动显示和隐藏，false则需要滚动时一直显示不会自动隐藏

Default Value:

*   true

#### static autoMakeVisible :boolean

决定Data元素被选中时，组件是否自动滚动到Data元素可见位置

Default Value:

*   true

#### static baseZIndex :Number

指定组件基准CSS的ZIndex值，改值仅在将hc与其他第三方组件混合使用时根据需要设置"

#### static compStack :Array

矢量组件comp嵌套堆栈，矢量组件comp可嵌套定义，通过改参数能得到当前嵌套层次信息

#### static dashPattern :Array

连线或多边形等图形的默认虚线样式

#### static devicePixelRatio :Number

设备像素比，hc系统自动取至window.devicePixelRatio，某些特性情况需要为mobile应用牺牲精度节省内存时可以强制设置为较小值

#### static disabledBackground :color

组件无效时的背景色

#### static disabledOpacity :Number

组件无效时的透明度

#### static edgeGroupAgentFunc :function

此函数返回连线组的代理连线，edges为hc.List类型的hc.Edge对象数组，默认返回edges.get(0)，可重载自定义规则

#### static graph3dViewAttributes :Object

Graph3dView组件初始化WebGL上下文参数，一般无需改动

Default Value:

*   null

#### static graph3dViewAxisXColor :color

Graph3dView组件显示x轴线颜色

Default Value:

*   \[1,0,0,1\]

#### static graph3dViewAxisYColor :color

Graph3dView组件显示y轴线颜色

Default Value:

*   \[0,1,0,1\]

#### static graph3dViewAxisZColor :color

Graph3dView组件显示z轴线颜色

Default Value:

*   \[0,0,1,1\]

#### static graph3dViewCenter :Array

Graph3dView组件投影呈现时，眼睛最终锁定的目标中心位置

Default Value:

*   \[0,0,0\]

#### static graph3dViewCenterAxisVisible :Boolean

Graph3dView组件屏幕中心点x|y|z三个轴线是否可见

Default Value:

*   false

#### static graph3dViewEditSizeColor :color

Graph3dView组件在编辑状态图元拉伸标识颜色

Default Value:

*   \[1,1,0,1\]

#### static graph3dViewEye :Array

Graph3dView组件投影呈现时，眼睛观察点所在位置

Default Value:

*   \[0,300,1000\]

#### static graph3dViewFar :Number

Graph3dView组件投影呈现内容的最远距离，该值可根据场景最远范围进行调节设置

Default Value:

*   10000

#### static graph3dViewFirstPersonMode :Boolean

Graph3dView组件是否为第一人称交互方式

Default Value:

*   false

#### static graph3dViewFogColor :color

雾颜色

Default Value:

*   white

#### static graph3dViewFogDisabled :Boolean

是否关闭雾化效果

Default Value:

*   true

#### static graph3dViewFogFar :Number

代表从该距离之后物体完全看不清

Default Value:

*   2000

#### static graph3dViewFogNear :Number

代表从该距离起物体开始受雾效果影响

Default Value:

*   1

#### static graph3dViewFovy :Number

Graph3dView组件在透视投影方式下的y轴张角弧度（Field of view）

Default Value:

*   0.7853981633974483

#### static graph3dViewGridColor :color

Graph3dView组件显示xz面的网格线颜色

Default Value:

*   \[0.4,0.75,0.85,1\]

#### static graph3dViewGridGap :Number

Graph3dView组件显示xz面的网格行列间距

Default Value:

*   50

#### static graph3dViewGridSize :Number

Graph3dView组件显示xz面的网格行列数

Default Value:

*   50

#### static graph3dViewGridVisible :Boolean

Graph3dView组件是否允许显示xz面网格

Default Value:

*   false

#### static graph3dViewHeadlighcColor :Array

头灯颜色

Default Value:

*   \[1,1,1,1\]

#### static graph3dViewHeadlighcDisabled :Boolean

是否关闭头灯效果

Default Value:

*   false

#### static graph3dViewHeadlighcIntensity :Number

头灯强度，默认为1，大于1增强，小于1减弱

Default Value:

*   1

#### static graph3dViewHeadlighcRange :Number

头灯影响范围，默认为`0`代表可照射到无穷远处，如果设置了值则光照射效果随物体远离光影而衰减

Default Value:

*   0

#### static graph3dViewHeadlighcRange :Number

头灯影响范围，默认为`0`代表可照射到无穷远处，如果设置了值则光照射效果随物体远离光影而衰减

Default Value:

*   0

#### static graph3dViewMouseRoamable :Boolean

Graph3dView组件在第一人称交互方式时，鼠标是否能漫游

Default Value:

*   true

#### static graph3dViewMoveStep :Number

Graph3dView组件键盘控制移动的步进

Default Value:

*   15

#### static graph3dViewNear :Number

Graph3dView组件投影呈现内容的最近距离，该值在可接受的范围内尽量设置较大值有利于呈现精度

Default Value:

*   10

#### static graph3dViewOriginAxisVisible :Boolean

Graph3dView组件原点x|y|z三个轴线是否可见

Default Value:

*   false

#### static graph3dViewOrtho :Boolean

Graph3dView组件是否显示为正交投影方式

Default Value:

*   false

#### static graph3dViewOrthoWidth :Number

Graph3dView组件正交投影方式下屏幕宽度内显示的逻辑宽度值

Default Value:

*   2000

#### static graph3dViewPannable :Boolean

Graph3dView组件是否允许按Shift键进行手抓图平移

Default Value:

*   true

#### static graph3dViewRectSelectable :Boolean

Graph3dView组件是否允许框选

Default Value:

*   true

#### static graph3dViewRectSelectBackground :color

Graph3dView组件框选背景

Default Value:

*   rgba(0,0,0,0.35)

#### static graph3dViewResettable :Boolean

Graph3dView组件是否允许按空格键复位，复位调用了Graph3dView#reset()函数，该函数会重置Graph3dView的eye|center|up三个参数

Default Value:

*   true

#### static graph3dViewRotatable :Boolean

Graph3dView组件是否允许进行旋转中心或方位操作

Default Value:

*   true

#### static graph3dViewRotateStep :Number

Graph3dView组件键盘控制旋转的步进

Default Value:

*   0.05235987755982988

#### static graph3dViewUp :Array

Graph3dView组件投影呈现时，摄像镜头垂直朝上方向

Default Value:

*   \[0,1,-1e-7\]

#### static graph3dViewWalkable :Boolean

Graph3dView组件是否允许前进后退操作

Default Value:

*   true

#### static graph3dViewZoomable :Boolean

Graph3dView组件是否允许缩放

Default Value:

*   true

#### static graphViewAutoScrollZone :Number

GraphView组件中拖动图元到边缘时会自动滚动，该参数决定开始自动滚动的区域范围，设置为0或负数则代表关闭自动滚动功能

Default Value:

*   16

#### static graphViewEditPointBackground :color

GraphView组件编辑点背景颜色

Default Value:

*   #D9D9D9

#### static graphViewEditPointBorderColor :color

GraphView组件编辑点边框颜色

Default Value:

*   #2C3E50

#### static graphViewEditPointSize :Number

GraphView组件编辑点大小

Default Value:

*   7

#### static graphViewPannable :Boolean

决定GraphView组件是否允许手抓图操作

Default Value:

*   true

#### static graphViewRectSelectable :Boolean

决定GraphView组件是否允许按Ctrl键进行框选操作

Default Value:

*   true

#### static graphViewRectSelectBackground :color

GraphView组件框选背景颜色

Default Value:

*   rgba(0,0,0,0.35)

#### static graphViewRectSelectBorderColor :color

GraphView组件框选边框颜色

Default Value:

*   #2C3E50

#### static graphViewResettable :Boolean

决定GraphView组件按空格键是否允许复位，复位调用了GraphView#reset()函数，该函数默认会调用setZoom(1)和setTranslate(0, 0)

Default Value:

*   true

#### static graphViewScrollBarVisible :Boolean

决定GraphView组件是否显示滚动条

Default Value:

*   true

#### static handleImageLoaded :function

图片在加载之后的回调函数

##### Example

    hc.Default.handleImageLoaded = function(name, img) {
    
    }

#### static handleModelLoaded :function

模型在加载之后的回调函数

##### Example

    hc.Default.handleModelLoaded = function(name, model) {
    
    }

#### static handleUnfoundImage :function

无法加载图片资源时会调用该函数，默认访问空，可自定义返回一个默认的图片

##### Example

    hc.Default.handleUnfoundImage = function(name, url) {
    
    }

#### static hitMaxArea :Number

进行框选判断时为了避免内存占用过大，hc会根据最大面积限制进行缩放判断，该参数一般无需改动

Default Value:

*   3000

#### static imageGradient :String

默认图片的渐进色类型

Default Value:

*   linear.northeast

#### static isTouchable :boolean

判断是否为触屏可Touch方式交互，hc系统一般会自动判断，对于极少数hc无法正确识别的系统下，可以通过配置强制指定

#### static labelColor :color

默认文字颜色

Default Value:

*   #000

#### static labelFont :font

默认文字字体

Default Value:

*   12px arial, sans-serif

#### static labelFont :font

默认文字字体

Default Value:

*   12px arial, sans-serif

#### static labelSelectColor :color

选中状态下文字颜色

Default Value:

*   #fff

#### static lineCap :String

线条末端线帽的样式，可选值为butt|round|square

Default Value:

*   butt

#### static lineJoin :String

当两条线交汇时创建边角的类型，可选参数为：bevel|round|miter

Default Value:

*   round

#### static listViewLabelColor :color

列表组件文字颜色

Default Value:

*   #000

#### static listViewLabelFont :String

列表组件文字字体

Default Value:

*   12px arial, sans-serif

#### static listViewLabelSelectColor :color

列表组件文字选中颜色

Default Value:

*   #FFF

#### static listViewRowLineColor :color

列表组件行线颜色

Default Value:

*   #D9D9D9

#### static listViewRowLineVisible :Boolean

列表组件行线是否可见

Default Value:

*   false

#### static listViewSelectBackground :color

列表组件选中背景色

Default Value:

*   #1ABC9C

#### static numberListener :function

数字类型监听器，该监听器将使得input文本输入框只允许输入数学相关字符

##### Example

    numberListener: (function(){
         var map = {
             46: 1,
             8: 1,
             9: 1,
             27: 1,
             13: 1,
             109: 1,
             110: 1,
             189: 1,
             190: 1
         };
         return function(e){
             var keyCode = e.keyCode;
             if(map[keyCode] || (keyCode === 65 && Default.isCtrlDown(e)) || (keyCode >= 35 && keyCode <= 39)){
                 return;
             }
             if ((e.shiftKey || (keyCode < 48 || keyCode > 57)) && (keyCode < 96 || keyCode > 105)) {
                 e.preventDefault();
             }
         };
     })()

#### static pinchZoomIncrement :Number

默认双指触屏Touch方式缩放步进

Default Value:

*   1.08

#### static propertyViewBackground :color

属性组件背景

Default Value:

*   #ECF0F1

#### static propertyViewCollapseIcon :String

属性组件合并图标

#### static propertyViewColumnLineColor :color

属性组件列线颜色

Default Value:

*   #D9D9D9

#### static propertyViewColumnLineVisible :Boolean

属性组件列线是否可见

Default Value:

*   true

#### static propertyViewExpandIcon :String

属性组件展开图标

#### static propertyViewLabelColor :color

属性组件文字颜色

Default Value:

*   #000

#### static propertyViewLabelFont :String

属性组件文字字体

Default Value:

*   12px arial, sans-serif

#### static propertyViewLabelSelectColor :color

属性组件文字选中颜色

Default Value:

*   #FFF

#### static propertyViewRowLineColor :color

属性组件行线颜色

Default Value:

*   #D9D9D9

#### static propertyViewRowLineVisible :Boolean

属性组件行线是否可见

Default Value:

*   true

#### static propertyViewSelectBackground :color

属性组件选中背景色

Default Value:

*   #1ABC9C

#### static reinvalidateCount :Number

组件初次加载时界面宽高值可能会为0，hc会自动尝试等待下次延迟刷新，该参数指定尝试次数，一般无需改动

Default Value:

*   3

#### static scrollBarColor :color

滚动条默认颜色

Default Value:

*   rgba(0,0,0,0.35)

#### static scrollBarInteractiveSize :Number

滚动条起作用区域默认大小

Default Value:

*   16

#### static scrollBarMinLength :Number

滚动条默认最小长度

Default Value:

*   20

#### static scrollBarSize :Number

滚动条默认宽度

Default Value:

*   7

#### static scrollBarTimeout :Number

滚动条默认的隐藏间隔毫秒数

Default Value:

*   1000

#### static scrollZoomIncrement :Number

默认滚轮缩放步进

Default Value:

*   1.05

#### static segmentResolution :Number

默认曲线分段微分数

Default Value:

*   12

#### static shapeResolution :Number

默认模型分段微分数

Default Value:

*   24

#### static shapeSide :Number

默认模型边数

Default Value:

*   24

#### static sortFunc :function

默认排序函数

##### Example

    hc.Default.sortFunc = function(v1, v2) {
    
    }

#### static splitViewDividerBackground :color

分割组件分隔条背景

Default Value:

*   #2C3E50

#### static splitViewDividerSize :Number

分割组件分隔条宽度

Default Value:

*   1

#### static splitViewDragOpacity :Number

分割组件分隔条拖拽过程透明度

Default Value:

*   0.5

#### static splitViewToggleIcon :String

分割组件展开合并图标

#### static tableHeaderBackground :color

表头组件背景

Default Value:

*   #ECF0F1

#### static tableHeaderColumnLineColor :color

表头组件列线颜色

Default Value:

*   #D9D9D9

#### static tableHeaderColumnLineVisible :Boolean

表头组件列线是否可见

Default Value:

*   true

#### static tableHeaderInsertColor :color

表头组件插入状态颜色

Default Value:

*   #1ABC9C

#### static tableHeaderLabelColor :color

表头组件文字颜色

Default Value:

*   #000

#### static tableHeaderLabelFont :String

表头组件文字字体

Default Value:

*   12px arial, sans-serif

#### static tableHeaderMoveBackground :color

表头组件移动状态背景

Default Value:

*   rgba(0,0,0,0.35)

#### static tableHeaderSortAscIcon :String

表头组件升序图标

#### static tableHeaderSortDescIcon :String

表头组件降序图标

#### static tableViewColumnLineColor :color

表格组件列线颜色

Default Value:

*   #D9D9D9

#### static tableViewColumnLineVisible :Boolean

表格组件列线是否可见

Default Value:

*   true

#### static tableViewLabelColor :color

表格组件文字颜色

Default Value:

*   #000

#### static tableViewLabelFont :String

表格组件文字字体

Default Value:

*   12px arial, sans-serif

#### static tableViewLabelSelectColor :color

表格组件文字选中颜色

Default Value:

*   #FFF

#### static tableViewRowLineColor :color

表格组件行线颜色

Default Value:

*   #D9D9D9

#### static tableViewRowLineVisible :Boolean

表格组件行线是否可见

Default Value:

*   true

#### static tableViewSelectBackground :color

表格组件选中背景色

Default Value:

*   #1ABC9C

#### static tabViewInsertColor :color

页签组件插入状态颜色

Default Value:

*   #1ABC9C

#### static tabViewLabelColor :color

页签组件文字颜色

Default Value:

*   #FFF

#### static tabViewLabelFont :String

页签组件文字字体

Default Value:

*   12px arial, sans-serif

#### static tabViewMoveBackground :color

页签组件移动状态背景

Default Value:

*   rgba(0,0,0,0.35)

#### static tabViewSelectBackground :color

页签组件选中背景

Default Value:

*   #1ABC9C

#### static tabViewSelectWidth :Number

页签组件选中宽度

Default Value:

*   3

#### static tabViewTabBackground :color

页签组件背景

Default Value:

*   #2C3E50

#### static tabViewTabGap :Number

页签组件间距

Default Value:

*   1

#### static toolbarBackground :color

工具条组件背景

Default Value:

*   #ECF0F1

#### static toolbarItemGap :Number

工具条组件Item的间距

Default Value:

*   8

#### static toolbarLabelColor :color

工具条组件文字颜色

Default Value:

*   #000

#### static toolbarLabelFont :String

工具条组件文字字体

Default Value:

*   12px arial, sans-serif

#### static toolbarLabelSelectColor :color

工具条组件文字选中颜色

Default Value:

*   #FFF

#### static toolbarSelectBackground :color

工具条组件选中背景色

Default Value:

*   #1ABC9C

#### static toolbarSeparatorColor :color

工具条组件的分隔条颜色

Default Value:

*   #868686

#### static toolTipBackground :color

ToolTip的背景颜色

Default Value:

*   #FFFFE0

#### static toolTipContinual :boolean

组件的ToolTip显示的情况下，如果鼠标移动到新的位置时，ToolTip是否实时持续跟进

Default Value:

*   false

#### static toolTipDelay :Number

组件的ToolTip显示的延迟间隔

Default Value:

*   800

#### static toolTipLabelColor :color

ToolTip的文字颜色

Default Value:

*   #000

#### static toolTipLabelFont :String

ToolTip的文字字体

Default Value:

*   12px arial, sans-serif

#### static toolTipLabelFont :String

ToolTip的文字字体

Default Value:

*   12px arial, sans-serif

#### static toolTipShadowColor :color

ToolTip的阴影颜色

Default Value:

*   rgba(0,0,0,0.35)

#### static treeTableViewCollapseIcon :String

树表格组件关闭状态图标

#### static treeTableViewColumnLineColor :color

树表格组件列线颜色

Default Value:

*   #D9D9D9

#### static treeTableViewColumnLineVisible :Boolean

树表格组件列线是否可见

Default Value:

*   true

#### static treeTableViewExpandIcon :String

树表格组件展开状态图标

#### static treeTableViewLabelColor :color

树表组件文字颜色

Default Value:

*   #000

#### static treeTableViewLabelFont :String

树表组件文字字体

Default Value:

*   12px arial, sans-serif

#### static treeTableViewLabelSelectColor :color

树表组件文字选中颜色

Default Value:

*   #FFF

#### static treeTableViewRowLineColor :color

树表格组件行线颜色

Default Value:

*   #D9D9D9

#### static treeTableViewRowLineVisible :Boolean

树表格组件行线是否可见

Default Value:

*   true

#### static treeTableViewSelectBackground :color

树表组件选中背景色

Default Value:

*   #1ABC9C

#### static treeViewCollapseIcon :String

树组件关闭状态图标

#### static treeViewExpandIcon :String

树组件展开状态图标

#### static treeViewLabelColor :color

树组件文字颜色

Default Value:

*   #000

#### static treeViewLabelFont :String

树组件文字字体

Default Value:

*   12px arial, sans-serif

#### static treeViewLabelSelectColor :color

树组件文字选中颜色

Default Value:

*   #FFF

#### static treeViewRowLineColor :color

树组件行线颜色

Default Value:

*   #D9D9D9

#### static treeViewRowLineVisible :Boolean

树组件行线是否可见

Default Value:

*   false

#### static treeViewSelectBackground :color

树组件选中背景色

Default Value:

*   #1ABC9C

#### static widgetHeaderHeighc :Number

通用组件抬头高度，例如TabView，TableHeader和Toolbar等的头部高度

Default Value:

*   22

#### static widgetIndent :Number

通用组件缩进，例如树组件每一层的缩进

Default Value:

*   20

#### static widgetRowHeighc :Number

通用组件行高，例如表格每行行高

Default Value:

*   20

#### static widgetTitleHeighc :Number

AccordionView和TabView等组件的Title默认高度

Default Value:

*   24

#### static zoomIncrement :Number

默认缩放步进

Default Value:

*   1.3

#### static zoomMax :Number

默认最大缩放倍数

Default Value:

*   20

#### static zoomMin :Number

默认最小缩放倍数

Default Value:

*   0.01

### Methods

#### static brighcer(color, factor) → {color}

返回比color更亮的颜色

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`color`&emsp;&emsp;color&emsp;&emsp;&emsp;&emsp;原始颜色  
`factor`&emsp;&emsp;Number&emsp;&emsp;变化因子，默认为40，允许值0~100 

##### Returns:

color -

新的颜色

##### Example

    var newColor = hc.Default.brighcer('#f00');

#### static callLater(func, scope, args, delay)

获取全局下一个id编号

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`func`&emsp;&emsp; function&emsp;&emsp;&emsp;&emsp;回调函数  
`scope`&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;函数域  
`args`&emsp;&emsp; Array&emsp;&emsp;&emsp;&emsp;&emsp;函数参数列表  
`delay`&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;延迟时间(毫秒)

#### static clone(obj) → {Object}

传入一个对象参数，以浅拷贝的方式返回一个新的复制对象

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`obj`&emsp;&emsp; Object&emsp;&emsp;&emsp;&emsp;要复制的对象  

##### Returns:

Object -

新复制的对象

#### static containedInView(event, view) → {Boolean}

判断交互事件所处位置是否在View组件之上，一般用于Drog And Drop的拖拽操作判断

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`event`&emsp;&emsp; Event&emsp;&emsp;&emsp;&emsp;事件对象  
`event`&emsp;&emsp; Object&emsp;&emsp;&emsp;&emsp;视图对象  

##### Returns:

Boolean

#### static containsPoint(rect, point) → {Boolean}

判断point是否包含在rect的矩形区域里

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`rect`&emsp;&emsp; Event&emsp;&emsp;&emsp;&emsp;矩形  
`point`&emsp;&emsp; Object&emsp;&emsp;&emsp;&emsp;点  

##### Returns:

Boolean -

矩形是否包含点

##### Example

    hc.Default.containsPoint({x: 0, y: 0, width: 100, heighc: 100}, {x: 50, y: 50})//true

#### static containsRect(rect1, rect2) → {Boolean}

判断矩形区域rect1是否包含矩形区域rect2

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description 
`rect1`&emsp;&emsp; Object&emsp;&emsp;&emsp;&emsp;矩形1  
`rect2`&emsp;&emsp; Object&emsp;&emsp;&emsp;&emsp;矩形2  

##### Returns:

Boolean -

矩形1是否包含矩形2

##### Example

    hc.Default.containsRect({x: 0, y: 0, width: 100, heighc: 100}, {x: 0, y: 0, width: 10, heighc: 10})//true

#### static createBoxModel()

构建六面体模型，该模型的六个面显示的颜色和贴图都将一样

#### static createConeModel()

构建圆锥体模型

#### static createCylinderModel()

构建圆柱体模型

#### static createDisabledDiv(iconURL, stopPropagation) → {Element}

创建不可用 Div

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`iconURL`&emsp;&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;背景图 URL  
`stopPropagation`&emsp;Boolean&emsp;&emsp;\<optional> &emsp;&emsp;阻止事件冒泡，默认为 true 表示阻止
`ahead`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

##### Returns:

Element -

DOM 对象

#### static createElement(tagName, borderColor, font, value) → {Element}

创建DOM对象

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`tagName`&emsp;&emsp;&emsp;String&emsp;&emsp; DOM类型(如div、a、span等)  
`borderColor`&emsp;String&emsp;&emsp;&emsp;边框颜色  
`font`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;字体  
`value`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;内容 

##### Returns:

Element -

DOM对象

#### static createExtrusionModel()

根据xz平面多边形，挤压形成3D模型

#### static createMatrix()

将一组JSON描述的缩放、移动和旋转等操作转换成对应的变化矩阵

#### static createParallelogramModel()

构建平行四边形体模型

#### static createRectModel()

构建矩形体模型

#### static createRighcTriangleModel()

构建直角三角形体模型

#### static createRingModel()

根据xy平面的曲线，环绕一周形成3D模型

#### static createRoundRectModel()

构建圆角矩形体模型

#### static createSmoothConeModel()

构建光滑圆锥体模型

#### static createSmoothCylinderModel()

构建光滑圆柱体模型

#### static createSmoothRingModel()

根据xy平面的曲线，环绕一周形成光滑3D模型

#### static createSmoothSphereModel()

构建光滑球体模型

#### static createSmoothcorusModel()

构建光滑圆环体模型

#### static createSphereModel()

构建球体模型

#### static createStarModel()

构建星形体模型

#### static createTorusModel()

构建圆环体模型

#### static createTrapezoidModel()

构建梯形体模型

#### static createTriangleModel()

构建三角形体模型

#### static darker(color, factor) → {color}

返回比color更暗的颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;&emsp;color&emsp;&emsp;&emsp;原始颜色  
`factor`&emsp;&emsp;&emsp; Number&emsp;&emsp;变化因子，默认为40，允许值0~100 

##### Returns:

color -

新的颜色

##### Example

    var newColor = hc.Default.darker('#f00');

#### static def(className, superClass, methods)

定义类

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`className`&emsp;&emsp;String | Object&emsp;&emsp;&emsp;类名，如果为字符串，自动注册到hc的classMap中，一般使用函数(构造函数)即可  
`superClass`&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;要继承的父类  
`methods`&emsp;&emsp;&emsp; Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;方法和变量声明 

##### Example

    function MyData() {
    	MyData.superClass.constructor.call(this);
    }
    hc.Default.def(MyData, hc.Data, {
    	sayHello: function() {
    		console.log('hello');
    	}
    });

#### static drawCenterImage(g, img, x, y, data, view, color)

以x,y为中心绘制img图片

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`g`&emsp;&emsp;&emsp;CanvasRenderingContext2D&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;画笔对象  
`img`&emsp;&emsp;hcMLImageElement | hcMLCanvasElement | Object&emsp;&emsp;&emsp;要绘制的图片(img对象、canvas对象或矢量对象)  
`x`&emsp;&emsp;&emsp; Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;中心点x坐标  
`y`&emsp;&emsp;&emsp; Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;中心点y坐标  
`data`&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;要绑定的Data对象 
`view`&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;要绑定的视图对象 
`color`&emsp;&emsp;color&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;染色 

#### static drawImage(g, image, x, y, width, heighc, data, view, blendColor)

绘制图片

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`g`&emsp;&emsp;&emsp;&emsp;CanvasRenderingContext2D&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;画笔对象  
`img`&emsp;&emsp;&emsp;hcMLImageElement | hcMLCanvasElement | Object&emsp;&emsp;&emsp;要绘制的图片(img对象、canvas对象或矢量对象)  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;中心点x坐标  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;中心点y坐标  
`width`&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制范围宽度 
`heighc`&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制范围高度 
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;要绑定的Data对象 
`view`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;要绑定的视图对象  
`blendColor`&emsp;color&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;染色 

#### static drawRoundRect(g, x, y, width, heighc, topLeftRadius, topRighcRadius, bottomLeftRadius, bottomRighcRadius)

绘制圆角矩形路径

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`g`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;CanvasRenderingContext2D&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;画笔对象  
`img`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;hcMLImageElement | hcMLCanvasElement | Object&emsp;&emsp;&emsp;要绘制的图片(img对象、canvas对象或矢量对象)  
`x`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制开始的x坐标  
`y`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制开始的y坐标  
`width`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的宽度 
`heighc`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的高度 
`topLeftRadius`&emsp;&emsp; Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; &emsp;&emsp;&emsp;&emsp;左上角圆角半径，如果后面三个参数为空，表示4个圆角的半径 
`topRighcRadius`&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;右上角圆角半径  
`bottomLeftRadius`&emsp;Number&emsp;&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 左下角圆角半径 
`bottomRighcRadius`&emsp;Number&emsp;&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;右下角圆角半径 

##### Example

    //示例：画一个黑边红背景，4个圆角半径为10的圆角矩形
    g.fillStyle = 'red';
    g.strokeStyle = 'black';
    g.beginPath();
    hc.Default.drawRoundRect(g, 0, 0, 100, 100, 10);
    g.closePath();
    g.fill();
    g.stroke();

#### static drawStretchImage(g, img, stretch, x, y, w, h, data, view, color)

在矩形位置内绘制图片

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`g`&emsp;&emsp;&emsp;&emsp;CanvasRenderingContext2D&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;画笔对象  
`img`&emsp;&emsp;&emsp;hcMLImageElement | hcMLCanvasElement | Object&emsp;&emsp;要绘制的图片(img对象、canvas对象或矢量对象) 
`stretch`&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;拉伸类型(uniform/centerUniform/fill) 
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;矩形左上角x坐标
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;矩形左上角y坐标
`w`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;矩形宽度
`h`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;矩形高度
`data`&emsp;&emsp; [hc.Data](hc.Data.hcml)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;要绑定的Data对象
`color`&emsp;&emsp; color&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;染色

#### static drawText(g, value, font, color, x, y, width, heighc, align, vAlign)

绘制文字

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`g`&emsp;&emsp;&emsp;&emsp;&emsp;CanvasRenderingContext2D&emsp;画笔对象 
`value`&emsp;&emsp;&emsp;String&emsp;&emsp;文字内容 
`font`&emsp;&emsp;&emsp; CanvasRenderingContext2D&emsp;文字字体 
`color`&emsp;&emsp;&emsp;color&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 文字颜色 
`x`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制开始的x坐标 
`y`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制开始的y坐标 
`width`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的宽度 
`heighc`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;  绘制的高度 
`align`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;文字水平对齐方式，可选值为left|center|righc 
`vAlign`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;文字垂直对齐方式，可选值为top|middle|bottom 

##### Example

    hc.Default.drawText(g, 'Hello, hc', '12px Arial', 'red', 0, 0, 200, 100, 'center', 'middle');

#### static getBatchInfo(name) → {Oject}

获取已注册的批量信息

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp;String&emsp;&emsp;批量名

##### Returns:

Oject -

批量信息

#### static getClass(name) → {function}

传入全路径类字符串名称，返回类定义(构造函数)

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp;String&emsp;&emsp;类名

##### Returns:

function -

类定义(构造函数)

#### static getClassMap() → {Object}

返回所有hc预定义类的json结构信息，key为类全路径名，value为类声明(构造函数)

##### Returns:

Object -

类结构信息

#### static getClientPoint(e) → {Object}

返回client属性坐标

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`e`&emsp;&emsp;&emsp;Event&emsp;&emsp;事件对象

##### Returns:

Object -

client坐标对象

##### Example

    //返回值示例:
    {
       x: 100,
       y: 100
    }

#### static getCompType(type)

获得注册的矢量组件类型

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`type`&emsp;&emsp;&emsp;String&emsp;&emsp;类型名称

#### static getCurrentComp() → {Object}

返回当前矢量组件comp，即hc.Default.compStack\[0\]，一般用于矢量值绑定func动态调用时使用

##### Returns:

Object -

矢量组件comp

#### static getCurrentKeyCodeMap() → {Object}

返回当前键盘按键信息，key为键的keyCode，如果按下则值为true

##### Returns:

Object -

键盘按键信息

#### static getDistance(p1, p2) → {Number}

获取两点之间距离，或向量长度

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`p1`&emsp;&emsp;&emsp;Object | Array&emsp;&emsp; 第一个点的坐标(格式{x: x, y: y})或第一个向量(格式\[x, y, z\])
`p2`&emsp;&emsp;&emsp;Object | Array&emsp;&emsp; 第二个点的坐标(格式{x: x, y: y})或第二个向量(格式\[x, y, z\])


##### Returns:

Number -

距离

##### Example

    //二维两点距离
    var distance = hc.Default.getDistance({x: 0, y: 0}, {x: 10, y: 0});// distance equals 10
    //三维两点距离
    var distance3d = hc.Default.getDistance([0, 0, 0], [0, 10, 0]);// distance3d equals 10

#### static getEdgeType(type) → {function}

获取连线类型函数

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`type`&emsp;&emsp;&emsp;String&emsp;&emsp;连线类型名 


##### Returns:

function -

连线类型函数

#### static getId() → {Number}

获取全局下一个id编号

##### Returns:

Number -

id

#### static getImage(name, color) → {hcMLImageElement|hcMLCanvasElement|Object}

获得已注册的图片

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Attributes&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;图片名  
`color`&emsp;&emsp;&emsp;color&emsp;&emsp;\<optional>&emsp;染色 

##### Returns:

hcMLImageElement | hcMLCanvasElement | Object -

返回已经注册的图片

#### static getImageMap() → {Object}

获得所有注册图片的信息对象

##### Returns:

Object -

已注册图片的映射表

#### static getLogicalPoint(e, view, translateX, translateY, zoomX, zoomY) → {Object}

获取交互点的逻辑坐标，使用视图对象上的此方法更为便捷

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`e`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;事件对象  
`view`&emsp;&emsp;&emsp;&emsp; Object&emsp;&emsp; 视图对象 
`translateX`&emsp;&emsp;Number&emsp;水平偏移  
`translateY`&emsp;&emsp;Number&emsp;垂直偏移 
`zoomX`&emsp;&emsp;&emsp;&emsp;Number&emsp; 水平缩放  
`zoomY`&emsp;&emsp;&emsp;&emsp;Number&emsp; 垂直缩放 

##### Returns:

Object -

逻辑点坐标

#### static getPagePoint(e) → {Object}

返回page属性坐标

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`e`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;事件对象  

##### Returns:

Object -

page坐标对象

##### Example

    //返回值示例:
    {
       x: 100,
       y: 100
    }

#### static getParentComp() → {Object}

返回当前矢量组件上一层comp，即hc.Default.compStack\[1\]，一般用于矢量值绑定func动态调用时使用

##### Returns:

Object -

矢量组件comp

#### static getShape3dModel(name) → {Object}

返回所注册的3D模型

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;模型名  


##### Returns:

Object -

模型

#### static getTextSize(font, text) → {Object}

计算文字的尺寸

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`font`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;文字字体，如:12px Arial  
`text`&emsp;&emsp;&emsp;&emsp; String&emsp;&emsp;文字内容 


##### Returns:

Object -

文字尺寸

##### Example

    //返回值示例:
    {
    	width: 100,
    	heighc: 100
    }

#### static getToolTipDiv() → {Element}

返回ToolTip的相应div对象，可获取进行风格自定义

##### Returns:

Element -

ToolTip相应的div对象

#### static getTouchCount(e) → {Number}

获取当前Touch手指个数

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`e`&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;事件对象  

##### Returns:

Number -

Touch手指个数

#### static getVersion() → {String}

获得hc的版本号

##### Returns:

String -

版本号

#### static getWindowInfo()

获取当前窗口left|top|width|heighc的参数信息

返回的对象格式如下：

##### Example

    {
    	left: 0,
    	top: 0,
    	width: 1280
    	heighc: 768
    }

#### static grow(rect, extend)

改变rect大小，上下左右分别扩展extend的大小

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`rect`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;原始矩形  
`extend`&emsp;&emsp;&emsp;Number&emsp;&emsp;扩展大小 

##### Example

    var rect = {x: 0, y: 0, width: 100, heighc: 100};
    hc.Default.grow(rect, 2)
    //rect结果：
    {
    	x: -2,
    	y: -2,
    	width: 104,
    	heighc: 104
    }

#### static hideToolTip()

隐藏正在显示的ToolTip

#### static intersection(rect1, rect2) → {Object}

获得两个矩形的相交区域

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`rect1`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;矩形1  
`rect2`&emsp;&emsp;&emsp;Object&emsp;&emsp;矩形2 

##### Returns:

Object -

相交的矩形区域，如果没有相交，返回null

##### Example

    var rect = hc.Default.intersection({x: 0, y: 0, width: 100, heighc: 100}, {x: 50, y: 50, width: 200, heighc: 200})
    //rect结果：
    {
    	x: 50,
    	y: 50,
    	width: 50,
    	heighc: 50
    }

#### static intersectsRect(rect1, rect2) → {Boolean}

判断矩形区域rect1和矩形区域rect2是否相交

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`rect1`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;矩形1  
`rect2`&emsp;&emsp;&emsp;Object&emsp;&emsp;矩形2 

##### Returns:

Boolean -

两个矩形是否相交

##### Example

    hc.Default.intersectsRect({x: 0, y: 0, width: 100, heighc: 100}, {x: 0, y: 0, width: 200, heighc: 200})//true

#### static isCtrlDown(e) → {boolean}

判断Ctrl键是否被按下

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`e`&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;事件对象  


##### Returns:

boolean -

Ctrl键是否被按下

#### static isDoubleClick(e) → {boolean}

判断是否为双击事件

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`e`&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;事件对象  

##### Returns:

boolean -

是否是双击

#### static isDragging() → {boolean}

判断目前是否处于拖拽状态

##### Returns:

boolean -

是否处于拖拽状态

#### static isIsolating() → {Boolean}

判断目前系统是否处于隔离状态，处于隔离状态时host吸附和Group组等图元间的联动关系将会被停止

##### Returns:

Boolean -

是否处于隔离状态

#### static isLeftButton(e) → {boolean}

判断是否鼠标左键被按下

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`e`&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;事件对象  

##### Returns:

boolean -

鼠标左键是否被按下

#### static isShiftDown(e) → {boolean}

判断Shift键是否被按下

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`e`&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;事件对象  

##### Returns:

boolean -

Shift键是否被按下

#### static isToolTipShowing() → {Boolean}

判断ToolTip是否正在显示状态

##### Returns:

Boolean -

ToolTip是否显示

#### static preventDefault(e)

阻止事件的默认行为，常用于屏蔽触屏上默认DoubleTap缩放等行为

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`e`&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;事件对象  


#### static removehcML(domElement) → {Boolean}

删除指定的DOM对象

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`domElement`&emsp;&emsp;&emsp;&emsp;Element&emsp;&emsp;DOM对象  

##### Returns:

Boolean -

操作是否成功

#### static setBatchInfo(name, batchInfo)

注册3d图元的批量信息，用于优化大数据量图元绘制性能，详细用法请参考批量手册

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp; String&emsp;&emsp;批量名 
`batchInfo`&emsp;&emsp;Object&emsp;&emsp;批量信息  


#### static setCompType(type, func)

注册矢量组件类型

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`type`&emsp;&emsp;&emsp;&emsp; String&emsp;&emsp;类型名称 
`func`&emsp;&emsp;&emsp;&emsp;function&emsp;&emsp;绘制函数，例：function(g, rect, comp, data, view){}  

#### static setEdgeType(type, func)

注册连线类型

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`type`&emsp;&emsp;&emsp;&emsp; String&emsp;&emsp;连线类型名 
`func`&emsp;&emsp;&emsp;&emsp;function&emsp;&emsp;决定连线走向的函数  


##### Example

    hc.Default.setEdgeType('customEdge', function(edge, gap, graphView) {
             return {
             	points: points;
             	segments: segments;
             }
    })

#### static setImage(name, width, heighc, img)

注册图片

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;图片名  
`width`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;图片宽度
`heighc`&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 图片高度
`img`&emsp;&emsp;&emsp; hcMLImageElement | hcMLCanvasElement | String | Object&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;img、canvas对象或图片url或base64字符串或矢量对象
 
#### static setIsolating(isolating)

设置系统的隔离状态，处于隔离状态时host吸附和Group组等图元间的联动关系将会被停止

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description    
`isolating`&emsp;&emsp;Boolean&emsp;&emsp;新的状态 



#### static setShape3dModel(name, model)

注册3D模型，请参考modeling建模手册

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description    
`name`&emsp;&emsp;String&emsp;&emsp;模型名 
`model`&emsp;&emsp;Object&emsp;&emsp;模型内容 


#### static showToolTip(eventOrPoint, innerhcML)

显示ToolTip

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; Description    
`eventOrPoint`&emsp;&emsp;Event | Object&emsp;&emsp;鼠标事件对象或点坐标 
`innerhcML`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;ToolTip的内容 

#### static startAnim(paramObj)

启动动画

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp; Description    
`paramObj`&emsp;&emsp;Object&emsp;&emsp;动画配置对象，请参考入门手册中的动画属性 


##### Example

    hc.Default.startAnim({
    	frames: 60,
    	interval: 16,
    	finishFunc: function() {
    		console.log('finish');
    	},
    	action: function(t) {
    		console.log(t);
    	}
    });

#### static startDragging(interactor, e, callEnd)

启动拖拽，自定义交互时可能用到

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`interactor`&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;交互器  
`e`&emsp;&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;事件对象
`callEnd`&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;默认为 true，如果明确指定为 false，就不要调用 oldDragger 的 handleWindowTouchEnd 了


#### static toBoundaries(points, segmets, resolution) → {Array}

将不连续曲线转化成Graph3dView#setBoundaries(bs)需要的参数格式

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`points`&emsp;&emsp;&emsp;Array&emsp;&emsp;&emsp; 曲线上的点坐标数组 
`segmets`&emsp;&emsp;&emsp;Array&emsp;&emsp;&emsp;曲线上的线段类型数组  
`resolution`&emsp;&emsp;Number&emsp; 曲线微分数

##### Returns:

Array -

适合Graph3dView#setBoundaries(bs)需要的参数格式

#### static toCanvas(image, width, heighc, stretch, data, view, color) → {hcMLCanvasElement}

将图片转换成Canvas对象

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`image`&emsp;&emsp;&emsp;hcMLImageElement | Object&emsp;&emsp; 要转换的图片(img对象或矢量对象) 
`width`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;新canvas的宽度  
`heighc`&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;新canvas的高度
`stretch`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;拉伸类型(uniform/centerUniform/fill) 
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;要绑定的Data对象  
`view`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;要绑定的视图对象
`color`&emsp;&emsp;&emsp;color&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;染色

##### Returns:

hcMLCanvasElement -

canvas对象

#### static toColorData(color) → {Array}

将颜色转换为rgba格式

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description    
`color`&emsp;&emsp;&emsp;color&emsp;&emsp;旧格式的颜色 

##### Returns:

Array -

rgba格式的颜色

#### static toggleFullscreen(view)

切换 hc 视图组件的全屏显示状态

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description    
`view`&emsp;&emsp;&emsp;Object&emsp;&emsp;hc 视图组件，比如 hc.graph.GraphView, hc.widget.TreeView, hc.widget.BorderPane 等 

#### static transformVec()

将指定矢量或顶点，通过矩阵转换运算出变化后的新矢量或顶点位置

#### static unionPoint(p1, p2) → {Object}

将点组合成矩形

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`p1`&emsp;&emsp;&emsp;Object&emsp;&emsp;第一个点或点数组  
`p2`&emsp;&emsp;&emsp;Object&emsp;&emsp;第二个点 

##### Returns:

Object -

组合的矩形

##### Example

    //组合两点：
    var rect = hc.Default.unionPoint({x: 0, y: 0}, {x: 100, y: 100});
    //rect结果：
    {
    	x: 0,
    	y: 0,
    	width: 100,
    	heighc: 100
    }
    组合多点：
    var rect = hc.Default.unionPoint([{x: 0, y: 0}, {x: 50, y: 50}, {x: 100, y: 100}]);
    //rect结果：
    {
    	x: 0,
    	y: 0,
    	width: 100,
    	heighc: 100
    }

#### static unionRect(rect1, rect2) → {Object}

将两个矩形区域union融合成新的矩形区域

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`rect1`&emsp;&emsp;&emsp;Object&emsp;&emsp;第一个矩形区域  
`rect2`&emsp;&emsp;&emsp;Object&emsp;&emsp;第二个矩形区域 

##### Returns:

Object -

新的矩形区域

##### Example

    var rect = hc.Default.unionRect(
    {x: 0, y: 0, width: 100, heighc: 100},
    {x: 0, y: 0, width: 200, heighc: 200});
    //rect结果：
    {
    	x: 0,
    	y: 0,
    	width: 200,
    	heighc: 200
    }

#### static xhrLoad(urls, callback, option)

ajax 请求对应 url 内容

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`urls`&emsp;&emsp;&emsp;&emsp;String | Array&emsp;&emsp;url 字符串或者多个url，为字符串数据  
`callback`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp; 回调函数，仅有一个参数，为请求结果 
`option`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;选项，可以设置 method,responseType 
