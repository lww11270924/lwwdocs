<h3>hc.Tab()</h3>   

---
#### new Tab()

页签，用于加入TabView页签组件

### Extends

*   [hc.Data](hc.Data.html)

### Methods

#### a(name, value) → {Object}

获取或设置attr属性，仅有一个参数时相当于[getAttr](hc.Data.html#getAttr)，有两个参数时相当于[setAttr](hc.Data.html#setAttr)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`child`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;属性名  
`value`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;属性值

##### Returns:

Object

Inherited From:

*   [hc.Data#a](hc.Data.html#a)

#### addChild(child, index)

添加孩子节点，index为孩子插入索引，为空则插入作为最后的孩子，内部会自动调用child的setParent

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`child`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;孩子元素  
`index`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;插入索引

Inherited From:

*   [hc.Data#addChild](hc.Data.html#addChild)

#### addStyleIcon(name, icon)

增加icon，icon参数请参考beginner guide

##### Parameters:
>Name&emsp;&emsp;&emsp; Type&emsp;&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;icon名  
`icon`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;icon参数  

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
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`property`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;属性名  
`oldValue`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;旧值  
`newValue`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;新值  

Inherited From:

*   [hc.Data#firePropertyChange](hc.Data.html#firePropertyChange)

#### fp(property, oldValue, newValue)

派发属性变化事件，同[firePropertyChange](hc.Data.html#firePropertyChange)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`property`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;属性名  
`oldValue`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;旧值  
`newValue`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;新值  

Inherited From:

*   [hc.Data#fp](hc.Data.html#fp)

#### getAttr(name) → {Object}

获取attr属性

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;属性名  

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
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`index`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;索引  

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

#### getLayer() → {String|Number}

获取数据元素在GraphView组件中的图层位置

##### Returns:

String | Number - 图层名

Inherited From:

*   [hc.Data#getLayer](hc.Data.html#getLayer)

Default Value:

*   0

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

#### getStyle(name) → {Object}

获取样式属性

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;样式名  

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

#### getView() → {htmlElement}

获取页签被选中时呈现的视图组件

##### Returns:

htmlElement

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

#### isClosable() → {Boolean}

页签是否可被关闭

##### Returns:

Boolean

#### isDescendantOf(data) → {Boolean}

判断自身是否为指定data的子孙

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;要对比的数据元素  

##### Returns:

Boolean - 自身是否为指定data的子孙

Inherited From:

*   [hc.Data#isDescendantOf](hc.Data.html#isDescendantOf)

#### isDisabled() → {Boolean}

页签是否被禁用

##### Returns:

Boolean

#### isEmpty() → {Boolean}

判断是否有孩子，同[hasChildren](hc.Data.html#hasChildren)

##### Returns:

Boolean - 是否有孩子

Inherited From:

*   [hc.Data#isEmpty](hc.Data.html#isEmpty)

#### isParentOf(data) → {Boolean}

判断自身是否为指定data的父亲

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;要对比的数据元素  

##### Returns:

Boolean - 自身是否为指定data的父亲

Inherited From:

*   [hc.Data#isParentOf](hc.Data.html#isParentOf)

#### isRelatedTo(data) → {Boolean}

判断自身与指定data是否有父子或子孙关系

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;要对比的数据元素  

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
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`child`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;被删除的孩子元素  
`index`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;索引


Inherited From:

*   [hc.Data#onChildAdded](hc.Data.html#onChildAdded)

#### onChildRemoved(child, index)

删除孩子时的回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`child`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;被删除的孩子元素  
`index`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;索引


Inherited From:

*   [hc.Data#onChildRemoved](hc.Data.html#onChildRemoved)

#### onParentChanged(oldParent, parent)

改变父亲元素时的回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`oldParent`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;旧的父元素  
`parent`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;新的父元素

Inherited From:

*   [hc.Data#onParentChanged](hc.Data.html#onParentChanged)

#### onPropertyChanged(event)

属性变化回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp; Description  
`event`&emsp;&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;属性变化事件

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
`name`&emsp;&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;样式名  
`oldValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;旧的样式值  
`newValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;新的样式值

Inherited From:

*   [hc.Data#onStyleChanged](hc.Data.html#onStyleChanged)

#### removeChild(child)

删除指定孩子元素，内部会自动调用孩子元素的setParent

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`child`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;要删除的孩子元素  

Inherited From:

*   [hc.Data#removeChild](hc.Data.html#removeChild)

#### removeStyleIcon(name)

删除icon

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp;String&emsp;&emsp;要删除的icon名  

Inherited From:

*   [hc.Data#removeStyleIcon](hc.Data.html#removeStyleIcon)

#### s(name, value) → {Object}

获取或设置样式，仅有一个参数时相当于[getStyle](hc.Data.html#getStyle)，有两个参数时相当于[setStyle](hc.Data.html#setStyle)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;样式名  
`value`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;样式值

##### Returns:

Object

Inherited From:

*   [hc.Data#s](hc.Data.html#s)

#### setAdjustChildrenToTop(adjustToTop)

GraphView点击图元会自动sendToTop，该属性决定是否对子图元也进行sendToTop操作

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`adjustToTop`&emsp;&emsp;Boolean&emsp;&emsp;是否将children自动sendToTop  

Inherited From:

*   [hc.Data#setAdjustChildrenToTop](hc.Data.html#setAdjustChildrenToTop)

#### setAttr(name, value)

设置attr属性

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;String&emsp;&emsp;&emsp;属性名  
`value`&emsp;&emsp;Object&emsp;&emsp;属性值

Inherited From:

*   [hc.Data#setAttr](hc.Data.html#setAttr)

#### setAttrObject(attrObject)

设置attr属性对象，该属性默认为空，用于存储用户业务信息

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`attrObject`&emsp;&emsp;Object&emsp;&emsp;attr属性对象

Inherited From:

*   [hc.Data#setAttrObject](hc.Data.html#setAttrObject)

#### setClosable(v)

设置页签是否可被关闭

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;Boolean

#### setDisabled(v)

设置页签是否被禁用

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;Boolean

#### setDisplayName(displayName)

设置显示名称，常作为Column和Property的列头和属性名称显示

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`displayName`&emsp;&emsp;String&emsp;&emsp;显示名称 

Inherited From:

*   [hc.Data#setDisplayName](hc.Data.html#setDisplayName)

#### setIcon(icon)

设置小图标名称，常作为TreeView和ListView等组件上的节点小图标

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`icon`&emsp;&emsp;&emsp;&emsp;String | Object&emsp;&emsp;图标名或矢量  

Inherited From:

*   [hc.Data#setIcon](hc.Data.html#setIcon)

#### setId(id)

设置唯一编号，如果手工设置，一定要确保在data加入到DataModel之前设置并且唯一不重复

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`id`&emsp;&emsp;&emsp;&emsp; String | Number&emsp;&emsp;唯一编号  


Inherited From:

*   [hc.Data#setId](hc.Data.html#setId)

#### setLayer(layer)

设置数据元素在GraphView组件中的图层位置

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`layer`&emsp;&emsp;&emsp;String | Number&emsp;&emsp;图层名  

Inherited From:

*   [hc.Data#setLayer](hc.Data.html#setLayer)

#### setName(name)

设置数据元素名称

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;数据元素名称  

Inherited From:

*   [hc.Data#setName](hc.Data.html#setName)

#### setParent(parent)

设置父元素

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`parent`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;父元素  

Inherited From:

*   [hc.Data#setParent](hc.Data.html#setParent)

#### setStyle(name, value)

设置样式

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;样式名  
`value`&emsp;&emsp; Object&emsp;&emsp;&emsp;样式值

Inherited From:

*   [hc.Data#setStyle](hc.Data.html#setStyle)

#### setTag(tag)

设置标识号，可通过[getDataByTag](hc.DataModel.html#getDataByTag)快速查找

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`tag`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;标识号

Inherited From:

*   [hc.Data#setTag](hc.Data.html#setTag)

#### setToolTip(toolTip)

设置文字提示信息

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`toolTip`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;文字提示

Inherited From:

*   [hc.Data#setToolTip](hc.Data.html#setToolTip)

#### setView(v)

设置页签被选中时呈现的视图组件

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;htmlElement

#### size() → {Number}

获取孩子元素总数

##### Returns:

Number - 孩子元素总数

Inherited From:

*   [hc.Data#size](hc.Data.html#size)

#### toChildren(matchFunc, scope) → {[hc.List](hc.List.html)}

以matchFunc为过滤函数构建新的孩子元素集合

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`matchFunc`&emsp;&emsp;function&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;过滤函数  
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

