
[ht](ht.html)[.widget](ht.widget.html).TableHeader(tableView)
-------------------------------------------------------------

#### new TableHeader(tableView)

表头组件，常与TableView和TreeTableView结合呈现Column信息，并提供Column的排序、大小和位置变化等交互操作功能

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`tableView`&emsp;&emsp;[ht.widget.TableView](ht.widget.TableView.html) | [ht.widget.TreeTableView](ht.widget.TreeTableView.html)&emsp;&emsp;表格组件

### Methods

#### addPropertyChangeListener(listener, scope, ahead)

增加自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [mp](ht.widget.TableHeader.html#mp)

#### addViewListener(listener, scope, ahead)

监听视图事件，如布局、刷新等

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

#### drawColumn(g, column, x, y, width, height)

绘制列头，可重载自定义

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`g`&emsp;&emsp;&emsp;&emsp;&emsp;CanvasRenderingContext2D&emsp;&emsp;画笔对象  
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;数据元素  
`selected`&emsp;Boolean&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;数据元素是否选中  
`column`&emsp;&emsp;[hc.Column](hc.Column.html)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;列信息  
`x`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角x坐标  
`y`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角y坐标  
`width`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的宽度  
`heighc`&emsp;&emsp; Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的高度

#### getCheckIcon() → {String}

返回check图标

##### Returns:

String

#### getColumnLineColor() → {color}

获取列线颜色

##### Returns:

color

#### getHeight() → {Number}

获取布局高度

##### Returns:

Number

#### getIndent() → {Number}

获取缩进，一般当作列头图标的宽度

##### Returns:

Number

#### getInsertColor() → {color}

获取移动列时可插入位置的提示颜色

##### Returns:

color

#### getLabel(column) → {String}

获取列头文字信息，默认返回column.toLabel()，可重载自定义

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`column`&emsp;&emsp;&emsp;[ht.Column](ht.Column.html)

##### Returns:

String

#### getLabelAlign() → {String}

获取列头文字水平对齐方式，默认会考虑column.getAlign()值，可重载自定义

##### Returns:

String

#### getLabelColor(column) → {color}

获取列头文字颜色，默认会返回column.getColor()||tableHeader.getLabelColor();

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`column`&emsp;&emsp;&emsp;[ht.Column](ht.Column.html)&emsp;&emsp;列

##### Returns:

color

#### getLabelFont(column) → {String}

获取列头文字字体，可重载自定义

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`column`&emsp;&emsp;&emsp;[ht.Column](ht.Column.html)&emsp;&emsp;列


##### Returns:

String

#### getLogicalPoint(event) → {Object}

传入htML事件对象，将事件坐标转换为组件中的逻辑坐标

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`event`&emsp;&emsp;&emsp;Event&emsp;&emsp;事件对象

##### Returns:

Object

See:

*   [lp](ht.widget.TableHeader.html#lp)

#### getMoveBackground() → {color}

获取移动列时的列头背景色

##### Returns:

color

#### getSortAscIcon() → {String}

获取表头列升序图标

##### Returns:

String

#### getSortDescIcon() → {String}

获取表头列降序图标

##### Returns:

String

#### getTableView() → {[ht.widget.TableView](ht.widget.TableView.html)|[ht.widget.TreeTableView](ht.widget.TreeTableView.html)}

获取绑定的表格组件

##### Returns:

[ht.widget.TableView](ht.widget.TableView.html) | [ht.widget.TreeTableView](ht.widget.TreeTableView.html)

#### getView() → {htMLDivElement}

获取组件的根层div

##### Returns:

htMLDivElement

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

*   [iv](ht.widget.TableHeader.html#iv)

#### isColumnLineVisible() → {Boolean}

获取列线是否可见，默认为true

##### Returns:

Boolean

#### isDisabled() → {Boolean}

组件是否处于不可用状态，处于此状态时不能进行任何操作并且会遮挡一层蒙板

##### Returns:

Boolean

#### isMovable() → {Boolean}

获取列顺序是否允许移动改变，默认为true

##### Returns:

Boolean

#### isResizable() → {Boolean}

获取列宽是否允许改变，默认为true

##### Returns:

Boolean

#### iv(delay)

无效组件，并调用延时刷新，[invalidate](ht.widget.TableHeader.html#invalidate)的缩写

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms) 

See:

*   [invalidate](ht.widget.TableHeader.html#invalidate)

#### lp(event) → {Object}

传入htML事件对象，将事件坐标转换为组件中的逻辑坐标，[getLogicalPoint](ht.widget.TableHeader.html#getLogicalPoint)的缩写

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`event`&emsp;&emsp;Event&emsp;&emsp;事件对象 

##### Returns:

Object

See:

*   [getLogicalPoint](ht.widget.TableHeader.html#getLogicalPoint)

#### mp(listener, scope, ahead)

增加自身属性变化事件监听器，[addPropertyChangeListener](ht.widget.TableHeader.html#addPropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [addPropertyChangeListener](ht.widget.TableHeader.html#addPropertyChangeListener)

#### removePropertyChangeListener(listener, scope)

删除自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

#### removeViewListener(listener, scope)

删除视图事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

#### setCheckIcon(icon)

设置check图标

##### Parameters:
>Name&emsp;&emsp; Type&emsp;&emsp;Description  
`icon`&emsp;&emsp;&emsp;String

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

#### setDisabled(value, iconUrl)

设置组件是否处于不可用状态，处于不可用状态时不能进行任何操作并且会遮挡一层蒙板

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`value`&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 是否禁用组件  
`iconUrl`&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;蒙板上显示的icon的路径

#### setHeight(v)

设置布局高度

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;高度值


#### setIndent(v)

设置缩进，一般当作列头图标的宽度

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Number

#### setInsertColor(color)

设置移动列时可插入位置的提示颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color


#### setLabelColor(color)

设置列头文本颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color

#### setLabelFont(font)

设置列头文本字体

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`font`&emsp;&emsp;&emsp;String

#### setMovable(movable)

设置列顺序是否允许移动改变，默认为true

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`movable`&emsp;&emsp;&emsp;Boolean

#### setMoveBackground(color) → {color}

设置移动列时的列头背景色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color

##### Returns:

color

#### setResizable(v)

设置列宽是否允许改变，默认为true

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setSortAscIcon(icon)

设置表头列升序图标

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`icon`&emsp;&emsp;&emsp;String


#### setSortDescIcon(icon)

设置表头列降序图标

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`icon`&emsp;&emsp;&emsp;String

#### setWidth(v)

设置布局宽度

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp; Description  
`v`&emsp;&emsp;&emsp;&emsp;Number&emsp;宽度值

#### ump(listener, scope)

删除自身属性变化事件监听器，[removePropertyChangeListener](ht.widget.TableHeader.html#removePropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [removePropertyChangeListener](ht.widget.TableHeader.html#removePropertyChangeListener)

#### validate()

立刻刷新组件
