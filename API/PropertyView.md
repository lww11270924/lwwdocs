
[hc](hc.html)[.widget](hc.widget.html).PropertyView(dataModel)
--------------------------------------------------------------

#### new PropertyView(dataModel)

属性组件，用于显示Data类型对象属性，以分组、排序等方式展示属性

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`dataModel`&emsp;&emsp;[hc.DataModel](hc.DataModel.html)&emsp;&emsp;绑定的数据模型 

### Methods

#### addBottomPainter(painter)

增加底层Painter  
  
组件上提供Painter接口，开发者可以使用Canvas的画笔对象自由绘制任意形状，底层Painter绘制在组件最下面

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`painter`&emsp;&emsp;&emsp;function&emsp;&emsp;Painter类 

##### Example

    //Painter示例：
    graphView.addBottomPainter(function(g){
        g.fillStyle = '#000000';
        g.fillRect(0, 0, 100, 100);
    });

#### addProperties(properties)

以json的方式配置属性(新增)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp; Type&emsp;&emsp;Description  
`properties`&emsp;&emsp;&emsp;Array&emsp;&emsp;json属性 

##### Example

    //示例：
    propertyView.addProperties([{
    	name: 'id',
    	displayName: '序号'
    },
    {
    	name: 'background',
    	accessType: 'style'
    }
    ]);

#### addPropertyChangeListener(listener, scope, ahead)

