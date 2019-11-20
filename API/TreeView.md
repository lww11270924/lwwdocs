
[hc](hc.html)[.widget](hc.widget.html).TreeView(dataModel)
----------------------------------------------------------

#### new TreeView(dataModel)

树形组件，以树形的方式呈现DataModel中Data数据的父子关系

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`dataModel`&emsp;&emsp;&emsp;[hc.DataModel](hc.DataModel.html)&emsp;&emsp;绑定的数据模型 

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

#### addPropertyChangeListener(listener, scope, ahead)

增加自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


See:

*   [mp](hc.widget.TreeView.html#mp)

#### addToDOM(parentNode)

将组件加入到指定的DOM元素底下，不指定则加入到 document.body 下

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`parentNode`&emsp;DOM&emsp;&emsp;DOM元素,默认为 document.body 


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
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


#### collapse(data)

合并data对象

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素 

#### collapseAll()

合并所有对象

#### disableToolTip()

关闭ToolTip功能

#### dm(dataModel) → {[hc.DataModel](hc.DataModel.html)}

获取或设置数据模型，没有参数时相当于[getDataModel](hc.widget.TreeView.html#getDataModel)，有参数时相当于[setDataModel](hc.widget.TreeView.html#setDataModel)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`dataModel`&emsp;&emsp;[hc.DataModel](hc.DataModel.html)&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;数据模型

##### Returns:

[hc.DataModel](hc.DataModel.html) -

dataModel

#### drawIcon(g, data, x, y, width, heighc)

绘制图标，可重载自定义

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`g`&emsp;&emsp;&emsp;&emsp;CanvasRenderingContext2D&emsp;画笔对象
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;数据元素
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角x坐标
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角y坐标
`width`&emsp;&emsp; Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的宽度
`heighc`&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的高度

#### drawLabel(g, data, x, y, heighc)

绘制文本，可重载自定义，label一般绘制在最后因此没有width参数限制

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`g`&emsp;&emsp;&emsp;&emsp;CanvasRenderingContext2D&emsp;画笔对象
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;数据元素
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角x坐标
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角y坐标
`heighc`&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的高度

#### drawRow(g, data, selected, x, y, width, heighc) → {htmlElement}

绘制行内容，可重载自定义，默认调用drawIcon和drawLabel，如果返回值为html元素，则使用html元素当作Renderer

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`g`&emsp;&emsp;&emsp;&emsp;CanvasRenderingContext2D&emsp;画笔对象
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;数据元素
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角x坐标
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角y坐标
`width`&emsp;&emsp; Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的宽度
`heighc`&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的高度

##### Returns:

htmlElement

#### drawRowBackground(g, data, selected, x, y, width, heighc)

绘制行背景色，默认仅在选中该行时填充选中背景色，可重载自定义

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`g`&emsp;&emsp;&emsp;&emsp;CanvasRenderingContext2D&emsp;画笔对象
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;数据元素
`selected`&emsp;Boolean&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;数据元素是否选中
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角x坐标
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角y坐标
`width`&emsp;&emsp; Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的宽度
`heighc`&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的高度

#### enableToolTip()

启用ToolTip

#### expand(data)

展开data对象

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素

#### expandAll()

展开所有对象

#### getBodyColor(data) → {color}

获取数据元素icon的背景色，可重载自定义

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素

##### Returns:

color -

颜色值，默认返回data.s('body.color')

#### getBorderColor(data) → {color}

获取数据元素icon的边框色，可重载自定义

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素

##### Returns:

color -

颜色值，默认返回data.s('border.color')

#### getCheckIcon(data) → {String}

返回数据元素对应的check图标，可重载自定义check图标，该函数在checkMode模式下有效

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素

##### Returns:

String

#### getCheckMode() → {String}

获取check模式

  
*   null：默认值，不启用check选择模式
  
*   default：check模式的默认选择方式，即单击选中或取消选中，只影响当前点击中的data对象
  
*   children：该check模式将同时影响点击中的data对象，以及其孩子对象
  
*   descendant：该check模式将同时影响点击中的data对象，以及其所有子孙对象
  
*   all：该check模式将同时影响点击中的data对象，以及其所有父辈和子孙对象
  

##### Returns:

String

#### getCollapseIcon() → {String}

获取toggle的关闭图标

##### Returns:

String

#### getDataAt(pointOrEvent) → {[hc.Data](hc.Data.html)}

传入逻辑坐标点或者交互event事件参数，返回当前点下的数据元素

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`pointOrEvent`&emsp;&emsp;&emsp;Object | Event&emsp;&emsp;逻辑坐标点或交互事件对象(如鼠标事件对象) 

##### Returns:

[hc.Data](hc.Data.html) - 点下的数据元素

#### getDataModel() → {[hc.DataModel](hc.DataModel.html)}

获取绑定的数据模型

##### Returns:

[hc.DataModel](hc.DataModel.html) - 数据模型

#### getEndRowIndex() → {Number}

获取当前可见区域的结束行索引

##### Returns:

Number

#### getExpandIcon() → {String}

获取toggle的展开图标

##### Returns:

String

#### getFocusData() → {[hc.Data](hc.Data.html)}

在checkMode模式下数据除了被选中有check状态外，还可以有被点击行的focus状态  
  
此方法获取focus数据元素

##### Returns:

[hc.Data](hc.Data.html)

#### getHeighc() → {Number}

获取布局高度

##### Returns:

Number

#### getIcon(data) → {String}

获取data对象对应的icon图标，可重载自定义

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素

##### Returns:

String

#### getIconWidth(data) → {Number}

返回data对象对应的图标宽度，默认如果有图标则以indent值为宽度，可重载自定义

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素


##### Returns:

Number

#### getIndent(data) → {Number}

获取indent缩进，该值一般当作图标的宽度

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素


##### Returns:

Number

#### getLabel(data) → {String}

获取data对象显示的文字，默认返回data.toLabel()，可重载自定义

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素


##### Returns:

String

#### getLabelColor(data) → {color}

获取data对象的文本颜色，可重载自定义

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素


##### Returns:

color

#### getLabelFont(data) → {String}

获取data对象的文本字体，可重载自定义

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素


##### Returns:

String

#### getLabelSelectColor() → {color}

获取选中文本的颜色

##### Returns:

color

#### getLevel(data) → {Number}

获取当前data的缩减层次，一般结合indent参数用于绘制

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素

##### Returns:

Number

#### getLoader() → {Object}

获取延迟加载器

##### Returns:

Object

#### getLogicalPoint(event) → {Object}

传入html事件对象，将事件坐标转换为组件中的逻辑坐标

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`event`&emsp;&emsp;&emsp;Event&emsp;&emsp;事件对象

##### Returns:

Object

See:

*   [lp](hc.widget.TreeView.html#lp)

#### getRootData() → {[hc.Data](hc.Data.html)}

获取根节点，默认为空，从DataModel#getRoots()的对象开始展示

##### Returns:

[hc.Data](hc.Data.html)

#### getRowDatas() → {[hc.List](hc.List.html)}

获取当前显示的Data对象集合，该集合已被排序和过滤

##### Returns:

[hc.List](hc.List.html)

#### getRowHeighc() → {Number}

获取行高

##### Returns:

Number

#### getRowIndex(data) → {Number}

获取data对象所在的行索引

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素


##### Returns:

Number

#### getRowLineColor() → {color}

获取行线颜色

##### Returns:

color

#### getRowSize() → {Number}

返回当前可见行总行数

##### Returns:

Number

#### getScrollBarColor() → {color}

获取滚动条颜色

##### Returns:

color

#### getScrollBarSize() → {Number}

获取滚动条宽度

##### Returns:

Number

#### getSelectableFunc() → {function}

获取选择过滤器函数

##### Returns:

function

#### getSelectBackground() → {color}

获取行选中背景颜色

##### Returns:

color

#### getSelectionModel() → {[hc.SelectionModel](hc.SelectionModel.html)}

获取选中模型

##### Returns:

[hc.SelectionModel](hc.SelectionModel.html)

See:

*   [sm](hc.widget.TreeView.html#sm)

#### getSortFunc() → {function}

获取排序函数

##### Returns:

function

#### getStartRowIndex() → {Number}

获取当前可见区域的起始行索引

##### Returns:

Number

#### getToggleIcon(data) → {String}

返回当前data对象对应的展开或合并图标，可重载自定义

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素

##### Returns:

String

#### getToolTip(e) → {String}

获取ToolTip文字，可重载返回自定义的toolTip文字

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`e`&emsp;&emsp;&emsp;Event&emsp;&emsp;鼠标或Touch事件对象

##### Returns:

String - toolTip文字，默认取出鼠标下的图元，然后返回其getToolTip()

#### getTranslateY() → {Number}

获取垂直平移值

##### Returns:

Number - 垂直平移值

See:

*   [ty](hc.widget.TreeView.html#ty)

#### getView() → {htmlDivElement}

获取组件的根层div

##### Returns:

htmlDivElement

#### getViewRect() → {Object}

获取组件中可见区域的逻辑尺寸

##### Returns:

Object

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

*   [iv](hc.widget.TreeView.html#iv)

#### invalidateData(data)

无效数据元素

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;要无效的数据元素  

#### invalidateModel()

无效模型，最彻底的刷新方式

See:

*   [ivm](hc.widget.TreeView.html#ivm)

#### isAutoHideScrollBar() → {Boolean}

是否自动隐藏滚动条

##### Returns:

Boolean

#### isAutoMakeVisible() → {Boolean}

选中数据元素时，是否自动平移组件以确保该元素出现在可见区域内

##### Returns:

Boolean

#### isCheckMode() → {Boolean}

是否是check模式

##### Returns:

Boolean

#### isChildrenSortable(parent) → {Boolean}

判断是否允许对parent对象的孩子排序，默认返回true，可重载屏蔽孩子排序

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`parent`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;父元素  

##### Returns:

Boolean

#### isDisabled() → {Boolean}

组件是否处于不可用状态，处于此状态时不能进行任何操作并且会遮挡一层蒙板

##### Returns:

Boolean

#### isExpanded(data) → {Boolean}

判断data对象是否展开

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素  


##### Returns:

Boolean

#### isRootVisible() → {Boolean}

判断rootData节点是否可见

##### Returns:

Boolean

#### isRowLineVisible() → {Boolean}

获取行线是否可见，默认为true

##### Returns:

Boolean

#### isSelectable(data) → {Boolean}

判断data对象是否可被选中

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素  

##### Returns:

Boolean

#### isSelected(data) → {Boolean}

判断data对象是否被选中

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元  


##### Returns:

Boolean

#### isSelectedById(id) → {Boolean}

根据id判断data对象是否被选中

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`id`&emsp;&emsp;&emsp;String | Number&emsp;&emsp;数据元素id  


##### Returns:

Boolean

#### isSelectionModelShared() → {Boolean}

当前组件是否共享选中模型

##### Returns:

Boolean

#### isVisible(data) → {Boolean}

判断数据元素是否可见

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素  


##### Returns:

Boolean

#### iv(delay)

无效组件，并调用延时刷新，[invalidate](hc.widget.TreeView.html#invalidate)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`delay`&emsp;&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms)  

See:

*   [invalidate](hc.widget.TreeView.html#invalidate)

#### ivm()

无效模型，重新构造内部的rows数据，最彻底的刷新方式，[invalidateModel](hc.widget.TreeView.html#invalidateModel)的缩写

See:

*   [invalidateModel](hc.widget.TreeView.html#invalidateModel)

#### lp(event) → {Object}

传入html事件对象，将事件坐标转换为组件中的逻辑坐标，[getLogicalPoint](hc.widget.TreeView.html#getLogicalPoint)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`event`&emsp;&emsp;&emsp;event&emsp;&emsp;事件对象  

##### Returns:

Object

See:

*   [getLogicalPoint](hc.widget.TreeView.html#getLogicalPoint)

#### makeVisible(data)

平移组件以确保数据元素在可见区域内

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素  


#### mp(listener, scope, ahead)

增加自身属性变化事件监听器，[addPropertyChangeListener](hc.widget.TreeView.html#addPropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


See:

*   [addPropertyChangeListener](hc.widget.TreeView.html#addPropertyChangeListener)

#### onCollapsed(data)

合并data对象时调用，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素  

#### onDataClicked(data, e)

数据元素被点击时回调，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;双击的数据元素  
`e`&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;事件对象 

#### onDataDoubleClicked(data, e)

数据元素被双击时回调，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;双击的数据元素  
`e`&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;事件对象 

#### onExpanded(data)

展开data对象时调用，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素 

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
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

#### removeSelection()

删除所有选中的图元

#### removeTopPainter(painter)

删除顶层Painter

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`painter`&emsp;&emsp;&emsp;Object&emsp;&emsp;Painter类 

#### removeViewListener(listener, scope)

删除视图事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域


#### scrollToIndex(index)

平移(滚动)组件至指定的行号

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`index`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp; 行号

#### selectAll()

选中所有数据元素

#### setAutoHideScrollBar(v)

设置是否自动隐藏滚动条

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Boolean


#### setAutoMakeVisible(v)

设置当选中数据元素，是否自动平移(滚动)组件以确保该数据元素出现在可见区域内

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Boolean

#### setCheckMode(v)

设置check模式

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;String

  
*   null：默认值，不启用check选择模式
  
*   default：check模式的默认选择方式，即单击选中或取消选中，只影响当前点击中的data对象
  
*   children：该check模式将同时影响点击中的data对象，以及其孩子对象
  
*   descendant：该check模式将同时影响点击中的data对象，以及其所有子孙对象
  
*   all：该check模式将同时影响点击中的data对象，以及其所有父辈和子孙对象
  

#### setCollapseIcon(v)

设置toggle的关闭图标

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;String

#### setDataModel(dataModel)

设置绑定的数据模型

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`dataModel`&emsp;[hc.DataModel](hc.DataModel.html)&emsp;数据模型 

#### setDisabled(value, iconUrl)

设置组件是否处于不可用状态，处于不可用状态时不能进行任何操作并且会遮挡一层蒙板

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`value`&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;是否禁用组件 
`iconUrl`&emsp;&emsp;String&emsp;&emsp;\<optional>&emsp;&emsp;蒙板上显示的icon的路径

#### setExpandIcon(v)

设置toggle的展开图标

##### Parameters:
>Name&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;String&emsp;&emsp;icon

#### setFocusData(data)

在checkMode模式下数据除了被选中有check状态外，还可以有被点击行的focus状态  
  
此方法设置focus的数据元素

##### Parameters:
>Name&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素

#### setFocusDataById(id)

在checkMode模式下数据除了被选中有check状态外，还可以有被点击行的focus状态  
  
此方法设置focus的数据元素

##### Parameters:
>Name&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;String | Number&emsp;&emsp;数据元素的id

#### setHeighc(v)

设置布局高度

##### Parameters:
>Name&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;Number&emsp;&emsp;高度值

#### setIndent(v)

设置indent缩进，该值一般当作图标的宽度

##### Parameters:
>Name&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;Number

#### setLabelColor(v)

设置行label文字颜色

##### Parameters:
>Name&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;color

#### setLabelFont(v)

设置行label文字字体

##### Parameters:
>Name&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;String

#### setLabelSelectColor(v)

设置行label文字选中颜色

##### Parameters:
>Name&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;color

#### setLoader(v)

设置延迟加载器

##### Parameters:
>Name&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;Object

##### Example

    //示例：
    treeView.setLoader({
    	load: function(data) {
    		//展开此data时回调，可用于加载子节点
    	},
    	isLoaded: function(data) {
    		//返回此data的子结点是否已加载
    	}
    });

#### setRootData(v)

指定根节点，默认为空，从DataModel#getRoots()的对象开始展示

##### Parameters:
>Name&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;[hc.Data](hc.Data.html)

#### setRootVisible(v)

设置根节点是否可见

##### Parameters:
>Name&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;Boolean


#### setRowHeighc(v)

设置行高

##### Parameters:
>Name&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;Number


#### setRowLineColor(color)

设置行线颜色

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;color

#### setRowLineVisible(v)

设置行线是否可见

##### Parameters:
>Name&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;Boolean


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

#### setSelectableFunc(func)

设置选择过滤器函数

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`func`&emsp;&emsp;function&emsp;&emsp;过滤器函数


#### setSelectBackground(color)

设置行选中背景颜色

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;color

#### setSelectionModelShared(v)

设置组件是否共享选中模型

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;Boolean

#### setSortFunc(func)

设置排序函数

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`func`&emsp;&emsp;function

#### setTranslate(x, y, anim)

设置垂直平移值(水平平移值无效)

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;水平平移值，此参数无效 
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;垂直平移值 
`anim`&emsp;&emsp;&emsp;Boolean&emsp;&emsp;是否使用动画 

#### setTranslateY(v)

设置垂直平移值

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;Number&emsp;垂直平移值 

#### setVisibleFunc(func)

设置可见过滤器

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`func`&emsp;&emsp;function&emsp;过滤器函数 

#### setWidth(v)

设置布局宽度

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;Number&emsp;&emsp;宽度值 


#### showVBar()

显示垂直滚动条

#### sm() → {[hc.SelectionModel](hc.SelectionModel.html)}

获取选中模型，[getSelectionModel](hc.widget.TreeView.html#getSelectionModel)的缩写

##### Returns:

[hc.SelectionModel](hc.SelectionModel.html)

See:

*   [getSelectionModel](hc.widget.TreeView.html#getSelectionModel)

#### toggle(data)

展开或合并data对象

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素 

#### translate(x, y, anim)

在当前值基础上增加垂直平移值(水平无效)

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 新增的水平平移值，此参数无效  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听新增的垂直平移值器函数域
`anim`&emsp;&emsp;&emsp;Boolean&emsp;&emsp;\<optional> &emsp;是否使用动画

#### ty(value)

获取或设置垂直平移值，没有参数时相当于[getTranslateY](hc.widget.TreeView.html#getTranslateY)，有参数时相当于[setTranslateY](hc.widget.TreeView.html#setTranslateY)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`value`&emsp;&emsp;&emsp;Number&emsp;&emsp;平移值 

#### ump(listener, scope)

删除自身属性变化事件监听器，[removePropertyChangeListener](hc.widget.TreeView.html#removePropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [removePropertyChangeListener](hc.widget.TreeView.html#removePropertyChangeListener)

#### validate()

立刻刷新组件

