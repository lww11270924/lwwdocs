
#### new Column()

列数据，用于定义表格组件的列信息，包含列名称、类型以及自定义渲染和编辑单元格等信息

### Extends

*   [hc.Data](hc.Data.hcml)

### Methods

#### a(name, value) → {Object}

获取或设置attr属性，仅有一个参数时相当于[getAttr](hc.Data.hcml#getAttr)，有两个参数时相当于[setAttr](hc.Data.hcml#setAttr)

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Attributes&emsp;&emsp;Description  
`name`&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;属性名  
`value`&emsp;&emsp;Object&emsp;\<optional>&emsp;属性值

##### Returns:

Object

Inherited From:

*   [hc.Data#a](hc.Data.hcml#a)

#### addChild(child, index)

添加孩子节点，index为孩子插入索引，为空则插入作为最后的孩子，内部会自动调用child的setParent

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Attributes&emsp;&emsp;Description  
`child`&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;孩子元素  
`index`&emsp;&emsp;Number&emsp;\<optional>&emsp;插入索引

Inherited From:

*   [hc.Data#addChild](hc.Data.hcml#addChild)

#### addStyleIcon(name, icon)

增加icon，icon参数请参考beginner guide

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Attributes&emsp;&emsp;Description  
`name`&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;icon名  
`icon`&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;icon参数

Inherited From:

*   [hc.Data#addStyleIcon](hc.Data.hcml#addStyleIcon)

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

*   [hc.Data#clearChildren](hc.Data.hcml#clearChildren)

#### dm() → {[hc.DataModel](hc.DataModel.hcml)}

获取[DataModel](hc.DataModel.hcml)，[getDataModel](hc.Data.hcml#getDataModel)的缩写

##### Returns:

[hc.DataModel](hc.DataModel.hcml) -

dataModel

Inherited From:

*   [hc.Data#dm](hc.Data.hcml#dm)

#### eachChild(func, scope)

遍历孩子元素

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Attributes&emsp;&emsp;Description  
`func`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;遍历函数  
`scope`&emsp;&emsp;Object&emsp;&emsp;\<optional>&emsp;函数域

Inherited From:

*   [hc.Data#eachChild](hc.Data.hcml#eachChild)

##### Example

    data.eachChild(function(child) {
       console.log(child.getId());
    });

#### firePropertyChange(property, oldValue, newValue)

派发属性变化事件

#### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Attributes&emsp;&emsp;Description  
`property`&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;属性名   
`oldValue`&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;旧值  
`newValue`&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;新值  

Inherited From:

*   [hc.Data#firePropertyChange](hc.Data.hcml#firePropertyChange)

#### formatValue(value) → {Object}

将要显示的值传入此方法格式化处理并返回，一般用于将数字转换更易读的文本格式，可重载自定义

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`value`&emsp;&emsp;Object&emsp;&emsp;&emsp;格式化之前值   

##### Returns:

Object -

格式化之后的值

#### fp(property, oldValue, newValue)

派发属性变化事件，同[firePropertyChange](hc.Data.hcml#firePropertyChange)

#### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Attributes&emsp;&emsp;Description  
`property`&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;属性名   
`oldValue`&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;旧值  
`newValue`&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;新值  

Inherited From:

*   [hc.Data#fp](hc.Data.hcml#fp)

#### getAccessType() → {String|null}

获取列的属性类型，值列表如下：  

  
*   null: 默认类型，如name为age，采用getAge()和setAge(98)的get/set或is/set方式存取
  
*   style: 如name为age，采用getStyle('age')和setStyle('age', 98)的方式存取
  
*   field：如name为age，采用data.age和data.age = 98的方式存取
  
*   attr：如name为age，采用getAttr('age')和setAttr('age', 98)的方式存取
  

##### Returns:

String | null

#### getAlign() → {String}

获取文字的水平对齐方式，可用值有left|righc|center，默认为left

##### Returns:

String

#### getAttr(name) → {Object}

获取attr属性

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;String&emsp;&emsp;&emsp;属性名   

##### Returns:

Object

Inherited From:

*   [hc.Data#getAttr](hc.Data.hcml#getAttr)

#### getAttrObject() → {Object}

获取attr属性对象，该属性默认为空，用于存储用户业务信息

##### Returns:

Object -

attr属性对象

Inherited From:

*   [hc.Data#getAttrObject](hc.Data.hcml#getAttrObject)

#### getChildAt(index) → {[hc.Data](hc.Data.hcml)}

返回指定索引位置的孩子

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp; Description  
`index`&emsp;&emsp;String&emsp;&emsp;索引   

##### Returns:

[hc.Data](hc.Data.hcml) -

索引对应的孩子

Inherited From:

*   [hc.Data#getChildAt](hc.Data.hcml#getChildAt)

#### getChildren() → {[hc.List](hc.List.hcml)}

获取所有孩子节点

##### Returns:

[hc.List](hc.List.hcml) -

孩子元素集合

Inherited From:

*   [hc.Data#getChildren](hc.Data.hcml#getChildren)

#### getClass() → {function}

获取类声明(构造函数)

##### Returns:

function -

类声明(构造函数)

Inherited From:

*   [hc.Data#getClass](hc.Data.hcml#getClass)

#### getClassName() → {String}

获取类全名，继承Data并希望序列化时应该重写此方法返回子类的类名字符串

##### Returns:

String -

类全名

Inherited From:

*   [hc.Data#getClassName](hc.Data.hcml#getClassName)

See:

*   [hc.Data#getSuperClass](hc.Data.hcml#getSuperClass)

#### getColor() → {color}

获取表头文字的颜色

##### Returns:

color

#### getColorPicker() → {Object}

获取颜色选择器配置

##### Returns:

Object

See:

*   [setColorPicker](hc.Column.hcml#setColorPicker)

#### getDataModel() → {[hc.DataModel](hc.DataModel.hcml)}

获取所属的DataModel

##### Returns:

[hc.DataModel](hc.DataModel.hcml) -

DataModel数据容器

Inherited From:

*   [hc.Data#getDataModel](hc.Data.hcml#getDataModel)

#### getDisplayName() → {String}

获取显示名称，常作为Column和Property的列头和属性名称显示

##### Returns:

String -

显示名称

Inherited From:

*   [hc.Data#getDisplayName](hc.Data.hcml#getDisplayName)

#### getEnumIcons() → {Array}

当此列使用下拉列表作为编辑器时，此方法返回下拉列表的所有枚举icon数组

##### Returns:

Array

#### getEnumLabels() → {Array}

当此列使用下拉列表作为编辑器时，此方法返回下拉列表的所有枚举文字数组

##### Returns:

Array

#### getEnumMaxHeighc() → {Array}

当此列使用下拉列表作为编辑器时，此方法返回下拉列表的最大高度(超出使用滚动条)

##### Returns:

Array

#### getEnumValues() → {Array}

当此列使用下拉列表作为编辑器时，此方法返回下拉列表的值数组

##### Returns:

Array

#### getIcon() → {String|Object}

获取小图标名称，常作为TreeView和ListView等组件上的节点小图标

##### Returns:

String | Object -

图标名或矢量

Inherited From:

*   [hc.Data#getIcon](hc.Data.hcml#getIcon)

#### getId() → {Number}

获取唯一编号

##### Returns:

Number -

唯一编号

Inherited From:

*   [hc.Data#getId](hc.Data.hcml#getId)

#### getItemEditor() → {function}

获取自定义的单元格编辑器

##### Returns:

function

#### getLayer() → {String|Number}

获取数据元素在GraphView组件中的图层位置

##### Returns:

String | Number -

图层名

Inherited From:

*   [hc.Data#getLayer](hc.Data.hcml#getLayer)

Default Value:

*   0

#### getName() → {String}

获取数据元素名

##### Returns:

String -

名称

Inherited From:

*   [hc.Data#getName](hc.Data.hcml#getName)

#### getParent() → {[hc.Data](hc.Data.hcml)}

获取父元素

##### Returns:

[hc.Data](hc.Data.hcml) -

父元素

Inherited From:

*   [hc.Data#getParent](hc.Data.hcml#getParent)

#### getSerializableAttrs() → {Object}

此函数返回一个map，决定序列化时哪些attr属性可被序列化，默认所有attr对象里的属性都会被序列化

##### Returns:

Object -

需要被序列化的attr属性map

Inherited From:

*   [hc.Data#getSerializableAttrs](hc.Data.hcml#getSerializableAttrs)

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

Inherited From:

*   [hc.Data#getSerializableProperties](hc.Data.hcml#getSerializableProperties)

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

Inherited From:

*   [hc.Data#getSerializableStyles](hc.Data.hcml#getSerializableStyles)

##### Example

    function(){
        var name, map = {};
        for (name in this._styleMap) {
            map[name] = 1;
        }
        return map;
    }

#### getSlider() → {Object}

获取拉条配置

##### Returns:

Object

See:

*   [setSlider](hc.Column.hcml#setSlider)

#### getSortFunc() → {function}

获取排序函数

##### Returns:

function

#### getSortOrder() → {String}

获取排序状态  

  
*   asc: 升序
  
*   desc: 降序
  

##### Returns:

String

#### getStyle(name) → {Object}

获取样式属性

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp;String&emsp;&emsp;样式名   

##### Returns:

Object

Inherited From:

*   [hc.Data#getStyle](hc.Data.hcml#getStyle)

#### getStyleMap() → {Object}

获取图元内部样式映射信息

##### Returns:

Object -

样式映射表

Inherited From:

*   [hc.Data#getStyleMap](hc.Data.hcml#getStyleMap)

#### getSuperClass() → {function}

获取父类声明(构造函数)，继承类时可以用来调用父类构造或函数

##### Returns:

function -

父类声明(构造函数)

Inherited From:

*   [hc.Data#getSuperClass](hc.Data.hcml#getSuperClass)

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

Inherited From:

*   [hc.Data#getTag](hc.Data.hcml#getTag)

#### getToolTip(data, tableView) → {String}

获取toolTip文字

#### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;数据元素  
`tableView`&emsp;[hc.widget.TableView](hc.widget.TableView.hcml)&emsp;视图对象 

##### Returns:

String

Overrides:

*   [hc.Data#getToolTip](hc.Data.hcml#getToolTip)

#### getUIClass() → {function}

获取拓扑组件上的UI类

##### Returns:

function -

UI类声明(构造函数)

Inherited From:

*   [hc.Data#getUIClass](hc.Data.hcml#getUIClass)

#### getValueType() → {String}

获取值类型，值类型用于提示组件提供合适的renderer渲染，合适的编辑控件，及改变值时必要的类型转换  

  
*   null：默认类型，显示为文本方式
  
*   string：字符串类型，显示为文本方式
  
*   boolean：布尔类型，显示为勾选框
  
*   color：颜色类型，以填充背景色的方式显示
  
*   int：整型类型，文本编辑器改变值时自动通过parseInt进行转换
  
*   number：浮点数类型，文本编辑器改变值时自动通过parseFloat转换
  

##### Returns:

String

#### getWidth() → {Number}

获取列宽度

##### Returns:

Number

#### hasChildren() → {Boolean}

判断是否有孩子

##### Returns:

Boolean -

是否有孩子

Inherited From:

*   [hc.Data#hasChildren](hc.Data.hcml#hasChildren)

#### invalidate()

强制触发属性变化事件通知界面更新

Inherited From:

*   [hc.Data#invalidate](hc.Data.hcml#invalidate)

#### isAdjustChildrenToTop() → {Boolean}

GraphView点击图元会自动sendToTop，该属性决定是否对子图元也进行sendToTop操作

##### Returns:

Boolean -

是否将children自动sendToTop

Inherited From:

*   [hc.Data#isAdjustChildrenToTop](hc.Data.hcml#isAdjustChildrenToTop)

#### isBatchEditable() → {Boolean}

判断该列是否允许多选时批量编辑，默认为true

##### Returns:

Boolean

#### isDescendantOf(data) → {Boolean}

判断自身是否为指定data的子孙

#### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;要对比的数据元素  
`tableView`&emsp;[hc.widget.TableView](hc.widget.TableView.hcml)&emsp;视图对象 


##### Returns:

Boolean -

自身是否为指定data的子孙

Inherited From:

*   [hc.Data#isDescendantOf](hc.Data.hcml#isDescendantOf)

#### isEditable() → {Boolean}

判断此列是否可编辑

##### Returns:

Boolean

#### isEmptiable() → {Boolean}

判断属性是否可为空字符串，可避免输入空字符串，空字符串转换成undefined。默认为false

##### Returns:

Boolean

#### isEmpty() → {Boolean}

判断是否有孩子，同[hasChildren](hc.Data.hcml#hasChildren)

##### Returns:

Boolean -

是否有孩子

Inherited From:

*   [hc.Data#isEmpty](hc.Data.hcml#isEmpty)

#### isEnumEditable() → {Boolean}

枚举下拉编辑器是否允许可输入，默认为false

##### Returns:

Boolean

#### isEnumStrict() → {Boolean}

判断值匹配时是否采用严格的===进行比较，默认为true，若为false则采用==进行比较

##### Returns:

Boolean

#### isNullable() → {Boolean}

判断属性是否可为空，默认为true，设置为false可避免输入null或undefined

##### Returns:

Boolean

#### isParentOf(data) → {Boolean}

判断自身是否为指定data的父亲

#### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;要对比的数据元素  

##### Returns:

Boolean -

自身是否为指定data的父亲

Inherited From:

*   [hc.Data#isParentOf](hc.Data.hcml#isParentOf)

#### isRelatedTo(data) → {Boolean}

判断自身与指定data是否有父子或子孙关系

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;要对比的数据元素  


##### Returns:

Boolean -

自身与指定data是否有父子或子孙关系

Inherited From:

*   [hc.Data#isRelatedTo](hc.Data.hcml#isRelatedTo)

#### isSortable() → {Boolean}

判断当前列是否可排序

##### Returns:

Boolean

#### isVisible() → {Boolean}

判断当前列是否是否可见

##### Returns:

Boolean

#### iv()

强制触发属性变化事件通知界面更新，[invalidate](hc.Data.hcml#invalidate)的缩写

Inherited From:

*   [hc.Data#iv](hc.Data.hcml#iv)

#### onChildAdded(child, index)

添加孩子时的回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`child`&emsp;&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;新增加的孩子元素  
`index`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;索引 

Inherited From:

*   [hc.Data#onChildAdded](hc.Data.hcml#onChildAdded)

#### onChildRemoved(child, index)

删除孩子时的回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`child`&emsp;&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;新增加的孩子元素  
`index`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;索引 

Inherited From:

*   [hc.Data#onChildRemoved](hc.Data.hcml#onChildRemoved)

#### onParentChanged(oldParent, parent)

改变父亲元素时的回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`oldParent`&emsp;&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;旧的父元素  
`parent`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;新的父元素 

Inherited From:

*   [hc.Data#onParentChanged](hc.Data.hcml#onParentChanged)

#### onPropertyChanged(event)

属性变化回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`event`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;属性变化事件  

Inherited From:

*   [hc.Data#onPropertyChanged](hc.Data.hcml#onPropertyChanged)

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
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;样式名  
`oldValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;旧的样式值  
`newValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;新的样式值 

Inherited From:

*   [hc.Data#onStyleChanged](hc.Data.hcml#onStyleChanged)

#### removeChild(child)

删除指定孩子元素，内部会自动调用孩子元素的setParent

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`child`&emsp;&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;要删除的孩子元素  

Inherited From:

*   [hc.Data#removeChild](hc.Data.hcml#removeChild)

#### removeStyleIcon(name)

删除icon

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;要删除的icon名 

Inherited From:

*   [hc.Data#removeStyleIcon](hc.Data.hcml#removeStyleIcon)

#### s(name, value) → {Object}

获取或设置样式，仅有一个参数时相当于[getStyle](hc.Data.hcml#getStyle)，有两个参数时相当于[setStyle](hc.Data.hcml#setStyle)

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;样式名  
`value`&emsp;&emsp; Object&emsp;&emsp;\<optional> &emsp;&emsp;&emsp;样式值  

##### Returns:

Object

Inherited From:

*   [hc.Data#s](hc.Data.hcml#s)

#### setAccessType(accessType)

设置列的属性类型，可选值如下：  

  
*   null: 默认类型，如name为age，采用getAge()和setAge(98)的get/set或is/set方式存取
  
*   style: 如name为age，采用getStyle('age')和setStyle('age', 98)的方式存取
  
*   field：如name为age，采用data.age和data.age = 98的方式存取
  
*   attr：如name为age，采用getAttr('age')和setAttr('age', 98)的方式存取
  

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`accessType`&emsp;&emsp;&emsp;String | null&emsp;&emsp;&emsp;样式名  

#### setAdjustChildrenToTop(adjustToTop)

GraphView点击图元会自动sendToTop，该属性决定是否对子图元也进行sendToTop操作

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`adjustToTop`&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;是否将children自动sendToTop  

Inherited From:

*   [hc.Data#setAdjustChildrenToTop](hc.Data.hcml#setAdjustChildrenToTop)

#### setAlign(align)

设置文字的水平对齐方式，可用值有left|righc|center，默认为left

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`align`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;对齐方式  

#### setAttr(name, value)

设置attr属性

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;属性名    
`value`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;属性值  

Inherited From:

*   [hc.Data#setAttr](hc.Data.hcml#setAttr)

#### setAttrObject(attrObject)

设置attr属性对象，该属性默认为空，用于存储用户业务信息

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`attrObject`&emsp;&emsp;Object&emsp;&emsp;&emsp;attr属性对象    

Inherited From:

*   [hc.Data#setAttrObject](hc.Data.hcml#setAttrObject)

#### setBatchEditable(v)

设置该列是否允许多选时批量编辑，默认为true

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Boolean 

#### setColor(color)

设置表头文字的颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;&emsp;color

#### setColorPicker(v)

设置颜色选择器配置，需要引入form插件，设置此属性后，此列将使用颜色选择器作为单元格编辑器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Object  


颜色选择器配置，如{background: 'red'}可以指定颜色选择器背景为红色，如果要使用默认配置，使用空对象{}即可

#### setDisplayName(displayName)

设置显示名称，常作为Column和Property的列头和属性名称显示

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`displayName`&emsp;&emsp;String&emsp;&emsp;&emsp;显示名称  


Inherited From:

*   [hc.Data#setDisplayName](hc.Data.hcml#setDisplayName)

#### setEditable(editable)

设置此列是否可编辑

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`editable`&emsp;&emsp;Boolean

#### setEmptiable(emptiable)

设置属性是否可为空字符串，可避免输入空字符串，空字符串转换成undefined。默认为false

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`emptiable`&emsp;&emsp;Boolean
#### setEnum(v)

设置枚举列表，此列自动采用下拉列表作为单元格编辑器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Object | Array

##### Example

    //示例，参数依次表示：值，文字、icon
    column.setEnum([1,2,3], ['C','C++','JS'], ['c_icon', 'c++_icon', 'js_icon']);
    //也可以使用对象的方式：
    column.setEnum({values:[1,2,3], labels:['C','C++','JS'], icons:['c_icon', 'c++_icon', 'js_icon']});

#### setIcon(icon)

设置小图标名称，常作为TreeView和ListView等组件上的节点小图标

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`icon`&emsp;&emsp;&emsp;&emsp;String | Object&emsp;图标名或矢量

Inherited From:

*   [hc.Data#setIcon](hc.Data.hcml#setIcon)

#### setId(id)

设置唯一编号，如果手工设置，一定要确保在data加入到DataModel之前设置并且唯一不重复

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`id`&emsp;&emsp;&emsp;&emsp;String | Number&emsp;唯一编号

Inherited From:

*   [hc.Data#setId](hc.Data.hcml#setId)

#### setItemEditor(editor)

设置自定义的单元格编辑器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`editor`&emsp;&emsp;&emsp;&emsp;function

#### setLayer(layer)

设置数据元素在GraphView组件中的图层位置

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`layer`&emsp;&emsp;&emsp;&emsp;String | Number&emsp;&emsp;图层名

Inherited From:

*   [hc.Data#setLayer](hc.Data.hcml#setLayer)

#### setName(name)

设置数据元素名称

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;数据元素名称

Inherited From:

*   [hc.Data#setName](hc.Data.hcml#setName)

#### setNullable(nullable)

设置属性是否可为空，默认为true，设置为false可避免输入null或undefined

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`nullable`&emsp;&emsp;Boolean

#### setParent(parent)

设置父元素

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`parent`&emsp;&emsp;[hc.Data](hc.Data.hcml)&emsp;&emsp;&emsp;&emsp;父元素

Inherited From:

*   [hc.Data#setParent](hc.Data.hcml#setParent)

#### setSlider(v)

设置拉条配置，需要引入form插件，设置此属性后，此列将使用拉条作为单元格编辑器

##### Parameters:
>Name&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;Object

拉条配置，如{background: 'red'}可以指定拉条背景为红色，如果要使用默认配置，使用空对象{}即可

#### setSortable(nullable)

设置当前列是否可排序

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`nullable`&emsp;&emsp;Boolean

#### setSortFunc(func)

设置排序函数

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`func`&emsp;&emsp;function

#### setSortOrder(sortOrder)

设置排序状态  

  
*   asc: 升序
  
*   desc: 降序
  

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`sortOrder`&emsp;&emsp;String

#### setStyle(name, value)

设置样式

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp;String&emsp;&emsp;样式名  
`value`&emsp;&emsp;Object&emsp;&emsp;样式值

Inherited From:

*   [hc.Data#setStyle](hc.Data.hcml#setStyle)

#### setTag(tag)

设置标识号，可通过[getDataByTag](hc.DataModel.hcml#getDataByTag)快速查找

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`tag`&emsp;&emsp;String&emsp;&emsp;标识号  

Inherited From:

*   [hc.Data#setTag](hc.Data.hcml#setTag)

#### setToolTip(toolTip)

设置文字提示信息

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`toolTip`&emsp;&emsp;String&emsp;&emsp;文字提示  

Inherited From:

*   [hc.Data#setToolTip](hc.Data.hcml#setToolTip)

#### setValueType(type)

设置值类型，值类型用于提示组件提供合适的renderer渲染，合适的编辑控件，及改变值时必要的类型转换  

  
*   null：默认类型，显示为文本方式
  
*   string：字符串类型，显示为文本方式
  
*   boolean：布尔类型，显示为勾选框
  
*   color：颜色类型，以填充背景色的方式显示
  
*   int：整型类型，文本编辑器改变值时自动通过parseInt进行转换
  
*   number：浮点数类型，文本编辑器改变值时自动通过parseFloat转换
  

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`type`&emsp;&emsp;String | null

#### setVisible(v)

设置当前列是否是否可见

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Boolean


#### setWidth(v)

设置列宽度

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Number

#### size() → {Number}

获取孩子元素总数

##### Returns:

Number -

孩子元素总数

Inherited From:

*   [hc.Data#size](hc.Data.hcml#size)

#### toChildren(matchFunc, scope) → {[hc.List](hc.List.hcml)}

以matchFunc为过滤函数构建新的孩子元素集合

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description  
`matchFunc`&emsp;&emsp;function&emsp;&emsp;\<optional>&emsp;&emsp;过滤函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp; \<optional>&emsp;&emsp; 函数域

##### Returns:

[hc.List](hc.List.hcml) -

孩子元素集合

Inherited From:

*   [hc.Data#toChildren](hc.Data.hcml#toChildren)

##### Example

    var list = data.toChildren(function(child) {
       if (child.a('visible')) {
       	return true;
       }
    });

#### toEnumIcon(value) → {String}

根据value查找对应的枚举icon

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`value`&emsp;&emsp;Object&emsp;&emsp;枚举值

##### Returns:

String

#### toEnumLabel(value) → {String}

根据value查找对应的枚举label文字

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`value`&emsp;&emsp;Object&emsp;&emsp;枚举值

##### Returns:

String

#### toLabel() → {String}

返回值作为TreeView和GraphView等组件上的图元文字标签，默认返回displayName||name信息

##### Returns:

String -

文字标签

Inherited From:

*   [hc.Data#toLabel](hc.Data.hcml#toLabel)

#### toString() → {String}

重写js默认的toString

##### Returns:

String

Inherited From:

*   [hc.Data#toString](hc.Data.hcml#toString)
