<h3>hc.widget.Toolbar(items)</h3>   

---
#### new Toolbar(items)

工具条组件，提供按钮等组件的水平摆放功能

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`items`&emsp;&emsp;&emsp;Array&emsp;&emsp;配置json，详细内容可以参考Toolbar手册 

### Methods

#### addItem(item, index)

在指定index位置插入新元素，index为空代表插入到最后

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`item`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`index`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;\<optional>&emsp;&emsp;监听器函数域

#### addPropertyChangeListener(listener, scope, ahead)

增加自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


See:

*   [mp](hc.widget.Toolbar.html#mp)

#### addToDOM(parentNode)

将组件加入到指定的DOM元素底下，不指定则加入到 document.body 下

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`parentNode`&emsp;&emsp;DOM&emsp;&emsp;DOM元素,默认为 document.body 


#### addViewListener(listener, scope, ahead)

监听视图事件，如布局、刷新等

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

#### disableToolTip()

关闭ToolTip功能

#### drawItem(g, item, x, heighc) → {Number}

绘制元素，并返回该元素所占的宽度值

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`g`&emsp;&emsp;&emsp;&emsp;CanvasRenderingContext2D&emsp;画笔对象
`item`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 元素
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;左上角x坐标
`heighc`&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;绘制的高度

##### Returns:

Number - 宽度值

#### enableToolTip()

启用ToolTip

#### getHeighc() → {Number}

获取布局高度

##### Returns:

Number

#### getItemById(id) → {Object}

获取指定id对应的元素，id值为item元素上的id属性定义

##### Parameters:
>Name&emsp;Type&emsp;&emsp;&emsp;Description  
`id`&emsp;&emsp;Object

##### Returns:

Object

#### getItemGap() → {Number}

获取元素之间的间距

##### Returns:

Number

#### getItems() → {Array}

获取工具条元素数组

##### Returns:

Array

#### getLabelColor(item) → {color}

获取文本颜色，可重载自定义

##### Parameters:
>Name&emsp;Type&emsp;&emsp;&emsp;Description  
`item`&emsp;Object

##### Returns:

color

#### getLabelFont() → {String}

获取文本字体，可重载自定义

##### Returns:

String

#### getLabelSelectColor() → {color}

获取文本选中颜色

##### Returns:

color

#### getLogicalPoint(event) → {Object}

传入html事件对象，将事件坐标转换为组件中的逻辑坐标

##### Parameters:
>Name&emsp;Type&emsp;&emsp;&emsp;Description  
`event`&emsp;Event&emsp;&emsp;事件对象

##### Returns:

Object

See:

*   [lp](hc.widget.Toolbar.html#lp)

#### getSelectBackground() → {color}

获取选中元素的背景色，可重载自定义

##### Returns:

color

#### getSeparatorColor() → {color}

获取分割条颜色

##### Returns:

color

#### getToolTip(e) → {String}

获取ToolTip文字，可重载返回自定义的toolTip文字

##### Parameters:
>Name&emsp;Type&emsp;&emsp;&emsp;Description  
`e`&emsp;&emsp;&emsp;Event&emsp;&emsp;鼠标或Touch事件对象

##### Returns:

String - toolTip文字，默认取出鼠标下的元素，然后返回其toolTip

#### getTranslateX() → {Number}

获取水平平移(滚动)值

##### Returns:

Number

#### getValue(id) → {Object}

根据id获取对应item元素值，比如input的值

##### Parameters:
>Name&emsp;Type&emsp;&emsp;&emsp;Description  
`id`&emsp;&emsp;Object&emsp;&emsp;元素id

##### Returns:

Object

See:

*   [v](hc.widget.Toolbar.html#v)

#### getView() → {htmlDivElement}

获取组件的根层div

##### Returns:

htmlDivElement

#### getWidth() → {Number}

获取布局宽度

##### Returns:

Number

#### invalidate(delay)

无效组件，并调用延时刷新

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`delay`&emsp;&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms)  

See:

*   [iv](hc.widget.Toolbar.html#iv)

#### isDisabled() → {Boolean}

组件是否处于不可用状态，处于此状态时不能进行任何操作并且会遮挡一层蒙板

##### Returns:

Boolean

#### isStickToRighc() → {Boolean}

获取是否向右对齐排布，默认为false

##### Returns:

Boolean

#### iv(delay)

无效组件，并调用延时刷新，[invalidate](hc.widget.Toolbar.html#invalidate)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`delay`&emsp;&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms)

See:

*   [invalidate](hc.widget.Toolbar.html#invalidate)

#### lp(event) → {Object}

传入html事件对象，将事件坐标转换为组件中的逻辑坐标，[getLogicalPoint](hc.widget.Toolbar.html#getLogicalPoint)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`event`&emsp;&emsp;&emsp;Event&emsp;&emsp;事件对象

##### Returns:

Object

See:

*   [getLogicalPoint](hc.widget.Toolbar.html#getLogicalPoint)

#### mp(listener, scope, ahead)

增加自身属性变化事件监听器，[addPropertyChangeListener](hc.widget.Toolbar.html#addPropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`iconURL`&emsp;&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;背景图 URL  
`stopPropagation`&emsp;Boolean&emsp;&emsp;\<optional> &emsp;&emsp;阻止事件冒泡，默认为 true 表示阻止
`ahead`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [addPropertyChangeListener](hc.widget.Toolbar.html#addPropertyChangeListener)

#### redraw()

重绘组件

#### removeItem(item)

删除指定元素

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`item`&emsp;&emsp;&emsp;Object

#### removeItemById(id)

根据id删除指定元素

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`id`&emsp;&emsp;&emsp;Object


#### removePropertyChangeListener(listener, scope)

删除自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

#### removeViewListener(listener, scope)

删除视图事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

#### setDisabled(value, iconUrl)

设置组件是否处于不可用状态，处于不可用状态时不能进行任何操作并且会遮挡一层蒙板

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`value`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;是否禁用组件
`iconURL`&emsp;&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;蒙板上显示的icon的路径


#### setHeighc(heighc)

设置布局高度

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`heighc`&emsp;&emsp;&emsp;Number&emsp;&emsp;高度值  

#### setItemGap(gap)

设置元素之间的间距

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`gap`&emsp;&emsp;&emsp;Number

#### setItems(items)

设置工具条元素数组

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`items`&emsp;&emsp;&emsp;Array

#### setLabelColor(v)

设置文本颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`v`&emsp;&emsp;&emsp;&emsp;color

#### setLabelFont(v)

设置文本字体

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`v`&emsp;&emsp;&emsp;&emsp;String

#### setLabelSelectColor(v)

设置文本选中颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`v`&emsp;&emsp;&emsp;&emsp;color

#### setSelectBackground(v)

设置选中元素的背景色，可重载自定义

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`v`&emsp;&emsp;&emsp;&emsp;color

#### setSeparatorColor(v)

设置分割条颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`v`&emsp;&emsp;&emsp;&emsp;color

#### setStickToRighc(v)

设置是否向右对齐排布，默认为false

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`v`&emsp;&emsp;&emsp;&emsp;Boolean

#### setTranslateX(x)

设置拓扑水平平移(滚动)值

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;水平平移(滚动)值

#### setValue(id, value)

根据id设置对应item元素值，比如input的值

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`id`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;元素id  
`value`&emsp;&emsp;&emsp;Object&emsp;&emsp;值

See:

*   [v](hc.widget.Toolbar.html#v)

#### setWidth(width)

设置布局宽度

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`width`&emsp;&emsp;&emsp;Number&emsp;宽度  

#### tx(value)

获取或设置水平平移(滚动)值，没有参数时相当于[getTranslateX](hc.widget.Toolbar.html#getTranslateX)，有参数时相当于[setTranslateX](hc.widget.Toolbar.html#setTranslateX)

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description 
`value`&emsp;&emsp;&emsp;Number&emsp;平移(滚动)值  

#### ump(listener, scope)

删除自身属性变化事件监听器，[removePropertyChangeListener](hc.widget.Toolbar.html#removePropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [removePropertyChangeListener](hc.widget.Toolbar.html#removePropertyChangeListener)

#### v(id, value) → {Object}

根据id获取或设置对应item元素值，比如input的值；没有参数时相当于[getValue](hc.widget.Toolbar.html#getValue)，有参数时相当于[setValue](hc.widget.Toolbar.html#setValue)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`id`&emsp;&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;监听器函数 
`value`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;值

##### Returns:

Object

#### validate()

立刻刷新组件