增加自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [mp](hc.widget.PropertyView.html#mp)

#### addToDOM(parentNode)

将组件加入到指定的DOM元素底下，不指定则加入到 document.body 下

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`parentNode`&emsp;&emsp;&emsp;DOM&emsp;&emsp;DOM元素,默认为 document.body 


#### addTopPainter(painter)

增加顶层Painter  
  
组件上提供Painter接口，开发者可以使用Canvas的画笔对象自由绘制任意形状，顶层Painter绘制在组件最上面

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`painter`&emsp;&emsp;&emsp;function&emsp;&emsp;Painter类 

##### Example

    //Painter示例：
    graphView.addTopPainter(function(g){
        g.fillStyle = '#000000';
        g.fillRect(0, 0, 100, 100);
    });

#### addViewListener(listener, scope, ahead)

监听视图事件，如布局、刷新等

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

#### adjustTranslateY(value) → {Number}

传入即将设置的垂直平移值，返回最终设置值，可重载限制垂直平移范围

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`value`&emsp;&emsp;&emsp;Number&emsp;&emsp;原始垂直平移值   

##### Returns:

Number - 新的垂直平移值

#### collapse(categoryName)

合并分组

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`categoryName`&emsp;&emsp;&emsp;String&emsp;&emsp;分组名   

#### collapseAll()

合并所有分组

#### disableToolTip()

关闭ToolTip功能

#### dm(dataModel) → {[hc.DataModel](hc.DataModel.html)}

获取或设置数据模型，没有参数时相当于[getDataModel](hc.widget.PropertyView.html#getDataModel)，有参数时相当于[setDataModel](hc.widget.PropertyView.html#setDataModel)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;&emsp;Description  
`dataModel`&emsp;&emsp;[hc.DataModel](hc.DataModel.html)&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;&emsp; 数据模型

##### Returns:

[hc.DataModel](hc.DataModel.html) - dataModel

#### drawCategoryName(g, name, rowIndex, x, y, w, h)

绘制分组名，可重载自定义

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`g`&emsp;&emsp;&emsp;&emsp;&emsp;CanvasRenderingContext2D&emsp;&emsp;画笔对象  
`name`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;分组名  
`rowIndex`&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;行索引  
`x`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角x坐标  
`y`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角y坐标  
`width`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的宽度  
`heighc`&emsp;&emsp; Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的高度

#### drawPropertyName(g, property, rowIndex, x, y, w, h)

绘制分组名，可重载自定义

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`g`&emsp;&emsp;&emsp;&emsp;&emsp;CanvasRenderingContext2D&emsp;&emsp;画笔对象  
`property`&emsp;[hc.Property](hc.Property.html)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 属性对象  
`rowIndex`&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;行索引  
`x`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角x坐标  
`y`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角y坐标  
`w`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的宽度  
`h`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的高度

#### drawPropertyValue(g, property, value, rowIndex, x, y, w, w, data) → {htmlElement}

绘制属性值，可重载自定义，如果返回值为html元素，则使用html元素当作Renderer，一般重载Property的drawPropertyValue，无需重载此方法

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`g`&emsp;&emsp;&emsp;&emsp;&emsp;CanvasRenderingContext2D&emsp;&emsp;画笔对象  
`property`&emsp;[hc.Property](hc.Property.html)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 属性对象  
`value`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;值   
`rowIndex`&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;行索引  
`x`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角x坐标  
`y`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角y坐标  
`w`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的宽度  
`h`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的高度  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;数据元素 

##### Returns:

htmlElement

#### enableToolTip()

启用ToolTip

#### expand(categoryName)

展开分组

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; Type&emsp;&emsp;&emsp;Description  
`categoryName`&emsp;&emsp;&emsp;String&emsp;&emsp;分组名

#### expandAll()

展开所有分组

#### getBackground() → {color}

获取边框和分组行的背景颜色

##### Returns:

color

#### getCategoryColor(categoryName) → {color}

返回分组文本颜色，可重载自定义

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; Type&emsp;&emsp;&emsp;Description  
`categoryName`&emsp;&emsp;&emsp;String&emsp;&emsp;分组名

##### Returns:

color

#### getCategoryFont(categoryName) → {String}

返回分组文本字体，可重载自定义

##### Parameters:


##### Returns:

String

#### getCollapseIcon() → {String}

获取分组合并图标

##### Returns:

String

#### getColumnLineColor() → {color}

获取列线颜色

##### Returns:

color

#### getColumnPosition() → {Number}

获取列线位置比例，默认值0.5，允许范围为0~1

##### Returns:

Number

#### getCurrentData() → {[hc.Data](hc.Data.html)}

获取当前显示对象

##### Returns:

[hc.Data](hc.Data.html)

#### getDataModel() → {[hc.DataModel](hc.DataModel.html)}

获取绑定的数据模型

##### Returns:

[hc.DataModel](hc.DataModel.html) - 数据模型

#### getExpandIcon() → {String}

获取分组展开图标

##### Returns:

String

#### getHeighc() → {Number}

获取布局高度

##### Returns:

Number

#### getIndent() → {Number}

获取左侧缩进，左侧空间用于绘制分组toggle图标，以及属性提示icon图标

##### Returns:

Number

#### getLabelColor(property, value, rowIndex) → {color}

返回属性值文本颜色，可重载自定义

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description   
`property`&emsp;[hc.Property](hc.Property.html)&emsp;&emsp; 属性对象  
`value`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;值   
`rowIndex`&emsp;Number&emsp;&emsp;&emsp;&emsp;行索引  

##### Returns:

color

#### getLabelFont(property, value, rowIndex) → {String}

返回属性值文本字体，可重载自定义

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description   
`property`&emsp;[hc.Property](hc.Property.html)&emsp;&emsp; 属性对象  
`value`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;值   
`rowIndex`&emsp;Number&emsp;&emsp;&emsp;&emsp;行索引  

##### Returns:

String

#### getLableSelectColor() → {color}

获取文本选中颜色

##### Returns:

color

#### getLogicalPoint(event) → {Object}

传入html事件对象，将事件坐标转换为组件中的逻辑坐标

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description   
`event`&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;&emsp;事件对象   

##### Returns:

Object

See:

*   [lp](hc.widget.PropertyView.html#lp)

#### getPropertyAt(event) → {[hc.Property](hc.Property.html)}

返回event事件所在的行的属性信息

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description   
`event`&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;&emsp;事件对象   

##### Returns:

[hc.Property](hc.Property.html)

#### getPropertyColor(property, rowIndex) → {color}

返回属性名文本颜色，可重载自定义

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description   
`property`&emsp;[hc.Property](hc.Property.html)&emsp;&emsp; 属性对象  
`rowIndex`&emsp;Number&emsp;&emsp;&emsp;&emsp;行索引  

##### Returns:

color

#### getPropertyFont(property, rowIndex) → {color}

返回属性名文本字体，可重载自定义

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description   
`property`&emsp;[hc.Property](hc.Property.html)&emsp;&emsp; 属性对象  
`rowIndex`&emsp;Number&emsp;&emsp;&emsp;&emsp;行索引  


##### Returns:

color

#### getPropertyModel() → {[hc.DataModel](hc.DataModel.html)}

获取propertyModel属性，可增删Property属性对象

##### Returns:

[hc.DataModel](hc.DataModel.html)

#### getPropertyName() → {String}

返回显示在左列的属性名，可重载自定义

##### Returns:

String

#### getRawProperties() → {[hc.List](hc.List.html)}

返回要显示的原始未过滤排序的属性集合，默认返回propertyModel.getRoots()，可重载自定义

##### Returns:

[hc.List](hc.List.html)

#### getRowHeighc() → {Number}

获取行高

##### Returns:

Number

#### getRowIndexAt(event) → {Number}

获取event事件所在的行索引

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description   
`event`&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;&emsp;事件对象   

##### Returns:

Number

#### getRows() → {[hc.List](hc.List.html)}

返回当前显示的所有行信息的集合，集合元素为string类型代表分组名，{data:d,property:p}结构对象代表属性信息

##### Returns:

[hc.List](hc.List.html)

#### getScrollBarColor() → {color}

获取滚动条颜色

##### Returns:

color

#### getScrollBarSize() → {Number}

获取滚动条宽度

##### Returns:

Number

#### getSelectBackground() → {color}

获取行选中背景颜色

##### Returns:

color

#### getSelectionModel() → {[hc.SelectionModel](hc.SelectionModel.html)}

获取选中模型

##### Returns:

[hc.SelectionModel](hc.SelectionModel.html)

See:

*   [sm](hc.widget.PropertyView.html#sm)

#### getSelectRowIndex() → {Number}

获取当前选中行索引

##### Returns:

Number

#### getSortFunc() → {function}

获取排序函数

##### Returns:

function

#### getTranslateY() → {Number}

获取垂直平移值

##### Returns:

Number -

垂直平移值

See:

*   [ty](hc.widget.PropertyView.html#ty)

#### getView() → {htmlDivElement}

获取组件的根层div

##### Returns:

htmlDivElement

#### getVisibleFunc() → {function}

获取可见过滤器函数

##### Returns:

function

#### getWidth() → {Number}

获取布局宽度

##### Returns:

Number

#### invalidate(delay)

无效组件，并调用延时刷新

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms)  

See:

*   [iv](hc.widget.PropertyView.html#iv)

#### invalidateModel()

无效模型，最彻底的刷新方式

See:

*   [ivm](hc.widget.PropertyView.html#ivm)

#### isAutoHideScrollBar() → {Boolean}

是否自动隐藏滚动条

##### Returns:

Boolean

#### isBatchEditable() → {Boolean}

是否启用批量编辑

##### Returns:

Boolean

#### isCategorizable() → {Boolean}

是否分组显示，默认为true，为false则忽略Property的categoryName属性

##### Returns:

Boolean

#### isColumnLineVisible() → {Boolean}

获取列线是否可见，默认为true

##### Returns:

Boolean

#### isDisabled() → {Boolean}

组件是否处于不可用状态，处于此状态时不能进行任何操作并且会遮挡一层蒙板

##### Returns:

Boolean

#### isEditable() → {Boolean}

返回可否编辑的总开关，默认为false，每个Property属性对象可再控制

##### Returns:

Boolean

#### isExpanded(categoryName) → {Boolean}

分组是否展开

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`categoryName`&emsp;&emsp;String&emsp;&emsp;分组名 

##### Returns:

Boolean

#### isPropertyEditable(property) → {Boolean}

判断属性是否可编辑，可重载自定义

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`property`&emsp;&emsp;[hc.Property](hc.Property.html)&emsp;&emsp;属性对象 

##### Returns:

Boolean

#### isRowLineVisible() → {Boolean}

获取行线是否可见，默认为true

##### Returns:

Boolean

#### isSelectionModelShared() → {Boolean}

当前组件是否共享选中模型

##### Returns:

Boolean

#### isVisible(property) → {Boolean}

判断属性是否可见

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`property`&emsp;&emsp;[hc.Property](hc.Property.html)&emsp;&emsp;属性对象 


##### Returns:

Boolean

#### iv(delay)

无效组件，并调用延时刷新，[invalidate](hc.widget.PropertyView.html#invalidate)的缩写

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms)  

See:

*   [invalidate](hc.widget.PropertyView.html#invalidate)

#### ivm()

无效模型，重新构造内部的rows数据，最彻底的刷新方式，[invalidateModel](hc.widget.PropertyView.html#invalidateModel)的缩写

See:

*   [invalidateModel](hc.widget.PropertyView.html#invalidateModel)

#### lp(event) → {Object}

传入html事件对象，将事件坐标转换为组件中的逻辑坐标，[getLogicalPoint](hc.widget.PropertyView.html#getLogicalPoint)的缩写

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`event`&emsp;&emsp;Event&emsp;&emsp;&emsp;&emsp;事件对象  

##### Returns:

Object

See:

*   [getLogicalPoint](hc.widget.PropertyView.html#getLogicalPoint)

#### mp(listener, scope, ahead)

增加自身属性变化事件监听器，[addPropertyChangeListener](hc.widget.PropertyView.html#addPropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [addPropertyChangeListener](hc.widget.PropertyView.html#addPropertyChangeListener)

#### onCollapsed(categoryName)

合并分组时调用，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`categoryName`&emsp;&emsp;String&emsp;&emsp;分组名 

#### onExpanded(categoryName)

展开分组时调用，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`categoryName`&emsp;&emsp;String&emsp;&emsp;分组名 

#### onTranslateEnded()

平移动画结束时回调，可重载做后续处理

#### redraw()

重绘组件中所有行，仅次于invalidateModel的彻底刷新方式

#### removeBottomPainter(painter)

删除底层Painter

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`painter`&emsp;&emsp;&emsp;Object&emsp;&emsp;Painter类 

#### removePropertyChangeListener(listener, scope)

删除自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

#### removeSelection()

删除所有选中的图元

#### removeTopPainter(painter)

删除顶层Painter

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`painter`&emsp;&emsp;&emsp;function&emsp;&emsp;Painter类 

#### removeViewListener(listener, scope)

删除视图事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

#### setAutoHideScrollBar(v)

设置是否自动隐藏滚动条

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setBackground(color)

设置边框和分组行的背景颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color

#### setBatchEditable(v)

设置是否启用批量编辑

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setCategorizable(v)

设置是否分组显示，默认为true，为false则忽略Property的categoryName属性

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean


#### setCollapseIcon(icon)

设置分组合并图标

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`icon`&emsp;&emsp;&emsp; String

#### setColumnLineColor(color)

设置列线颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color


#### setColumnLineVisible(v)

设置列线是否可见

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setColumnPosition(v)

设置列线位置比例，默认值0.5，允许范围为0~1

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Number

#### setDataModel(dataModel)

设置绑定的数据模型

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`dataModel`&emsp;&emsp;&emsp;[hc.DataModel](hc.DataModel.html)&emsp;&emsp;数据模型

#### setDisabled(value, iconUrl)

设置组件是否处于不可用状态，处于不可用状态时不能进行任何操作并且会遮挡一层蒙板

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`value`&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 是否禁用组件  
`iconUrl`&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;蒙板上显示的icon的路径

#### setEditable(editable)

设置可否编辑的总开关，默认为false，每个Property属性对象可再控制

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`editable`&emsp;&emsp;&emsp;Boolean

#### setExpandIcon(icon)

设置分组展开图标

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`icon`&emsp;&emsp;&emsp;String

#### setHeighc(v)

设置布局高度

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;高度值

#### setIndent(v)

设置左侧缩进，左侧空间用于绘制分组toggle图标，以及属性提示icon图标

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Number

#### setLabelColor(color)

设置属性值文本颜色

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`color`&emsp;&emsp;color

#### setLabelFont(font)

设置属性值文本字体

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`font`&emsp;&emsp;String

#### setLabelSelectColor(color)

设置选中文本颜色

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`color`&emsp;&emsp;color

#### setProperties(properties)

以json的方式配置属性(设置)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`properties`&emsp;&emsp;Array&emsp;&emsp;json属性

##### Example

    //示例：
    propertyView.setProperties([{
    	name: 'id',
    	displayName: '序号'
    },
    {
    	name: 'background',
    	accessType: 'style'
    }
    ]);

#### setRowHeighc(v)

设置行高

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Number

#### setRowLineColor(color)

设置行线颜色

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`color`&emsp;&emsp;color

#### setRowLineVisible(v)

设置行线是否可见

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Boolean

#### setScrollBarColor(color)

设置滚动条颜色

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;color&emsp;&emsp;颜色值

#### setScrollBarSize(size)

设置滚动条宽度

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`size`&emsp;&emsp;Number&emsp;&emsp;宽度值

#### setSelectBackground(color)

设置行选中背景颜色

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;color

#### setSelectionModelShared(v)

设置组件是否共享选中模型

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Boolean

#### setSelectRowIndex(v)

设置当前选中行索引

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Number

#### setSortFunc(func)

设置排序函数

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`func`&emsp;&emsp;function

#### setTranslate(x, y, anim)

设置水平和垂直平移值

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;水平平移值  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;垂直平移值  
`anim`&emsp;&emsp;Boolean&emsp;&emsp; \<optional> &emsp;&emsp;是否使用动画

#### setTranslateY(y)

设置垂直平移值

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;垂直平移值  

#### setVisibleFunc(func)

设置可见属性过滤器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function&emsp;&emsp;过滤器函数 

#### setWidth(v)

设置布局宽度

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;宽度值

#### showVBar()

显示垂直滚动条

#### sm() → {[hc.SelectionModel](hc.SelectionModel.html)}

获取选中模型，[getSelectionModel](hc.widget.PropertyView.html#getSelectionModel)的缩写

##### Returns:

[hc.SelectionModel](hc.SelectionModel.html)

See:

*   [getSelectionModel](hc.widget.PropertyView.html#getSelectionModel)

#### toggle(categoryName)

切换分组展开合并状态

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`categoryName`&emsp;&emsp;String&emsp;&emsp;分组名 

#### translate(x, y, anim)

在当前值基础上增加水平和垂直平移值

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;新增的水平平移值(无效)  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;新增的垂直平移值  
`anim`&emsp;&emsp;Boolean&emsp;&emsp; \<optional> &emsp;&emsp;是否使用动画

#### ty(value)

获取或设置垂直平移值，没有参数时相当于[getTranslateY](hc.widget.PropertyView.html#getTranslateY)，有参数时相当于[setTranslateY](hc.widget.PropertyView.html#setTranslateY)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`value`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移值  

#### ump(listener, scope)

删除自身属性变化事件监听器，[removePropertyChangeListener](hc.widget.PropertyView.html#removePropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [removePropertyChangeListener](hc.widget.PropertyView.html#removePropertyChangeListener)

#### validate()

立刻刷新组件
