
[html](html.htmlml).PolyLine()
------------------------

#### new PolyLine()

支持{x: 10, y: 20, e: 30}格式的三维空间点描述，如果e值为空则取elevation的海拔值， 修改html.Polyline的elevation和tall值时，会自动调节points顶点中的e值； 同理points顶点信息变化也会同步修改html.Polyline的elevation和tall值。

### Extends

*   [html.Shape](html.Shape.htmlml)

### Methods

#### a(name, value) → {Object}

获取或设置attr属性，仅有一个参数时相当于[getAttr](html.Data.htmlml#getAttr)，有两个参数时相当于[setAttr](html.Data.htmlml#setAttr)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp; String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;属性名  
`value`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;属性值


##### Returns:

Object

Inherited From:

*   [html.Data#a](html.Data.htmlml#a)

#### addChild(child, index)

添加孩子节点，index为孩子插入索引，为空则插入作为最后的孩子，内部会自动调用child的setParent

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`child`&emsp;&emsp;&emsp;&emsp;[html.Data](html.Data.htmlml)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;孩子元素  
`index`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;插入索引

Inherited From:

*   [html.Data#addChild](html.Data.htmlml#addChild)

#### addPoint(point, index)

增加点

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`point`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 坐标点  
`index`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;\<optional>&emsp;索引，如果不指定索引则加到最后

Inherited From:

*   [html.Shape#addPoint](html.Shape.htmlml#addPoint)

#### addStyleIcon(name, icon)

增加icon，icon参数请参考beginner guide

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;icon名  
`icon`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;icon参数

Inherited From:

*   [html.Data#addStyleIcon](html.Data.htmlml#addStyleIcon)

##### Example

    data.addStyleIcon("arrow1", {
       position: 2,
       width: 50,
       heightml: 25,
       keepOrien: true,
       names: ['arrow']
    });

#### clearChildren()

删除所有孩子节点，内部会自动调用setParent

Inherited From:

*   [html.Data#clearChildren](html.Data.htmlml#clearChildren)

#### dm() → {[html.DataModel](html.DataModel.htmlml)}

获取[DataModel](html.DataModel.htmlml)，[getDataModel](html.Data.htmlml#getDataModel)的缩写

##### Returns:

[html.DataModel](html.DataModel.htmlml) -

dataModel

Inherited From:

*   [html.Data#dm](html.Data.htmlml#dm)

#### eachtmlhild(func, scope)

遍历孩子元素

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;&emsp; function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;遍历函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域

Inherited From:

*   [html.Data#eachtmlhild](html.Data.htmlml#eachtmlhild)

##### Example

    data.eachtmlhild(function(child) {
       console.log(child.getId());
    });

#### firePropertyChange(property, oldValue, newValue)

派发属性变化事件

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;Description  
`property`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;属性名  
`oldValue`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;旧值  
`newValue`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;新值

Inherited From:

*   [html.Data#firePropertyChange](html.Data.htmlml#firePropertyChange)

#### fp(property, oldValue, newValue)

派发属性变化事件，同[firePropertyChange](html.Data.htmlml#firePropertyChange)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;Description  
`property`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;属性名  
`oldValue`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;旧值  
`newValue`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;新值

Inherited From:

*   [html.Data#fp](html.Data.htmlml#fp)

#### getAgentEdges() → {[html.List](html.List.htmlml)}

获取当前图元代理的连线集合

##### Returns:

[html.List](html.List.htmlml)

Inherited From:

*   [html.Node#getAgentEdges](html.Node.htmlml#getAgentEdges)

#### getAttaches() → {[html.List](html.List.htmlml)}

获取吸附到自身的所有图元

##### Returns:

[html.List](html.List.htmlml)

Inherited From:

*   [html.Node#getAttaches](html.Node.htmlml#getAttaches)

#### getAttr(name) → {Object}

获取attr属性

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp; String&emsp;&emsp;&emsp;属性名  

##### Returns:

Object

Inherited From:

*   [html.Data#getAttr](html.Data.htmlml#getAttr)

#### getAttrObject() → {Object}

获取attr属性对象，该属性默认为空，用于存储用户业务信息

##### Returns:

Object - attr属性对象

Inherited From:

*   [html.Data#getAttrObject](html.Data.htmlml#getAttrObject)

#### getChildAt(index) → {[html.Data](html.Data.htmlml)}

返回指定索引位置的孩子

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`index`&emsp;&emsp;&emsp; Number&emsp;&emsp;索引  

##### Returns:

[html.Data](html.Data.htmlml) - 索引对应的孩子

Inherited From:

*   [html.Data#getChildAt](html.Data.htmlml#getChildAt)

#### getChildren() → {[html.List](html.List.htmlml)}

获取所有孩子节点

##### Returns:

[html.List](html.List.htmlml) - 孩子元素集合

Inherited From:

*   [html.Data#getChildren](html.Data.htmlml#getChildren)

#### getClass() → {function}

获取类声明(构造函数)

##### Returns:

function - 类声明(构造函数)

Inherited From:

*   [html.Data#getClass](html.Data.htmlml#getClass)

#### getClassName() → {String}

获取类全名，继承Data并希望序列化时应该重写此方法返回子类的类名字符串

##### Returns:

String - 类全名

Inherited From:

*   [html.Data#getClassName](html.Data.htmlml#getClassName)

See:

*   [html.Data#getSuperClass](html.Data.htmlml#getSuperClass)

#### getCorners(xPadding, yPadding) → {Array}

获取图元四个角的实时坐标(包括旋转后的坐标)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`xPadding`&emsp;&emsp;Number&emsp;&emsp;水平方向padding  
`yPadding`&emsp;&emsp;Number&emsp;&emsp;垂直方向padding 

##### Returns:

Array - 四个角坐标，顺序为左上，右上，右下，左下

Inherited From:

*   [html.Node#getCorners](html.Node.htmlml#getCorners)

##### Example

    //返回值示例：
    [
    {x: 0, y: 0},//左上
    {x: 100, y: 0},//右上
    {x: 100, y: 100},//右下
    {x: 0, y: 100}//左下
    ]

#### getDataModel() → {[html.DataModel](html.DataModel.htmlml)}

获取所属的DataModel

##### Returns:

[html.DataModel](html.DataModel.htmlml) - DataModel数据容器

Inherited From:

*   [html.Data#getDataModel](html.Data.htmlml#getDataModel)

#### getDisplayName() → {String}

获取显示名称，常作为Column和Property的列头和属性名称显示

##### Returns:

String - 显示名称

Inherited From:

*   [html.Data#getDisplayName](html.Data.htmlml#getDisplayName)

#### getEdges() → {[html.List](html.List.htmlml)}

获取所有跟图元关联的连线(不包括代理的连线)

##### Returns:

[html.List](html.List.htmlml)

Inherited From:

*   [html.Node#getEdges](html.Node.htmlml#getEdges)

#### getElevation() → {Number}

获取图元中心在3D坐标系中的y坐标

##### Returns:

Number

Inherited From:

*   [html.Node#getElevation](html.Node.htmlml#getElevation)

#### getHeightml() → {Number}

获取图元在2D拓扑中的高度，或3D拓扑中的z轴长度

##### Returns:

Number

Inherited From:

*   [html.Node#getHeightml](html.Node.htmlml#getHeightml)

#### getHost() → {[html.Data](html.Data.htmlml)}

获取宿主图元，当图元吸附上宿主图元时，宿主移动或旋转时会带动所有吸附者

##### Returns:

[html.Data](html.Data.htmlml)

Inherited From:

*   [html.Node#getHost](html.Node.htmlml#getHost)

#### getIcon() → {String|Object}

获取小图标名称，常作为TreeView和ListView等组件上的节点小图标

##### Returns:

String | Object - 图标名或矢量

Inherited From:

*   [html.Data#getIcon](html.Data.htmlml#getIcon)

#### getId() → {Number}

获取唯一编号

##### Returns:

Number - 唯一编号

Inherited From:

*   [html.Data#getId](html.Data.htmlml#getId)

#### getImage() → {[html.Data](html.Data.htmlml)}

获取拓扑上展现的图片信息，在GraphView拓扑图中图片一般以position为中心绘制

##### Returns:

[html.Data](html.Data.htmlml)

Inherited From:

*   [html.Node#getImage](html.Node.htmlml#getImage)

#### getLayer() → {String|Number}

获取数据元素在GraphView组件中的图层位置

##### Returns:

String | Number - 图层名

Inherited From:

*   [html.Data#getLayer](html.Data.htmlml#getLayer)

Default Value:

*   0

#### getLength(resolution) → {Number}

计算Shape的长度

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;&emsp;Description  
`resolution`&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;曲线分段微分数，默认为12，数字越大计算结果越精确，同时也越耗费性能

##### Returns:

Number

Inherited From:

*   [html.Shape#getLength](html.Shape.htmlml#getLength)

#### getLoopedEdges() → {[html.List](html.List.htmlml)}

获取所有跟节点关联的自环连线

##### Returns:

[html.List](html.List.htmlml)

Inherited From:

*   [html.Node#getLoopedEdges](html.Node.htmlml#getLoopedEdges)

#### getName() → {String}

获取数据元素名

##### Returns:

String - 名称

Inherited From:

*   [html.Data#getName](html.Data.htmlml#getName)

#### getParent() → {[html.Data](html.Data.htmlml)}

获取父元素

##### Returns:

[html.Data](html.Data.htmlml) - 父元素

Inherited From:

*   [html.Data#getParent](html.Data.htmlml#getParent)

#### getPoints() → {[html.List](html.List.htmlml)}

获取点集合

##### Returns:

[html.List](html.List.htmlml)

Inherited From:

*   [html.Shape#getPoints](html.Shape.htmlml#getPoints)

#### getPosition() → {Object}

获取图元中心点坐标

##### Returns:

Object

Inherited From:

*   [html.Node#getPosition](html.Node.htmlml#getPosition)

##### Example

    //返回值示例：
    {
    	x: 0,
    	y: 0
    }

#### getPosition3d() → {Array}

获取图元中心点在3D拓扑中的三维坐标

##### Returns:

Array - 三维坐标数组，格式为\[x, y, z\]

Inherited From:

*   [html.Node#getPosition3d](html.Node.htmlml#getPosition3d)

#### getRect() → {Object}

获取图元的矩形区域(包括旋转)

##### Returns:

Object - 矩形区域

Inherited From:

*   [html.Node#getRect](html.Node.htmlml#getRect)

##### Example

    //返回值示例：
    {x: 0, y: 0, width: 100, heightml: 100}

#### getRotation() → {Number}

获取图元的旋转角度，围绕中心点顺时针旋转

##### Returns:

Number - 旋转角度(弧度制)

Inherited From:

*   [html.Node#getRotation](html.Node.htmlml#getRotation)

#### getRotation3d() → {Array}

获取图元在3D拓扑中的三维旋转角度

##### Returns:

Array - 三维旋转角度(弧度制)，格式为\[x, y, z\]，即\[getRotationX(), -getRotation(), getRotationZ()\]

Inherited From:

*   [html.Node#getRotation3d](html.Node.htmlml#getRotation3d)

#### getRotationMode() → {String}

返回三维旋转模式  
  
图元在3D拓扑中旋转时，先沿x轴旋转，再沿y轴旋转和先沿y轴旋转，再沿x轴旋转最后的结果是不一样的

##### Returns:

String - 三维旋转模式，xyz|xzy|yxz|yzx|zxy|zyx

Inherited From:

*   [html.Node#getRotationMode](html.Node.htmlml#getRotationMode)

See:

*   [setRotationMode](html.Node.htmlml#setRotationMode)

#### getRotationX() → {Number}

获取图元在3d拓扑中沿x轴的旋转角度(弧度制)

##### Returns:

Number

Inherited From:

*   [html.Node#getRotationX](html.Node.htmlml#getRotationX)

#### getRotationY() → {Number}

获取图元在3d拓扑中沿y轴的旋转角度(弧度制)

##### Returns:

Number

Inherited From:

*   [html.Node#getRotationY](html.Node.htmlml#getRotationY)

#### getRotationZ() → {Number}

获取图元在3d拓扑中沿z轴的旋转角度(弧度制)

##### Returns:

Number

Inherited From:

*   [html.Node#getRotationZ](html.Node.htmlml#getRotationZ)

#### getScale() → {Object}

获取图元在2D拓扑中的缩放值

##### Returns:

Object

Inherited From:

*   [html.Node#getScale](html.Node.htmlml#getScale)

##### Example

    //返回值示例：
    {
    	x: 1,
    	y: 1
    }

#### getScale3d() → {Array}

获取图元在3D拓扑中的缩放值

##### Returns:

Array - 格式为\[x, y, z\]，即\[getScaleX(), getScaleTall(), getScaleY()\]

Inherited From:

*   [html.Node#getScale3d](html.Node.htmlml#getScale3d)

#### getScaleTall() → {Number}

获取图元在3D拓扑中y轴方向的缩放值

##### Returns:

Number - y轴方向缩放值

Inherited From:

*   [html.Node#getScaleTall](html.Node.htmlml#getScaleTall)

#### getScaleX() → {Number}

获取图元在2D拓扑中x轴方向的缩放值

##### Returns:

Number - x轴方向缩放值

Inherited From:

*   [html.Node#getScaleX](html.Node.htmlml#getScaleX)

#### getScaleY() → {Number}

设置图元在2D拓扑中y轴方向的缩放值

##### Returns:

Number - y轴方向缩放值

Inherited From:

*   [html.Node#getScaleY](html.Node.htmlml#getScaleY)

#### getSegments() → {[html.List](html.List.htmlml)}

获取线段类型集合

##### Returns:

[html.List](html.List.htmlml)

Inherited From:

*   [html.Shape#getSegments](html.Shape.htmlml#getSegments)

#### getSerializableAttrs() → {Object}

此函数返回一个map，决定序列化时哪些attr属性可被序列化，默认所有attr对象里的属性都会被序列化

##### Returns:

Object - 需要被序列化的attr属性map

Inherited From:

*   [html.Data#getSerializableAttrs](html.Data.htmlml#getSerializableAttrs)

##### Example

    function(){
        var name, map = {};
        for (name in this._attrObject) {
            map[name] = 1;
        }
        return map;
    }

#### getSerializableProperties() → {Object}

此函数返回一个map，决定序列化时哪些属性可被序列化，如果有自定义的get/set属性并且需要序列化，应该重写此方法

##### Returns:

Object - 需要被序列化的属性map

Inherited From:

*   [html.Data#getSerializableProperties](html.Data.htmlml#getSerializableProperties)

##### Example

    function(){
        return {
            name: 1,
            displayName: 1,
            icon: 1,
            toolTip: 1,
            parent: 1,
            layer: 1,
            tag: 1,
            adjustChildrenToTop: 1
        };
    }

#### getSerializableStyles() → {Object}

此函数返回一个map，决定序列化时哪些样式可被序列化，默认所有样式都会被序列化

##### Returns:

Object - 需要被序列化的样式map

Inherited From:

*   [html.Data#getSerializableStyles](html.Data.htmlml#getSerializableStyles)

##### Example

    function(){
        var name, map = {};
        for (name in this._styleMap) {
            map[name] = 1;
        }
        return map;
    }

#### getSize() → {Object}

获取图元在2D拓扑中的尺寸(宽高)

##### Returns:

Object

Inherited From:

*   [html.Node#getSize](html.Node.htmlml#getSize)

##### Example

    //返回值示例：
    {
    	with: 100,
    	heightml: 100
    }

#### getSize3d() → {Array}

获取图元在3D拓扑中的尺寸(长宽高)

##### Returns:

Array - 格式为\[x, y, z\]，即\[getWidth(), getTall(), getHeightml()\]

Inherited From:

*   [html.Node#getSize3d](html.Node.htmlml#getSize3d)

#### getSourceAgentEdges() → {[html.List](html.List.htmlml)}

获取代理的起始于该图元的连线

##### Returns:

[html.List](html.List.htmlml)

Inherited From:

*   [html.Node#getSourceAgentEdges](html.Node.htmlml#getSourceAgentEdges)

#### getSourceEdges() → {[html.List](html.List.htmlml)}

获取跟图元关联的并起始于该图元的连线(不包括代理的连线)

##### Returns:

[html.List](html.List.htmlml)

Inherited From:

*   [html.Node#getSourceEdges](html.Node.htmlml#getSourceEdges)

#### getStyle(name) → {Object}

获取样式属性

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;样式名  

##### Returns:

Object

Inherited From:

*   [html.Data#getStyle](html.Data.htmlml#getStyle)

#### getStyleMap() → {Object}

获取图元内部样式映射信息

##### Returns:

Object - 样式映射表

Inherited From:

*   [html.Data#getStyleMap](html.Data.htmlml#getStyleMap)

#### getSuperClass() → {function}

获取父类声明(构造函数)，继承类时可以用来调用父类构造或函数

##### Returns:

function - 父类声明(构造函数)

Inherited From:

*   [html.Data#getSuperClass](html.Data.htmlml#getSuperClass)

##### Example

    function MyNode() {
         this.getSuperClass().call(this);//调用父类构造函数
    }
    html.Default.def(MyNode, html.Data, {
       setName: function(name) {
       	this.getSuperClass().prototype.setName.call(this, name);//调用父类的setName函数
       	this._username = name;
       }
    });

#### getTag() → {String}

获取标识号，可通过[getDataByTag](html.DataModel.htmlml#getDataByTag)快速查找

##### Returns:

String - 标识号

Inherited From:

*   [html.Data#getTag](html.Data.htmlml#getTag)

#### getTall() → {Number}

获取图元在3D拓扑中的y轴长度

##### Returns:

Number

Inherited From:

*   [html.Node#getTall](html.Node.htmlml#getTall)

#### getTargetAgentEdges() → {[html.List](html.List.htmlml)}

获取图元代理的结束于该图元的连线

##### Returns:

[html.List](html.List.htmlml)

Inherited From:

*   [html.Node#getTargetAgentEdges](html.Node.htmlml#getTargetAgentEdges)

#### getTargetEdges() → {[html.List](html.List.htmlml)}

获取跟图元关联的并结束于该图元的连线(不包括代理的连线)

##### Returns:

[html.List](html.List.htmlml)

Inherited From:

*   [html.Node#getTargetEdges](html.Node.htmlml#getTargetEdges)

#### getThickness() → {Number}

获取3D拓扑中的线段厚度，小于0时可实现类似地板的填充效果

##### Returns:

Number

Inherited From:

*   [html.Shape#getThickness](html.Shape.htmlml#getThickness)

#### getToolTip() → {String}

获取文字提示信息

##### Returns:

String - 文字提示

Inherited From:

*   [html.Data#getToolTip](html.Data.htmlml#getToolTip)

#### getUIClass() → {function}

获取拓扑组件上的UI类

##### Returns:

function - UI类声明(构造函数)

Inherited From:

*   [html.Data#getUIClass](html.Data.htmlml#getUIClass)

#### getWidth() → {Number}

获取图元在2D拓扑中的宽度，或在3D拓扑中x轴的长度

##### Returns:

Number

Inherited From:

*   [html.Node#getWidth](html.Node.htmlml#getWidth)

#### handleHostPropertyChange(event)

当吸附宿主对象属性发生变化时回调该函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`event`&emsp;&emsp;&emsp;Event&emsp;&emsp;事件对象

Inherited From:

*   [html.Node#handleHostPropertyChange](html.Node.htmlml#handleHostPropertyChange)

#### hasAgentEdges() → {Boolean}

判断当前图元上是否有代理连线

##### Returns:

Boolean

Inherited From:

*   [html.Node#hasAgentEdges](html.Node.htmlml#hasAgentEdges)

#### hasChildren() → {Boolean}

判断是否有孩子

##### Returns:

Boolean - 是否有孩子

Inherited From:

*   [html.Data#hasChildren](html.Data.htmlml#hasChildren)

#### invalidate()

强制触发属性变化事件通知界面更新

Inherited From:

*   [html.Data#invalidate](html.Data.htmlml#invalidate)

#### isAdjustChildrenToTop() → {Boolean}

GraphView点击图元会自动sendToTop，该属性决定是否对子图元也进行sendToTop操作

##### Returns:

Boolean - 是否将children自动sendToTop

Inherited From:

*   [html.Data#isAdjustChildrenToTop](html.Data.htmlml#isAdjustChildrenToTop)

#### isClosePath() → {Boolean}

是否闭合Shape

##### Returns:

Boolean

Inherited From:

*   [html.Shape#isClosePath](html.Shape.htmlml#isClosePath)

#### isDescendantOf(data) → {Boolean}

判断自身是否为指定data的子孙

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[html.Data](html.Data.htmlml)&emsp;要对比的数据元素  

##### Returns:

Boolean - 自身是否为指定data的子孙

Inherited From:

*   [html.Data#isDescendantOf](html.Data.htmlml#isDescendantOf)

#### isEmpty() → {Boolean}

判断是否有孩子，同[hasChildren](html.Data.htmlml#hasChildren)

##### Returns:

Boolean - 是否有孩子

Inherited From:

*   [html.Data#isEmpty](html.Data.htmlml#isEmpty)

#### isHostOn(node) → {Boolean}

判断当前图元是否吸附到指定图元对象上

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`node`&emsp;&emsp;&emsp;&emsp;[html.Node](html.Node.htmlml)&emsp;指定的图元  

##### Returns:

Boolean

Inherited From:

*   [html.Node#isHostOn](html.Node.htmlml#isHostOn)

#### isParentOf(data) → {Boolean}

判断自身是否为指定data的父亲

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[html.Data](html.Data.htmlml)&emsp;要对比的数据元素  

##### Returns:

Boolean - 自身是否为指定data的父亲

Inherited From:

*   [html.Data#isParentOf](html.Data.htmlml#isParentOf)

#### isRelatedTo(data) → {Boolean}

判断自身与指定data是否有父子或子孙关系

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[html.Data](html.Data.htmlml)&emsp;要对比的数据元素  

##### Returns:

Boolean - 自身与指定data是否有父子或子孙关系

Inherited From:

*   [html.Data#isRelatedTo](html.Data.htmlml#isRelatedTo)

#### iv()

强制触发属性变化事件通知界面更新，[invalidate](html.Data.htmlml#invalidate)的缩写

Inherited From:

*   [html.Data#iv](html.Data.htmlml#iv)

#### onChildAdded(child, index)

添加孩子时的回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`child`&emsp;&emsp;&emsp;[html.Data](html.Data.htmlml)&emsp;&emsp;新增加的孩子元素  
`index`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;索引    

Inherited From:

*   [html.Data#onChildAdded](html.Data.htmlml#onChildAdded)

#### onChildRemoved(child, index)

删除孩子时的回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`child`&emsp;&emsp;&emsp;[html.Data](html.Data.htmlml)&emsp;&emsp;被删除的孩子元素  
`index`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;索引    

Inherited From:

*   [html.Data#onChildRemoved](html.Data.htmlml#onChildRemoved)

#### onHostChanged(oldHost, newHost)

当吸附的宿主对象发生变化时回调该函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp; Description  
`oldHost`&emsp;&emsp;&emsp;[html.Node](html.Node.htmlml)&emsp;&emsp;旧的宿主  
`newHost`&emsp;&emsp;&emsp;[html.Node](html.Node.htmlml)&emsp;&emsp;新的宿主   

Inherited From:

*   [html.Node#onHostChanged](html.Node.htmlml#onHostChanged)

#### onParentChanged(oldParent, parent)

改变父亲元素时的回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp; Description  
`oldParent`&emsp;&emsp;[html.Data](html.Data.htmlml)&emsp;&emsp;旧的父元素  
`parent`&emsp;&emsp;&emsp;[html.Data](html.Data.htmlml)&emsp;&emsp;新的父元素   

Inherited From:

*   [html.Data#onParentChanged](html.Data.htmlml#onParentChanged)

#### onPropertyChanged(event)

属性变化回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp; Description  
`event`&emsp;&emsp;Object&emsp;&emsp;属性变化事件  

Inherited From:

*   [html.Data#onPropertyChanged](html.Data.htmlml#onPropertyChanged)

##### Example

    //event格式：
    {
    	property: 'name',//发生变化的属性
    	oldValue: 'oldValue',//旧值
    	newValue: 'newValue',''新值
    	data: data//发生变化的data
    }

#### onStyleChanged(name, oldValue, newValue)

样式属性变化时会回调该函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp; Description  
`name`&emsp;&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;样式名
`oldValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;旧的样式值
`newValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;新的样式值

Inherited From:

*   [html.Data#onStyleChanged](html.Data.htmlml#onStyleChanged)

#### p(x, y) → {Object}

获取或设置设置图元中心点坐标，有参数时相当于[setPosition](html.Node.htmlml#setPosition)，没有参数时相当于[getPosition](html.Node.htmlml#getPosition)

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number | Obejct&emsp;&emsp;\<optional>&emsp;&emsp;单个参数时，为 {x ,y} 对象，两个参数时为 x 坐标  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;y 坐标 

##### Returns:

Object - 坐标值，格式为:{x: x, y: y}

Inherited From:

*   [html.Node#p](html.Node.htmlml#p)

See:

*   [setPosition](html.Node.htmlml#setPosition)
*   [getPosition](html.Node.htmlml#getPosition)

#### p3(x, y, z) → {Array}

获取或设置图元中心点在3D拓扑中的三维坐标，有三个参数时相当于[setPosition3d](html.Node.htmlml#setPosition3d)，没有参数时相当于[getPosition3d](html.Node.htmlml#getPosition3d)

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;&emsp;&emsp;x坐标  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;&emsp;&emsp;y坐标  
`z`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;&emsp;&emsp;z坐标

##### Returns:

Array - 三维坐标数组，格式为\[x, y, z\]

Inherited From:

*   [html.Node#p3](html.Node.htmlml#p3)

See:

*   [setPosition3d](html.Node.htmlml#setPosition3d)
*   [getPosition3d](html.Node.htmlml#getPosition3d)

#### r3(rotationX, rotationY, rotationZ) → {Array}

获取或设置图元在3D拓扑中的三维旋转角度，有三个参数时相当于[setRotation3d](html.Node.htmlml#setRotation3d)，没有参数时相当于[getRotation3d](html.Node.htmlml#getRotation3d)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`rotationX`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;&emsp;&emsp;沿x轴的旋转角度(弧度制)  
`rotationY`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;&emsp;&emsp;沿y轴的旋转角度(弧度制)  
`rotationZ`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;&emsp;&emsp;沿z轴的旋转角度(弧度制)


##### Returns:

Array - 三维旋转角度(弧度制)，格式为\[x, y, z\]，即\[getRotationX(), -getRotation(), getRotationZ()\]

Inherited From:

*   [html.Node#r3](html.Node.htmlml#r3)

See:

*   [setRotation3d](html.Node.htmlml#setRotation3d)
*   [getRotation3d](html.Node.htmlml#getRotation3d)

#### removeChild(child)

删除指定孩子元素，内部会自动调用孩子元素的setParent

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`child`&emsp;&emsp;[html.Data](html.Data.htmlml)&emsp;&emsp;要删除的孩子元素

Inherited From:

*   [html.Data#removeChild](html.Data.htmlml#removeChild)

#### removePointAt(index)

根据索引删除点

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`index`&emsp;&emsp;Number&emsp;&emsp;索引

Inherited From:

*   [html.Shape#removePointAt](html.Shape.htmlml#removePointAt)

#### removeStyleIcon(name)

删除icon

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;String&emsp;&emsp;要删除的icon名

Inherited From:

*   [html.Data#removeStyleIcon](html.Data.htmlml#removeStyleIcon)

#### rotateAt(x, y, angle)

以指定的坐标为中心旋转图元

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;指定x坐标  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;指定y坐标  
`angle`&emsp;&emsp;Boolean&emsp;&emsp;&emsp;旋转角度(弧度制)

Inherited From:

*   [html.Node#rotateAt](html.Node.htmlml#rotateAt)

#### s(name, value) → {Object}

获取或设置样式，仅有一个参数时相当于[getStyle](html.Data.htmlml#getStyle)，有两个参数时相当于[setStyle](html.Data.htmlml#setStyle)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp; String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;样式名  
`value`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;样式值

##### Returns:

Object

Inherited From:

*   [html.Data#s](html.Data.htmlml#s)

#### s3(width, tall, heightml) → {Array}

获取或设置图元在3D拓扑中的尺寸，有三个参数时相当于[setSize3d](html.Node.htmlml#setSize3d)，没有参数时相当于[getSize3d](html.Node.htmlml#getSize3d)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`width`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp; x轴方向的长度  
`tall`&emsp;&emsp;&emsp;&emsp; Number&emsp;&emsp;&emsp;y轴方向的长度  
`heightml`&emsp;&emsp;Number&emsp;&emsp;&emsp;z轴方向的长度

##### Returns:

Array - 格式为\[x, y, z\]，即\[getWidth(), getTall(), getHeightml()\]

Inherited From:

*   [html.Node#s3](html.Node.htmlml#s3)

See:

*   [setSize3d](html.Node.htmlml#setSize3d)
*   [getSize3d](html.Node.htmlml#getSize3d)

#### setAdjustChildrenToTop(adjustToTop)

GraphView点击图元会自动sendToTop，该属性决定是否对子图元也进行sendToTop操作

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`adjustToTop`&emsp;&emsp;Boolean&emsp;&emsp;是否将children自动sendToTop  

Inherited From:

*   [html.Data#setAdjustChildrenToTop](html.Data.htmlml#setAdjustChildrenToTop)

#### setAnchor(x, y)

设置图元中心点

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number | Object&emsp;&emsp;x轴方向的中心点比例，当仅有一个参数时，可为 {x: 0, y: 0} 的对象格式   
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;y轴方向的中心点比例


Inherited From:

*   [html.Node#setAnchor](html.Node.htmlml#setAnchor)

#### setAnchor3d(x, y, z)

设置图元在3D坐标系中的中心点

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number | Array&emsp;&emsp;x轴方向的中心点比例，当仅有一个参数时，可为 \[x, y, z\] 的数组格式   
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;y轴方向的中心点比例  
`z`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;z轴方向的中心点比例

Inherited From:

*   [html.Node#setAnchor3d](html.Node.htmlml#setAnchor3d)

#### setAnchorElevation(y)

设置图元在3D坐标系中的y轴方向的中心点比例

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description    
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;y轴方向的中心点比例  

Inherited From:

*   [html.Node#setAnchorElevation](html.Node.htmlml#setAnchorElevation)

#### setAnchorX(x)

设置图元x轴方向的中心点比例

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number | Array&emsp;&emsp;x轴方向的中心点比例  

Inherited From:

*   [html.Node#setAnchorX](html.Node.htmlml#setAnchorX)

#### setAnchorY(y)

设置图元y轴方向的中心点比例

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;y轴方向的中心点比例  

Inherited From:

*   [html.Node#setAnchorY](html.Node.htmlml#setAnchorY)

#### setAttr(name, value)

设置attr属性

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;属性名  
`value`&emsp;&emsp;&emsp;Object&emsp;&emsp;属性值

Inherited From:

*   [html.Data#setAttr](html.Data.htmlml#setAttr)

#### setAttrObject(attrObject)

设置attr属性对象，该属性默认为空，用于存储用户业务信息

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`attrObject`&emsp;&emsp;&emsp;Object&emsp;&emsp;attr属性对象 

Inherited From:

*   [html.Data#setAttrObject](html.Data.htmlml#setAttrObject)

#### setClosePath(v)

设置是否闭合Shape

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Boolean

Inherited From:

*   [html.Shape#setClosePath](html.Shape.htmlml#setClosePath)

#### setDisplayName(displayName)

设置显示名称，常作为Column和Property的列头和属性名称显示

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`displayName`&emsp;&emsp;String&emsp;&emsp;显示名称

Inherited From:

*   [html.Data#setDisplayName](html.Data.htmlml#setDisplayName)

#### setElevation(elevation)

设置图元中心在3D坐标系中的y坐标

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`elevation`&emsp;&emsp;Number&emsp;&emsp;y轴方向的坐标值

Inherited From:

*   [html.Node#setElevation](html.Node.htmlml#setElevation)

#### setHeightml(heightml)

设置图元在2D拓扑中的高度，或3D拓扑中的z轴长度

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`heightml`&emsp;&emsp;Number&emsp;&emsp;2D拓扑中的高度，或3D拓扑中的z轴长度

Inherited From:

*   [html.Node#setHeightml](html.Node.htmlml#setHeightml)

#### setHost(data)

设置宿主图元，当图元吸附上宿主图元时，宿主移动或旋转时会带动所有吸附者

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[html.Data](html.Data.htmlml)&emsp;&emsp;宿主图元

Inherited From:

*   [html.Node#setHost](html.Node.htmlml#setHost)

#### setIcon(icon)

设置小图标名称，常作为TreeView和ListView等组件上的节点小图标

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp; Description  
`icon`&emsp;&emsp; String | Object&emsp;&emsp;图标名或矢量

Inherited From:

*   [html.Data#setIcon](html.Data.htmlml#setIcon)

#### setId(id)

设置唯一编号，如果手工设置，一定要确保在data加入到DataModel之前设置并且唯一不重复

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`id`&emsp;&emsp;&emsp;&emsp;String | Number&emsp;&emsp;唯一编号

Inherited From:

*   [html.Data#setId](html.Data.htmlml#setId)

#### setImage(image)

设置拓扑上展现的图片信息，在GraphView拓扑图中图片一般以position为中心绘制

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`image`&emsp;&emsp;&emsp;&emsp;String | Object&emsp;&emsp;注册的图片名或url或矢量对象

Inherited From:

*   [html.Node#setImage](html.Node.htmlml#setImage)

#### setLayer(layer)

设置数据元素在GraphView组件中的图层位置

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`layer`&emsp;&emsp;&emsp;&emsp;String | Number&emsp;&emsp;图层名

Inherited From:

*   [html.Data#setLayer](html.Data.htmlml#setLayer)

#### setName(name)

设置数据元素名称

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;数据元素名称

Inherited From:

*   [html.Data#setName](html.Data.htmlml#setName)

#### setParent(parent)

设置父元素

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`parent`&emsp;&emsp;&emsp;&emsp;[html.Data](html.Data.htmlml)&emsp;&emsp;父元素

Inherited From:

*   [html.Data#setParent](html.Data.htmlml#setParent)

#### setPoint(index, point)

修改索引指向的点坐标

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`index`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp; 索引  
`point`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;新坐标点

Inherited From:

*   [html.Shape#setPoint](html.Shape.htmlml#setPoint)

#### setPoints(points)

设置Shape的点

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp; Type&emsp;&emsp;&emsp;&emsp;Description  
`points`&emsp;&emsp;&emsp;&emsp;[html.List](html.List.htmlml)

Inherited From:

*   [html.Shape#setPoints](html.Shape.htmlml#setPoints)

#### setPosition(x, y)

设置图元中心点坐标

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;x坐标  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;y坐标 

Inherited From:

*   [html.Node#setPosition](html.Node.htmlml#setPosition)

#### setPosition3d(x, y, z)

设置图元中心点在3D拓扑中的三维坐标

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;x坐标  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;y坐标  
`z`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;z坐标 

Inherited From:

*   [html.Node#setPosition3d](html.Node.htmlml#setPosition3d)

#### setRect(x, y, width, heightml)

设置图元矩形区域

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;x坐标  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;y坐标  
`width`&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;宽度  
`heightml`&emsp;Number&emsp;&emsp;&emsp;&emsp;高度

Inherited From:

*   [html.Node#setRect](html.Node.htmlml#setRect)

#### setRotation(rotation)

设置图元的旋转角度，围绕中心点顺时针旋转

##### Parameters:
>Name&emsp;&emsp; Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`rotation`&emsp;Number&emsp;&emsp;&emsp;旋转角度(弧度制)

Inherited From:

*   [html.Node#setRotation](html.Node.htmlml#setRotation)

#### setRotation3d(x, y, z)

设置图元在3D拓扑中的三维旋转角度

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`rotationX`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;沿x轴的旋转角度(弧度制)  
`rotationY`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;沿y轴的旋转角度(弧度制)  
`rotationZ`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;沿z轴的旋转角度(弧度制)

Inherited From:

*   [html.Node#setRotation3d](html.Node.htmlml#setRotation3d)

#### setRotationMode(rotationMode)

设置三维旋转模式  
  
图元在3D拓扑中旋转时，先沿x轴旋转，再沿y轴旋转和先沿y轴旋转，再沿x轴旋转最后的结果是不一样的

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`rotationMode`&emsp;&emsp; String

旋转模式，可选值如下：

  
*   xyz:先进行x轴旋转，再进行y轴旋转，最后进行z轴旋转
  
*   xzy:先进行x轴旋转，再进行z轴旋转，最后进行y轴旋转
  
*   yxz:先进行y轴旋转，再进行x轴旋转，最后进行z轴旋转
  
*   yzx:先进行y轴旋转，再进行z轴旋转，最后进行x轴旋转
  
*   zxy:先进行z轴旋转，再进行x轴旋转，最后进行y轴旋转
  
*   zyx:先进行z轴旋转，再进行y轴旋转，最后进行x轴旋转
  

Inherited From:

*   [html.Node#setRotationMode](html.Node.htmlml#setRotationMode)

See:

*   [getRotationMode](html.Node.htmlml#getRotationMode)

#### setRotationX(rotationX)

设置图元在3D拓扑中沿x轴的旋转角度(弧度制)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`rotationX`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;沿x轴的旋转角度(弧度制)  

Inherited From:

*   [html.Node#setRotationX](html.Node.htmlml#setRotationX)

#### setRotationY(rotationY)

设置图元在3D拓扑中沿y轴的旋转角度(弧度制)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`rotationY`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;沿y轴的旋转角度(弧度制)  

Inherited From:

*   [html.Node#setRotationY](html.Node.htmlml#setRotationY)

#### setRotationZ(rotationZ)

设置图元在3D拓扑中沿z轴的旋转角度(弧度制)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description   
`rotationZ`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;沿z轴的旋转角度(弧度制)

Inherited From:

*   [html.Node#setRotationZ](html.Node.htmlml#setRotationZ)

#### setScale(x, y)

设置图元在2D拓扑中的缩放值

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number | Object&emsp;&emsp;x轴方向缩放值,当仅有一个参数时，可传入{x, y}格式的对象   
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;y轴方向的中心点比例

Inherited From:

*   [html.Node#setScale](html.Node.htmlml#setScale)

#### setScale3d(x, y, z)

设置图元在3D拓扑中的缩放值

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number | Array&emsp;&emsp;x轴方向缩放值, 当仅有一个参数时，可以传入\[x, y, z\]格式数组   
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;y轴方向缩放值  
`z`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;z轴方向缩放值

Inherited From:

*   [html.Node#setScale3d](html.Node.htmlml#setScale3d)

#### setScaleTall(y)

设置图元在3D拓扑中y轴方向的缩放值

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;y轴方向缩放值  

Inherited From:

*   [html.Node#setScaleTall](html.Node.htmlml#setScaleTall)

#### setScaleX(x)

设置图元在2D拓扑中x轴方向的缩放值

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number | Array&emsp;&emsp;x轴方向缩放值  

Inherited From:

*   [html.Node#setScaleX](html.Node.htmlml#setScaleX)

#### setScaleY(y)

设置图元在2D拓扑中y轴方向的缩放值

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;y轴方向缩放值  

Inherited From:

*   [html.Node#setScaleY](html.Node.htmlml#setScaleY)

#### setSegments(segments)

设置Shape的线段类型

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`segments`&emsp;&emsp;&emsp;[html.List](html.List.htmlml)

Inherited From:

*   [html.Shape#setSegments](html.Shape.htmlml#setSegments)

#### setSize(width, heightml)

设置图元在2D拓扑中的尺寸(宽高)

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`width`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;宽度  
`heightml`&emsp;&emsp;Number&emsp;&emsp;&emsp;高度

Inherited From:

*   [html.Node#setSize](html.Node.htmlml#setSize)

#### setSize3d(width, tall, heightml)

设置图元在3D拓扑中的尺寸

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`width`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;x轴方向的长度  
`tall`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;y轴方向的长度  
`heightml`&emsp;&emsp;Number&emsp;&emsp;&emsp;z轴方向的长度

Inherited From:

*   [html.Node#setSize3d](html.Node.htmlml#setSize3d)

#### setStyle(name, value)

设置样式

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp; String&emsp;&emsp;&emsp;样式名  
`value`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;样式值  

Inherited From:

*   [html.Data#setStyle](html.Data.htmlml#setStyle)

#### setTag(tag)

设置标识号，可通过[getDataByTag](html.DataModel.htmlml#getDataByTag)快速查找

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`tag`&emsp;&emsp;&emsp; String&emsp;&emsp;&emsp;标识号  

Inherited From:

*   [html.Data#setTag](html.Data.htmlml#setTag)

#### setTall() → {Number}

设置图元在3D拓扑中的y轴方向的长度

##### Returns:

Number - tall y轴方向的长度

Inherited From:

*   [html.Node#setTall](html.Node.htmlml#setTall)

#### setThickness(thickness)

设置3D拓扑中的线段厚度，小于0时可实现类似地板的填充效果

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`thickness`&emsp;&emsp;Number

Inherited From:

*   [html.Shape#setThickness](html.Shape.htmlml#setThickness)

#### setToolTip(toolTip)

设置文字提示信息

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`toolTip`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;文字提示

Inherited From:

*   [html.Data#setToolTip](html.Data.htmlml#setToolTip)

#### setWidth() → {Number}

设置图元在3D拓扑中的x轴方向的长度

##### Returns:

Number - width x轴方向的长度

Inherited From:

*   [html.Node#setWidth](html.Node.htmlml#setWidth)

#### size() → {Number}

获取孩子元素总数

##### Returns:

Number - 孩子元素总数

Inherited From:

*   [html.Data#size](html.Data.htmlml#size)

#### t3(tx, ty, tz)

在当前坐标的基础上增加x、y、z三个方向的平移值，[translate3d](html.Node.htmlml#translate3d)的缩写

##### Parameters:
>Name&emsp;&emsp; Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`tx`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;x轴方向的平移值  
`ty`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;y轴方向的平移值  
`tz`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;z轴方向的平移值   

Inherited From:

*   [html.Node#t3](html.Node.htmlml#t3)

See:

*   [translate3d](html.Node.htmlml#translate3d)

#### toChildren(matchFunc, scope) → {[html.List](html.List.htmlml)}

以matchFunc为过滤函数构建新的孩子元素集合

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`matchFunc`&emsp;&emsp;function&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;过滤函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域

##### Returns:

[html.List](html.List.htmlml) - 孩子元素集合

Inherited From:

*   [html.Data#toChildren](html.Data.htmlml#toChildren)

##### Example

    var list = data.toChildren(function(child) {
       if (child.a('visible')) {
       	return true;
       }
    });

#### toLabel() → {String}

返回值作为TreeView和GraphView等组件上的图元文字标签，默认返回displayName||name信息

##### Returns:

String - 文字标签

Inherited From:

*   [html.Data#toLabel](html.Data.htmlml#toLabel)

#### toPoints() → {[html.List](html.List.htmlml)}

构建一个新的Shape点集合并返回

##### Returns:

[html.List](html.List.htmlml)

Inherited From:

*   [html.Shape#toPoints](html.Shape.htmlml#toPoints)

#### toSegments() → {[html.List](html.List.htmlml)}

构建一个新的线段类型集合并返回

##### Returns:

[html.List](html.List.htmlml)

Inherited From:

*   [html.Shape#toSegments](html.Shape.htmlml#toSegments)

#### toString() → {String}

重写js默认的toString

##### Returns:

String

Inherited From:

*   [html.Data#toString](html.Data.htmlml#toString)

#### translate(tx, ty)

在当前坐标的基础上增加x、y两个方向的平移值

##### Parameters:
>Name&emsp;&emsp; Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`tx`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;x轴方向的平移值  
`ty`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;y轴方向的平移值  

Inherited From:

*   [html.Node#translate](html.Node.htmlml#translate)

#### translate3d(tx, ty, tz)

在当前坐标的基础上增加x、y、z三个方向的平移值，[t3](html.Node.htmlml#t3)的缩写

##### Parameters:
>Name&emsp;&emsp; Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`tx`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;x轴方向的平移值  
`ty`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;y轴方向的平移值  
`tz`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;z轴方向的平移值 

Inherited From:

*   [html.Node#translate3d](html.Node.htmlml#translate3d)

See:

*   [t3](html.Node.htmlml#t3)

#### translate3dBy(direction, distance)

沿向量平移

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`direction`&emsp;&emsp;&emsp;&emsp;Array&emsp;&emsp;&emsp;方向向量  
`distance`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移距离 

Inherited From:

*   [html.Node#translate3dBy](html.Node.htmlml#translate3dBy)

#### translateBack(distance)

沿向量\[0, 0, -1\]平移

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description   
`distance`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移距离 


Inherited From:

*   [html.Node#translateBack](html.Node.htmlml#translateBack)

#### translateBottom(distance)

沿向量\[0, -1, 0\]平移

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description   
`distance`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移距离 


Inherited From:

*   [html.Node#translateBottom](html.Node.htmlml#translateBottom)

#### translateFront(distance)

沿向量\[0, 0, 1\]平移

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description   
`distance`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移距离 


Inherited From:

*   [html.Node#translateFront](html.Node.htmlml#translateFront)

#### translateLeft(distance)

沿向量\[-1, 0, 0\]平移

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description   
`distance`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移距离 

Inherited From:

*   [html.Node#translateLeft](html.Node.htmlml#translateLeft)

#### translateRightml(distance)

沿向量\[1, 0, 0\]平移

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description   
`distance`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移距离 


Inherited From:

*   [html.Node#translateRightml](html.Node.htmlml#translateRightml)

#### translateTop(distance)

沿向量\[0, 1, 0\]平移

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description   
`distance`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移距离 

Inherited From:

*   [html.Node#translateTop](html.Node.htmlml#translateTop)

