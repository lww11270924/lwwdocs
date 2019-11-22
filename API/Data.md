#### new Data()

数据元素基类，包含基本属性设置、样式设置、事件派发、父子关系等功能

### Methods

#### a(name, value) → {Object}

获取或设置attr属性；  
1、一个参数：  
· 当参数为 String 时相当于 [getAttr](API/Data.md#getAttr)；  
· 当参数为 Object 时，则会遍历该 Object 中的属性，逐个调用 [setAttr](API/Data.md#setAttr) 设置属性值；  
2、两个参数：  
· 相当于 [setAttr](API/Data.md#setAttr)

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;String | Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;属性名 | 属性键值对对象  
`value`&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;&emsp;属性值

##### Returns:

Object

#### addChild(child, index)

添加孩子节点，index为孩子插入索引，为空则插入作为最后的孩子，内部会自动调用child的setParent

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description  
`child`&emsp;&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;孩子元素  
`index`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;&emsp;插入索引



#### addStyleIcon(name, icon)

增加icon，icon参数请参考beginner guide

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp;String&emsp;&emsp;icon名 
`icon`&emsp;&emsp;Object&emsp;&emsp;icon参数 


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

#### dm() → {[hc.DataModel](hc.DataModel.hcml)}

获取[DataModel](hc.DataModel.hcml)，[getDataModel](hc.Data.hcml#getDataModel)的缩写

##### Returns:

[hc.DataModel](hc.DataModel.hcml) -

dataModel

#### eachChild(func, scope)

遍历孩子元素

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;遍历函数  
`scope`&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域

##### Example

    data.eachChild(function(child) {
       console.log(child.getId());
    });

#### firePropertyChange(property, oldValue, newValue)

派发属性变化事件

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`property`&emsp;&emsp;String&emsp;&emsp;属性名
`oldValue`&emsp;&emsp;Object&emsp;&emsp;旧值  
`newValue`&emsp;&emsp;Object&emsp;&emsp;新值 

#### fp(property, oldValue, newValue)

派发属性变化事件，同[firePropertyChange](hc.Data.hcml#firePropertyChange)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`property`&emsp;&emsp;String&emsp;&emsp;属性名
`oldValue`&emsp;&emsp;Object&emsp;&emsp;旧值  
`newValue`&emsp;&emsp;Object&emsp;&emsp;新值 

#### getAttr(name) → {Object}

获取attr属性

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp;String&emsp;&emsp;属性名

##### Returns:

Object

#### getAttrObject() → {Object}

获取attr属性对象，该属性默认为空，用于存储用户业务信息

##### Returns:

Object -

attr属性对象

#### getChildAt(index) → {[hc.Data](hc.Data.hcml)}

返回指定索引位置的孩子

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`index`&emsp;&emsp;Number&emsp;&emsp;索引

##### Returns:

[hc.Data](hc.Data.hcml) - 索引对应的孩子

#### getChildren() → {[hc.List](hc.List.hcml)}

获取所有孩子节点

##### Returns:

[hc.List](hc.List.hcml) - 孩子元素集合

#### getClass() → {function}

获取类声明(构造函数)

##### Returns:

function -

类声明(构造函数)

#### getClassName() → {String}

获取类全名，继承Data并希望序列化时应该重写此方法返回子类的类名字符串

##### Returns:

String -

类全名

See:

*   [hc.Data#getSuperClass](hc.Data.hcml#getSuperClass)

#### getDataModel() → {[hc.DataModel](hc.DataModel.hcml)}

获取所属的DataModel

##### Returns:

[hc.DataModel](hc.DataModel.hcml) -

DataModel数据容器

#### getDisplayName() → {String}

获取显示名称，常作为Column和Property的列头和属性名称显示

##### Returns:

String -

显示名称

#### getIcon() → {String|Object}

获取小图标名称，常作为TreeView和ListView等组件上的节点小图标

##### Returns:

String | Object -

图标名或矢量

#### getId() → {Number}

获取唯一编号

##### Returns:

Number -

唯一编号

#### getLayer() → {String|Number}

获取数据元素在GraphView组件中的图层位置

##### Returns:

String | Number -

图层名

Default Value:

*   0

#### getName() → {String}

获取数据元素名

##### Returns:

String -

名称

#### getParent() → {[hc.Data](hc.Data.hcml)}

获取父元素

##### Returns:

[hc.Data](hc.Data.hcml) -

父元素

#### getSerializableAttrs() → {Object}

此函数返回一个map，决定序列化时哪些attr属性可被序列化，默认所有attr对象里的属性都会被序列化

##### Returns:

Object -

需要被序列化的attr属性map

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

Object -

需要被序列化的属性map

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

Object -

需要被序列化的样式map

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
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp;String&emsp;&emsp;样式名

##### Returns:

Object

#### getStyleMap() → {Object}

获取图元内部样式映射信息

##### Returns:

Object -

样式映射表

#### getSuperClass() → {function}

获取父类声明(构造函数)，继承类时可以用来调用父类构造或函数

##### Returns:

function -

父类声明(构造函数)

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

获取标识号，可通过[getDataByTag](hc.DataModel.hcml#getDataByTag)快速查找

##### Returns:

String -

标识号

#### getToolTip() → {String}

获取文字提示信息

##### Returns:

String -

文字提示

#### getUIClass() → {function}

获取拓扑组件上的UI类

##### Returns:

function -

UI类声明(构造函数)

#### hasChildren() → {Boolean}

判断是否有孩子

##### Returns:

Boolean -

是否有孩子

#### invalidate()

强制触发属性变化事件通知界面更新

#### isAdjustChildrenToTop() → {Boolean}

GraphView点击图元会自动sendToTop，该属性决定是否对子图元也进行sendToTop操作

##### Returns:

Boolean -

是否将children自动sendToTop

#### isDescendantOf(data) → {Boolean}

判断自身是否为指定data的子孙

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;要对比的数据元素

##### Returns:

Boolean -

自身是否为指定data的子孙

#### isEmpty() → {Boolean}

判断是否有孩子，同[hasChildren](hc.Data.hcml#hasChildren)

##### Returns:

Boolean -

是否有孩子

#### isParentOf(data) → {Boolean}

判断自身是否为指定data的父亲

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;要对比的数据元素

##### Returns:

Boolean -

自身是否为指定data的父亲

#### isRelatedTo(data) → {Boolean}

判断自身与指定data是否有父子或子孙关系

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;要对比的数据元素

##### Returns:

Boolean -

自身与指定data是否有父子或子孙关系

#### iv()

强制触发属性变化事件通知界面更新，[invalidate](hc.Data.hcml#invalidate)的缩写

#### onChildAdded(child, index)

添加孩子时的回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp; Description  
`child`&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;新增加的孩子元素
`index`&emsp;&emsp;Number&emsp;索引


#### onChildRemoved(child, index)

删除孩子时的回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp; Description  
`child`&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;被删除的孩子元素
`index`&emsp;&emsp;Number&emsp;索引

#### onParentChanged(oldParent, parent)

改变父亲元素时的回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp; Description  
`oldParent`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;旧的父元素
`parent`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;新的父元素

#### onPropertyChanged(event)

属性变化回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp; Description  
`event`&emsp;&emsp;&emsp;Object&emsp;&emsp;属性变化事件


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


#### removeChild(child)

删除指定孩子元素，内部会自动调用孩子元素的setParent

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp; Description  
`child`&emsp;&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;要删除的孩子元素


#### removeStyleIcon(name)

删除icon

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp; Description  
`name`&emsp;&emsp;&emsp;String&emsp;要删除的icon名

#### s(name, value) → {Object}

获取或设置样式；  
1、一个参数：  
· 当参数为 String 时相当于 [getStyle](hc.Data.hcml#getStyle)；  
· 当参数为 Object 时，则会遍历该 Object 中的属性，逐个调用 [setStyle](hc.Data.hcml#setStyle) 设置属性值；  
2、两个参数：  
· 相当于 [setStyle](hc.Data.hcml#setStyle)

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;String | Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;样式名 | 样式键值对对象  
`value`&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;样式值

样式值

##### Returns:

Object

#### setAdjustChildrenToTop(adjustToTop)

GraphView点击图元会自动sendToTop，该属性决定是否对子图元也进行sendToTop操作

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`adjustToTop`&emsp;Boolean&emsp;&emsp;是否将children自动sendToTop


#### setAttr(name, value)

设置attr属性

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp;String&emsp;&emsp;属性名
`value`&emsp;&emsp;Object&emsp;&emsp;属性值

#### setAttrObject(attrObject)

设置attr属性对象，该属性默认为空，用于存储用户业务信息

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`attrObject`&emsp;Object&emsp;&emsp;attr属性对象


#### setDisplayName(displayName)

设置显示名称，常作为Column和Property的列头和属性名称显示

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`displayName`&emsp;String&emsp;&emsp;显示名称

#### setIcon(icon)

设置小图标名称，常作为TreeView和ListView等组件上的节点小图标

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`icon`&emsp;String | Object&emsp;图标名或矢量


#### setId(id)

设置唯一编号，如果手工设置，一定要确保在data加入到DataModel之前设置并且唯一不重复

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`id`&emsp;&emsp;&emsp;&emsp;String | Number&emsp;&emsp;&emsp;唯一编号

#### setLayer(layer)

设置数据元素在GraphView组件中的图层位置

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`layer`&emsp;&emsp;&emsp;String | Number&emsp;&emsp;&emsp;图层名

#### setName(name)

设置数据元素名称

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;数据元素名称

#### setParent(parent)

设置父元素

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`parent`&emsp;&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;&emsp;&emsp;父元素

#### setStyle(name, value)

设置样式

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;样式名  
`value`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;样式值


#### setTag(tag)

设置标识号，可通过[getDataByTag](hc.DataModel.hcml#getDataByTag)快速查找

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`tag`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;标识号  

#### setToolTip(toolTip)

设置文字提示信息

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`toolTip`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;文字提示  

#### size() → {Number}

获取孩子元素总数

##### Returns:

Number -

孩子元素总数

#### toChildren(matchFunc, scope) → {[hc.List](hc.List.hcml)}

以matchFunc为过滤函数构建新的孩子元素集合

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`matchFunc`&emsp;&emsp;function&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;过滤函数
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域

##### Returns:

[hc.List](hc.List.hcml) -

孩子元素集合

##### Example

    var list = data.toChildren(function(child) {
       if (child.a('visible')) {
       	return true;
       }
    });

#### toLabel() → {String}

返回值作为TreeView和GraphView等组件上的图元文字标签，默认返回displayName||name信息

##### Returns:

String -

文字标签

#### toString() → {String}

重写js默认的toString

##### Returns:

String
