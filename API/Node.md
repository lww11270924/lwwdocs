
#### new Node()

拓扑图元类型

### Extends

*   [hc.Data](hc.Data.html)

### Methods

#### a(name, value) → {Object}

获取或设置attr属性，仅有一个参数时相当于[getAttr](hc.Data.html#getAttr)，有两个参数时相当于[setAttr](hc.Data.html#setAttr)

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp; String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;属性名   
`value`&emsp;&emsp;Object&emsp;&emsp;\<optional>&emsp; &emsp; 属性值 

##### Returns:

Object

Inherited From:

*   [hc.Data#a](hc.Data.html#a)

#### addChild(child, index)

添加孩子节点，index为孩子插入索引，为空则插入作为最后的孩子，内部会自动调用child的setParent

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description  
`child`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;孩子元素   
`index`&emsp;&emsp;Number&emsp; \<optional> &emsp;&emsp;插入索引 

Inherited From:

*   [hc.Data#addChild](hc.Data.html#addChild)

#### addStyleIcon(name, icon)

增加icon，icon参数请参考beginner guide

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;String&emsp;&emsp;icon名   
`icon`&emsp;&emsp;&emsp;Object&emsp;&emsp;icon参数 

Inherited From:

*   [hc.Data#addStyleIcon](hc.Data.html#addStyleIcon)

##### Example

    data.addStyleIcon("arrow1", {
       position: 2,
       width: 50,
       heighc: 25,
       keepOrien: true,
       names: ['arrow']
    });

#### clearChildren()

删除所有孩子节点，内部会自动调用setParent

Inherited From:

*   [hc.Data#clearChildren](hc.Data.html#clearChildren)

#### dm() → {[hc.DataModel](hc.DataModel.html)}

获取[DataModel](hc.DataModel.html)，[getDataModel](hc.Data.html#getDataModel)的缩写

##### Returns:

[hc.DataModel](hc.DataModel.html) - dataModel

Inherited From:

*   [hc.Data#dm](hc.Data.html#dm)

#### eachChild(func, scope)

遍历孩子元素

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;&emsp; function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;遍历函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域

Inherited From:

*   [hc.Data#eachChild](hc.Data.html#eachChild)

##### Example

    data.eachChild(function(child) {
       console.log(child.getId());
    });

#### firePropertyChange(property, oldValue, newValue)

派发属性变化事件

##### Parameters:
>Name&emsp;&emsp; &emsp; Type&emsp;&emsp;&emsp;Description  
`property`&emsp;&emsp;String&emsp;&emsp;属性名  
`oldValue`&emsp;&emsp;Object&emsp;&emsp;旧值  
`newValue`&emsp;&emsp;Object&emsp;&emsp;新值

Inherited From:

*   [hc.Data#firePropertyChange](hc.Data.html#firePropertyChange)

#### fp(property, oldValue, newValue)

派发属性变化事件，同[firePropertyChange](hc.Data.html#firePropertyChange)

##### Parameters:
>Name&emsp;&emsp; &emsp; Type&emsp;&emsp;&emsp;Description  
`property`&emsp;&emsp;String&emsp;&emsp;属性名  
`oldValue`&emsp;&emsp;Object&emsp;&emsp;旧值  
`newValue`&emsp;&emsp;Object&emsp;&emsp;新值

Inherited From:

*   [hc.Data#fp](hc.Data.html#fp)

#### getAgentEdges() → {[hc.List](hc.List.html)}

获取当前图元代理的连线集合

##### Returns:

[hc.List](hc.List.html)

#### getAttaches() → {[hc.List](hc.List.html)}

获取吸附到自身的所有图元

##### Returns:

[hc.List](hc.List.html)

#### getAttr(name) → {Object}

获取attr属性

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp; &emsp; Description  
`name`&emsp; &emsp; String&emsp;&emsp;&emsp;属性名  

##### Returns:

Object

Inherited From:

*   [hc.Data#getAttr](hc.Data.html#getAttr)

#### getAttrObject() → {Object}

获取attr属性对象，该属性默认为空，用于存储用户业务信息

##### Returns:

Object - attr属性对象

Inherited From:

*   [hc.Data#getAttrObject](hc.Data.html#getAttrObject)

#### getChildAt(index) → {[hc.Data](hc.Data.html)}

返回指定索引位置的孩子

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp; &emsp; Description  
`index`&emsp;&emsp;Number&emsp;&emsp;索引  

##### Returns:

[hc.Data](hc.Data.html) - 索引对应的孩子

Inherited From:

*   [hc.Data#getChildAt](hc.Data.html#getChildAt)

#### getChildren() → {[hc.List](hc.List.html)}

获取所有孩子节点

##### Returns:

[hc.List](hc.List.html) - 孩子元素集合

Inherited From:

*   [hc.Data#getChildren](hc.Data.html#getChildren)

#### getClass() → {function}

获取类声明(构造函数)

##### Returns:

function - 类声明(构造函数)

Inherited From:

*   [hc.Data#getClass](hc.Data.html#getClass)

#### getClassName() → {String}

获取类全名，继承Data并希望序列化时应该重写此方法返回子类的类名字符串

##### Returns:

String - 类全名

Inherited From:

*   [hc.Data#getClassName](hc.Data.html#getClassName)

See:

*   [hc.Data#getSuperClass](hc.Data.html#getSuperClass)

#### getCorners(xPadding, yPadding) → {Array}

获取图元四个角的实时坐标(包括旋转后的坐标)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`xPadding`&emsp;&emsp;Number&emsp;&emsp;水平方向padding  
`yPadding`&emsp;&emsp;Number&emsp;&emsp;垂直方向padding  

##### Returns:

Array - 四个角坐标，顺序为左上，右上，右下，左下

##### Example

    //返回值示例：
    [
    {x: 0, y: 0},//左上
    {x: 100, y: 0},//右上
    {x: 100, y: 100},//右下
    {x: 0, y: 100}//左下
    ]

#### getDataModel() → {[hc.DataModel](hc.DataModel.html)}

获取所属的DataModel

##### Returns:

[hc.DataModel](hc.DataModel.html) - DataModel数据容器

Inherited From:

*   [hc.Data#getDataModel](hc.Data.html#getDataModel)

#### getDisplayName() → {String}

获取显示名称，常作为Column和Property的列头和属性名称显示

##### Returns:

String - 显示名称

Inherited From:

*   [hc.Data#getDisplayName](hc.Data.html#getDisplayName)

#### getEdges() → {[hc.List](hc.List.html)}

获取所有跟图元关联的连线(不包括代理的连线)

##### Returns:

[hc.List](hc.List.html)

#### getElevation() → {Number}

获取图元中心在3D坐标系中的y坐标

##### Returns:

Number

#### getHeighc() → {Number}

获取图元在2D拓扑中的高度，或3D拓扑中的z轴长度

##### Returns:

Number

#### getHost() → {[hc.Data](hc.Data.html)}

获取宿主图元，当图元吸附上宿主图元时，宿主移动或旋转时会带动所有吸附者

##### Returns:

[hc.Data](hc.Data.html)

#### getIcon() → {String|Object}

获取小图标名称，常作为TreeView和ListView等组件上的节点小图标

##### Returns:

String | Object - 图标名或矢量

Inherited From:

*   [hc.Data#getIcon](hc.Data.html#getIcon)

#### getId() → {Number}

获取唯一编号

##### Returns:

Number - 唯一编号

Inherited From:

*   [hc.Data#getId](hc.Data.html#getId)

#### getImage() → {[hc.Data](hc.Data.html)}

获取拓扑上展现的图片信息，在GraphView拓扑图中图片一般以position为中心绘制

##### Returns:

[hc.Data](hc.Data.html)

#### getLayer() → {String|Number}

获取数据元素在GraphView组件中的图层位置

##### Returns:

String | Number - 图层名

Inherited From:

*   [hc.Data#getLayer](hc.Data.html#getLayer)

Default Value:

*   0

#### getLoopedEdges() → {[hc.List](hc.List.html)}

获取所有跟节点关联的自环连线

##### Returns:

[hc.List](hc.List.html)

#### getName() → {String}

获取数据元素名

##### Returns:

String - 名称

Inherited From:

*   [hc.Data#getName](hc.Data.html#getName)

#### getParent() → {[hc.Data](hc.Data.html)}

获取父元素

##### Returns:

[hc.Data](hc.Data.html) - 父元素

Inherited From:

*   [hc.Data#getParent](hc.Data.html#getParent)

#### getPosition() → {Object}

获取图元中心点坐标

##### Returns:

Object

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

#### getRect() → {Object}

获取图元的矩形区域(包括旋转)

##### Returns:

Object - 矩形区域

##### Example

    //返回值示例：
    {x: 0, y: 0, width: 100, heighc: 100}

#### getRotation() → {Number}

获取图元的旋转角度，围绕中心点顺时针旋转

##### Returns:

Number - 旋转角度(弧度制)

#### getRotation3d() → {Array}

获取图元在3D拓扑中的三维旋转角度

##### Returns:

Array - 三维旋转角度(弧度制)，格式为\[x, y, z\]，即\[getRotationX(), -getRotation(), getRotationZ()\]

#### getRotationMode() → {String}

返回三维旋转模式  
  
图元在3D拓扑中旋转时，先沿x轴旋转，再沿y轴旋转和先沿y轴旋转，再沿x轴旋转最后的结果是不一样的

##### Returns:

String - 三维旋转模式，xyz|xzy|yxz|yzx|zxy|zyx

See:

*   [setRotationMode](hc.Node.html#setRotationMode)

#### getRotationX() → {Number}

获取图元在3d拓扑中沿x轴的旋转角度(弧度制)

##### Returns:

Number

#### getRotationY() → {Number}

获取图元在3d拓扑中沿y轴的旋转角度(弧度制)

##### Returns:

Number

#### getRotationZ() → {Number}

获取图元在3d拓扑中沿z轴的旋转角度(弧度制)

##### Returns:

Number

#### getScale() → {Object}

获取图元在2D拓扑中的缩放值

##### Returns:

Object

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

#### getScaleTall() → {Number}

获取图元在3D拓扑中y轴方向的缩放值

##### Returns:

Number - y轴方向缩放值

#### getScaleX() → {Number}

获取图元在2D拓扑中x轴方向的缩放值

##### Returns:

Number - x轴方向缩放值

#### getScaleY() → {Number}

设置图元在2D拓扑中y轴方向的缩放值

##### Returns:

Number - y轴方向缩放值

#### getSerializableAttrs() → {Object}

此函数返回一个map，决定序列化时哪些attr属性可被序列化，默认所有attr对象里的属性都会被序列化

##### Returns:

Object - 需要被序列化的attr属性map

Inherited From:

*   [hc.Data#getSerializableAttrs](hc.Data.html#getSerializableAttrs)

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

*   [hc.Data#getSerializableProperties](hc.Data.html#getSerializableProperties)

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

*   [hc.Data#getSerializableStyles](hc.Data.html#getSerializableStyles)

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

##### Example

    //返回值示例：
    {
    	with: 100,
    	heighc: 100
    }

#### getSize3d() → {Array}

获取图元在3D拓扑中的尺寸(长宽高)

##### Returns:

Array - 格式为\[x, y, z\]，即\[getWidth(), getTall(), getHeighc()\]

#### getSourceAgentEdges() → {[hc.List](hc.List.html)}

获取代理的起始于该图元的连线

##### Returns:

[hc.List](hc.List.html)

#### getSourceEdges() → {[hc.List](hc.List.html)}

获取跟图元关联的并起始于该图元的连线(不包括代理的连线)

##### Returns:

[hc.List](hc.List.html)

#### getStyle(name) → {Object}

获取样式属性

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;样式名  

##### Returns:

Object

Inherited From:

*   [hc.Data#getStyle](hc.Data.html#getStyle)

#### getStyleMap() → {Object}

获取图元内部样式映射信息

##### Returns:

Object - 样式映射表

Inherited From:

*   [hc.Data#getStyleMap](hc.Data.html#getStyleMap)

#### getSuperClass() → {function}

获取父类声明(构造函数)，继承类时可以用来调用父类构造或函数

##### Returns:

function - 父类声明(构造函数)

Inherited From:

*   [hc.Data#getSuperClass](hc.Data.html#getSuperClass)

##### Example

    function MyNode() {
         this.getSuperClass().call(this);//调用父类构造函数
    }
    hc.Default.def(MyNode, hc.Data, {
       setName: function(name) {
       	this.getSuperClass().prototype.setName.call(this, name);//调用父类的setName函数
       	this._username = name;
       }
    });

#### getTag() → {String}

获取标识号，可通过[getDataByTag](hc.DataModel.html#getDataByTag)快速查找

##### Returns:

String - 标识号

Inherited From:

*   [hc.Data#getTag](hc.Data.html#getTag)

#### getTall() → {Number}

获取图元在3D拓扑中的y轴长度

##### Returns:

Number

#### getTargetAgentEdges() → {[hc.List](hc.List.html)}

获取图元代理的结束于该图元的连线

##### Returns:

[hc.List](hc.List.html)

#### getTargetEdges() → {[hc.List](hc.List.html)}

获取跟图元关联的并结束于该图元的连线(不包括代理的连线)

##### Returns:

[hc.List](hc.List.html)

#### getToolTip() → {String}

获取文字提示信息

##### Returns:

String - 文字提示

Inherited From:

*   [hc.Data#getToolTip](hc.Data.html#getToolTip)

#### getUIClass() → {function}

获取拓扑组件上的UI类

##### Returns:

function - UI类声明(构造函数)

Inherited From:

*   [hc.Data#getUIClass](hc.Data.html#getUIClass)

#### getWidth() → {Number}

获取图元在2D拓扑中的宽度，或在3D拓扑中x轴的长度

##### Returns:

Number

#### handleHostPropertyChange(event)

当吸附宿主对象属性发生变化时回调该函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`event`&emsp;&emsp;&emsp;Event&emsp;&emsp;事件对象  

#### hasAgentEdges() → {Boolean}

判断当前图元上是否有代理连线

##### Returns:

Boolean

#### hasChildren() → {Boolean}

判断是否有孩子

##### Returns:

Boolean - 是否有孩子

Inherited From:

*   [hc.Data#hasChildren](hc.Data.html#hasChildren)

#### invalidate()

强制触发属性变化事件通知界面更新

Inherited From:

*   [hc.Data#invalidate](hc.Data.html#invalidate)

#### isAdjustChildrenToTop() → {Boolean}

GraphView点击图元会自动sendToTop，该属性决定是否对子图元也进行sendToTop操作

##### Returns:

Boolean - 是否将children自动sendToTop

Inherited From:

*   [hc.Data#isAdjustChildrenToTop](hc.Data.html#isAdjustChildrenToTop)

#### isDescendantOf(data) → {Boolean}

判断自身是否为指定data的子孙

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;要对比的数据元素 

##### Returns:

Boolean - 自身是否为指定data的子孙

Inherited From:

*   [hc.Data#isDescendantOf](hc.Data.html#isDescendantOf)

#### isEmpty() → {Boolean}

判断是否有孩子，同[hasChildren](hc.Data.html#hasChildren)

##### Returns:

Boolean - 是否有孩子

Inherited From:

*   [hc.Data#isEmpty](hc.Data.html#isEmpty)

#### isHostOn(node) → {Boolean}

判断当前图元是否吸附到指定图元对象上

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`node`&emsp;&emsp; [hc.Node](hc.Node.html)&emsp;&emsp;指定的图元 

##### Returns:

Boolean

#### isParentOf(data) → {Boolean}

判断自身是否为指定data的父亲

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;要对比的数据元素 

##### Returns:

Boolean - 自身是否为指定data的父亲

Inherited From:

*   [hc.Data#isParentOf](hc.Data.html#isParentOf)

#### isRelatedTo(data) → {Boolean}

判断自身与指定data是否有父子或子孙关系

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;要对比的数据元素   

##### Returns:

Boolean - 自身与指定data是否有父子或子孙关系

Inherited From:

*   [hc.Data#isRelatedTo](hc.Data.html#isRelatedTo)

#### iv()

强制触发属性变化事件通知界面更新，[invalidate](hc.Data.html#invalidate)的缩写

Inherited From:

*   [hc.Data#iv](hc.Data.html#iv)

#### onChildAdded(child, index)

添加孩子时的回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`child`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;新增加的孩子元素   
`index`&emsp;&emsp;Number&emsp;&emsp;索引 

Inherited From:

*   [hc.Data#onChildAdded](hc.Data.html#onChildAdded)

#### onChildRemoved(child, index)

删除孩子时的回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`child`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;被删除的孩子元素   
`index`&emsp;&emsp;Number&emsp;&emsp;索引 

Inherited From:

*   [hc.Data#onChildRemoved](hc.Data.html#onChildRemoved)

#### onHostChanged(oldHost, newHost)

当吸附的宿主对象发生变化时回调该函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`oldHost`&emsp;&emsp;&emsp;&emsp;[hc.Node](hc.Node.html)&emsp;&emsp; 旧的宿主  
`newHost`&emsp;&emsp;&emsp;&emsp;[hc.Node](hc.Node.html)&emsp;&emsp; 新的宿主


#### onParentChanged(oldParent, parent)

改变父亲元素时的回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`oldParent`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;旧的父元素  
`parent`&emsp;&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;新的父元素

Inherited From:

*   [hc.Data#onParentChanged](hc.Data.html#onParentChanged)

#### onPropertyChanged(event)

属性变化回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`event`&emsp;&emsp;&emsp;Object&emsp;&emsp;属性变化事件  

Inherited From:

*   [hc.Data#onPropertyChanged](hc.Data.html#onPropertyChanged)

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
`name`&emsp;&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp; 样式名  
`oldValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;旧的样式值  
`newValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;新的样式值

Inherited From:

*   [hc.Data#onStyleChanged](hc.Data.html#onStyleChanged)

#### p(x, y) → {Object}

获取或设置设置图元中心点坐标，有参数时相当于[setPosition](hc.Node.html#setPosition)，没有参数时相当于[getPosition](hc.Node.html#getPosition)

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description   
`x`&emsp;&emsp;&emsp;&emsp;&emsp;Number | Obejct&emsp;&emsp;\<optional> &emsp;&emsp;单个参数时，为 {x ,y} 对象，两个参数时为 x 坐标  
`y`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp; &emsp; \<optional> &emsp;&emsp; y 坐标

##### Returns:

Object - 坐标值，格式为:{x: x, y: y}

See:

*   [setPosition](hc.Node.html#setPosition)
*   [getPosition](hc.Node.html#getPosition)

#### p3(x, y, z) → {Array}

获取或设置图元中心点在3D拓扑中的三维坐标，有三个参数时相当于[setPosition3d](hc.Node.html#setPosition3d)，没有参数时相当于[getPosition3d](hc.Node.html#getPosition3d)

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;&emsp;&emsp;x坐标  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;&emsp;&emsp;y坐标  
`z`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;&emsp;&emsp;z坐标

##### Returns:

Array - 三维坐标数组，格式为\[x, y, z\]

See:

*   [setPosition3d](hc.Node.html#setPosition3d)
*   [getPosition3d](hc.Node.html#getPosition3d)

#### r3(rotationX, rotationY, rotationZ) → {Array}

获取或设置图元在3D拓扑中的三维旋转角度，有三个参数时相当于[setRotation3d](hc.Node.html#setRotation3d)，没有参数时相当于[getRotation3d](hc.Node.html#getRotation3d)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`rotationX`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;&emsp;&emsp;沿x轴的旋转角度(弧度制)  
`rotationY`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;&emsp;&emsp;沿y轴的旋转角度(弧度制)  
`rotationZ`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;&emsp;&emsp;沿z轴的旋转角度(弧度制)


##### Returns:

Array - 三维旋转角度(弧度制)，格式为\[x, y, z\]，即\[getRotationX(), -getRotation(), getRotationZ()\]

See:

*   [setRotation3d](hc.Node.html#setRotation3d)
*   [getRotation3d](hc.Node.html#getRotation3d)

#### removeChild(child)

删除指定孩子元素，内部会自动调用孩子元素的setParent

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description   
`child`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;要删除的孩子元素

Inherited From:

*   [hc.Data#removeChild](hc.Data.html#removeChild)

#### removeStyleIcon(name)

删除icon

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description   
`name`&emsp;&emsp; String&emsp;&emsp;&emsp;要删除的icon名

Inherited From:

*   [hc.Data#removeStyleIcon](hc.Data.html#removeStyleIcon)

#### rotateAt(x, y, angle)

以指定的坐标为中心旋转图元

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;指定x坐标   
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;指定y坐标  
`angle`&emsp;&emsp;Number&emsp;&emsp;旋转角度(弧度制)

#### s(name, value) → {Object}

获取或设置样式，仅有一个参数时相当于[getStyle](hc.Data.html#getStyle)，有两个参数时相当于[setStyle](hc.Data.html#setStyle)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp; String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;样式名  
`value`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;样式值

##### Returns:

Object

Inherited From:

*   [hc.Data#s](hc.Data.html#s)

#### s3(width, tall, heighc) → {Array}

获取或设置图元在3D拓扑中的尺寸，有三个参数时相当于[setSize3d](hc.Node.html#setSize3d)，没有参数时相当于[getSize3d](hc.Node.html#getSize3d)

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`width`&emsp;&emsp;&emsp; Number&emsp;&emsp;&emsp;x轴方向的长度  
`tall`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;y轴方向的长度  
`heighc`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;z轴方向的长度

##### Returns:

Array - 格式为\[x, y, z\]，即\[getWidth(), getTall(), getHeighc()\]

See:

*   [setSize3d](hc.Node.html#setSize3d)
*   [getSize3d](hc.Node.html#getSize3d)

#### setAdjustChildrenToTop(adjustToTop)

GraphView点击图元会自动sendToTop，该属性决定是否对子图元也进行sendToTop操作

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`adjustToTop`&emsp;&emsp;Boolean&emsp;&emsp;是否将children自动sendToTop  

Inherited From:

*   [hc.Data#setAdjustChildrenToTop](hc.Data.html#setAdjustChildrenToTop)

#### setAnchor(x, y)

设置图元中心点

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number | Object&emsp;&emsp;x轴方向的中心点比例，当仅有一个参数时，可为 {x: 0, y: 0} 的对象格式   
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;y轴方向的中心点比例  

#### setAnchor3d(x, y, z)

设置图元在3D坐标系中的中心点

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number | Array&emsp;&emsp;x轴方向的中心点比例，当仅有一个参数时，可为 \[x, y, z\] 的数组格式   
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;y轴方向的中心点比例  
`z`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;z轴方向的中心点比例 

#### setAnchorElevation(y)

设置图元在3D坐标系中的y轴方向的中心点比例

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`y`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;y轴方向的中心点比例 

#### setAnchorX(x)

设置图元x轴方向的中心点比例

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;x轴方向的中心点比例 

#### setAnchorY(y)

设置图元y轴方向的中心点比例

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`y`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;y轴方向的中心点比例   

#### setAttr(name, value)

设置attr属性

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp; &emsp; String&emsp;&emsp;属性名   
`value`&emsp;&emsp;&emsp;Object&emsp;&emsp;属性值 

Inherited From:

*   [hc.Data#setAttr](hc.Data.html#setAttr)

#### setAttrObject(attrObject)

设置attr属性对象，该属性默认为空，用于存储用户业务信息

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`attrObject`&emsp;&emsp;Object&emsp;&emsp;&emsp;attr属性对象 

Inherited From:

*   [hc.Data#setAttrObject](hc.Data.html#setAttrObject)

#### setDisplayName(displayName)

设置显示名称，常作为Column和Property的列头和属性名称显示

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`displayName`&emsp;&emsp;String&emsp;&emsp;&emsp;显示名称 

Inherited From:

*   [hc.Data#setDisplayName](hc.Data.html#setDisplayName)

#### setElevation(elevation)

设置图元中心在3D坐标系中的y坐标

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`elevation`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;y轴方向的坐标值 

#### setHeighc(heighc)

设置图元在2D拓扑中的高度，或3D拓扑中的z轴长度

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`heighc`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;2D拓扑中的高度，或3D拓扑中的z轴长度 

#### setHost(data)

设置宿主图元，当图元吸附上宿主图元时，宿主移动或旋转时会带动所有吸附者

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;&emsp;宿主图元 


#### setIcon(icon)

设置小图标名称，常作为TreeView和ListView等组件上的节点小图标

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`icon`&emsp;&emsp;&emsp; String | Object&emsp;&emsp;&emsp;&emsp;图标名或矢量 


Inherited From:

*   [hc.Data#setIcon](hc.Data.html#setIcon)

#### setId(id)

设置唯一编号，如果手工设置，一定要确保在data加入到DataModel之前设置并且唯一不重复

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`id`&emsp;&emsp;&emsp; &emsp; String | Number&emsp; &emsp; &emsp;唯一编号 

Inherited From:

*   [hc.Data#setId](hc.Data.html#setId)

#### setImage(image)

设置拓扑上展现的图片信息，在GraphView拓扑图中图片一般以position为中心绘制

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`image`&emsp;&emsp;&emsp;String | Object&emsp; &emsp; &emsp;注册的图片名或url或矢量对象 

#### setLayer(layer)

设置数据元素在GraphView组件中的图层位置

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`layer`&emsp;&emsp;&emsp;String | Number&emsp;&emsp;&emsp;图层名 

Inherited From:

*   [hc.Data#setLayer](hc.Data.html#setLayer)

#### setName(name)

设置数据元素名称

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp; &emsp;Description  
`name`&emsp;&emsp;&emsp; String&emsp;&emsp;&emsp;&emsp;数据元素名称 

Inherited From:

*   [hc.Data#setName](hc.Data.html#setName)

#### setParent(parent)

设置父元素

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`parent`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;&emsp;&emsp;父元素  

Inherited From:

*   [hc.Data#setParent](hc.Data.html#setParent)

#### setPosition(x, y)

设置图元中心点坐标

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;x坐标  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;y坐标   

#### setPosition3d(x, y, z)

设置图元中心点在3D拓扑中的三维坐标

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;x坐标  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;y坐标   
`z`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;z坐标

#### setRect(x, y, width, heighc)

设置图元矩形区域

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;x坐标  
`y`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;y坐标  
`width`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;宽度   
`heighc`&emsp;&emsp;&emsp; Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 高度 

#### setRotation(rotation)

设置图元的旋转角度，围绕中心点顺时针旋转

##### Parameters:
>Name&emsp;&emsp;&emsp; &emsp; Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`rotation`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;旋转角度(弧度制) 

#### setRotation3d(x, y, z)

设置图元在3D拓扑中的三维旋转角度

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;沿x轴的旋转角度(弧度制)  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;沿y轴的旋转角度(弧度制)  
`z`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;沿z轴的旋转角度(弧度制)

#### setRotationMode(rotationMode)

设置三维旋转模式  
  
图元在3D拓扑中旋转时，先沿x轴旋转，再沿y轴旋转和先沿y轴旋转，再沿x轴旋转最后的结果是不一样的

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp; &emsp;&emsp;Description  
`rotationMode`&emsp;&emsp;String

旋转模式，可选值如下：

  
*   xyz:先进行x轴旋转，再进行y轴旋转，最后进行z轴旋转
  
*   xzy:先进行x轴旋转，再进行z轴旋转，最后进行y轴旋转
  
*   yxz:先进行y轴旋转，再进行x轴旋转，最后进行z轴旋转
  
*   yzx:先进行y轴旋转，再进行z轴旋转，最后进行x轴旋转
  
*   zxy:先进行z轴旋转，再进行x轴旋转，最后进行y轴旋转
  
*   zyx:先进行z轴旋转，再进行y轴旋转，最后进行x轴旋转
  

See:

*   [getRotationMode](hc.Node.html#getRotationMode)

#### setRotationX(rotationX)

设置图元在3D拓扑中沿x轴的旋转角度(弧度制)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`rotationX`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;沿z轴的旋转角度(弧度制)

#### setRotationY(rotationY)

设置图元在3D拓扑中沿y轴的旋转角度(弧度制)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`rotationY`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;沿z轴的旋转角度(弧度制)

#### setRotationZ(rotationZ)

设置图元在3D拓扑中沿z轴的旋转角度(弧度制)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`rotationZ`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;沿z轴的旋转角度(弧度制)

#### setScale(x, y)

设置图元在2D拓扑中的缩放值

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; &emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;&emsp;Number | Object&emsp;&emsp;x轴方向缩放值,当仅有一个参数时，可传入{x, y}格式的对象   
`y`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp; &emsp;&emsp;&emsp;&emsp; y轴方向缩放值  

#### setScale3d(x, y, z)

设置图元在3D拓扑中的缩放值

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp; &emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;&emsp;Number | Array&emsp;&emsp;x轴方向缩放值, 当仅有一个参数时，可以传入\[x, y, z\]格式数组  
`y`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;y轴方向缩放值  
`z`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;z轴方向缩放值 


#### setScaleTall(y)

设置图元在3D拓扑中y轴方向的缩放值

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp; &emsp;Description  
`y`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;y轴方向缩放值 

#### setScaleX(x)

设置图元在2D拓扑中x轴方向的缩放值

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp; &emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;x轴方向缩放值 

#### setScaleY(y)

设置图元在2D拓扑中y轴方向的缩放值

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp; &emsp;Description  
`y`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;y轴方向缩放值 

#### setSize(width, heighc)

设置图元在2D拓扑中的尺寸(宽高)

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`width`&emsp;&emsp;&emsp; Number&emsp;&emsp;&emsp;宽度  
`heighc`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;高度

#### setSize3d(width, tall, heighc)

设置图元在3D拓扑中的尺寸

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`width`&emsp;&emsp;&emsp; Number&emsp;&emsp;&emsp;x轴方向的长度  
`tall`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;y轴方向的长度  
`heighc`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;z轴方向的长度

#### setStyle(name, value)

设置样式

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;样式名  
`value`&emsp;&emsp;&emsp;Object&emsp;&emsp;样式值

Inherited From:

*   [hc.Data#setStyle](hc.Data.html#setStyle)

#### setTag(tag)

设置标识号，可通过[getDataByTag](hc.DataModel.html#getDataByTag)快速查找

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp; &emsp; &emsp;Description  
`tag`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;标识号

Inherited From:

*   [hc.Data#setTag](hc.Data.html#setTag)

#### setTall() → {Number}

设置图元在3D拓扑中的y轴方向的长度

##### Returns:

Number - tall y轴方向的长度

#### setToolTip(toolTip)

设置文字提示信息

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp; &emsp; &emsp;Description  
`toolTip`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;文字提示

Inherited From:

*   [hc.Data#setToolTip](hc.Data.html#setToolTip)

#### setWidth() → {Number}

设置图元在3D拓扑中的x轴方向的长度

##### Returns:

Number - width x轴方向的长度

#### size() → {Number}

获取孩子元素总数

##### Returns:

Number - 孩子元素总数

Inherited From:

*   [hc.Data#size](hc.Data.html#size)

#### t3(tx, ty, tz)

在当前坐标的基础上增加x、y、z三个方向的平移值，[translate3d](hc.Node.html#translate3d)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`tx`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;x轴方向的平移值  
`ty`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;y轴方向的平移值  
`tz`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;z轴方向的平移值  

See:

*   [translate3d](hc.Node.html#translate3d)

#### toChildren(matchFunc, scope) → {[hc.List](hc.List.html)}

以matchFunc为过滤函数构建新的孩子元素集合

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`matchFunc`&emsp;&emsp;function&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;过滤函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域


##### Returns:

[hc.List](hc.List.html) - 孩子元素集合

Inherited From:

*   [hc.Data#toChildren](hc.Data.html#toChildren)

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

*   [hc.Data#toLabel](hc.Data.html#toLabel)

#### toString() → {String}

重写js默认的toString

##### Returns:

String

Inherited From:

*   [hc.Data#toString](hc.Data.html#toString)

#### translate(tx, ty)

在当前坐标的基础上增加x、y两个方向的平移值

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`tx`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;x轴方向的平移值  
`ty`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;y轴方向的平移值   

#### translate3d(tx, ty, tz)

在当前坐标的基础上增加x、y、z三个方向的平移值，[t3](hc.Node.html#t3)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`tx`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;x轴方向的平移值  
`ty`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;y轴方向的平移值  
`tz`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;z轴方向的平移值  

See:

*   [t3](hc.Node.html#t3)

#### translate3dBy(direction, distance)

沿向量平移

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`direction`&emsp;&emsp;&emsp;Array&emsp;&emsp;&emsp;方向向量  
`distance`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移距离

#### translateBack(distance)

沿向量\[0, 0, -1\]平移

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`distance`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移距离

#### translateBottom(distance)

沿向量\[0, -1, 0\]平移

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`distance`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移距离

#### translateFront(distance)

沿向量\[0, 0, 1\]平移

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`distance`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移距离

#### translateLeft(distance)

沿向量\[-1, 0, 0\]平移

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`distance`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移距离

#### translateRighc(distance)

沿向量\[1, 0, 0\]平移

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`distance`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移距离

#### translateTop(distance)

沿向量\[0, 1, 0\]平移

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`distance`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移距离
