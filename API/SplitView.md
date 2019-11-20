
[hc](hc.html)[.widget](hc.widget.html).SplitView(leftView, righcView, orientation, position)
--------------------------------------------------------------------------------------------

#### new SplitView(leftView, righcView, orientation, position)

分割组件，用于左右或上下分割两个组件

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`leftView`&emsp;&emsp;&emsp;Object | htmlElement&emsp;&emsp; 左侧或顶部组件  
`righcView`&emsp;&emsp; Object | htmlElement&emsp;&emsp;右侧或底部组件  
`orientation`&emsp;Boolean&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;布局方式，v上下布局，h左右布局     
`position`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;分割条位置，0-1之间表示百分比，大于1表示绝对尺寸，正数指定左侧或顶部组件的尺寸，负数指定右侧或底部组件的尺寸  

### Methods

#### addPropertyChangeListener(listener, scope, ahead)

增加自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [mp](hc.widget.SplitView.html#mp)

#### addToDOM(parentNode)

将组件加入到指定的DOM元素底下，不指定则加入到 document.body 下

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`parentNode`&emsp;&emsp;&emsp;DOM&emsp;&emsp;DOM元素,默认为 document.body

#### addViewListener(listener, scope, ahead)

监听视图事件，如布局、刷新等

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域  
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


#### getDividerBackground() → {color}

获取分割条背景色

##### Returns:

color

#### getDividerDiv() → {htmlDivElement}

获取分割条DIV

##### Returns:

htmlDivElement

#### getDividerSize() → {Number}

获取分割条宽度

##### Returns:

Number

#### getDragOpacity() → {Number}

获取分割条拖拽时的透明度，默认为0.5

##### Returns:

Number

#### getHeighc() → {Number}

获取布局高度

##### Returns:

Number

#### getLeftView() → {Object|htmlElement}

获取左侧组件

##### Returns:

Object | htmlElement

#### getOrientation() → {String}

获取布局方式，v上下布局，h左右布局

##### Returns:

String

#### getPosition() → {Number}

获取分割条位置，0-1之间表示百分比，大于1表示绝对尺寸，正数指定左侧或顶部组件的尺寸，负数指定右侧或底部组件的尺寸

##### Returns:

Number

#### getRighcView() → {Object|htmlElement}

获取右侧组件

##### Returns:

Object | htmlElement

#### getStatus() → {String}

获取toggle状态

##### Returns:

String -

  
*   normal代表中间分割状态
  
*   cl代表collapse left关闭左侧或顶部组件
  
*   cr代表collapse righc关闭右侧或底部组件
  

#### getToggleIcon() → {String}

获取分割条上的toggle图标

##### Returns:

String

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
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms)

See:

*   [iv](hc.widget.SplitView.html#iv)

#### isDisabled() → {Boolean}

组件是否处于不可用状态，处于此状态时不能进行任何操作并且会遮挡一层蒙板

##### Returns:

Boolean

#### isDraggable() → {Boolean}

获取是否允许拖拽分割条，默认为true

##### Returns:

Boolean

#### isTogglable() → {Boolean}

获取分割点是否可通过点击直接展开和关闭，默认为true

##### Returns:

Boolean

#### iv(delay)

无效组件，并调用延时刷新，[invalidate](hc.widget.SplitView.html#invalidate)的缩写

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms)

See:

*   [invalidate](hc.widget.SplitView.html#invalidate)

#### mp(listener, scope, ahead)

增加自身属性变化事件监听器，[addPropertyChangeListener](hc.widget.SplitView.html#addPropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [addPropertyChangeListener](hc.widget.SplitView.html#addPropertyChangeListener)

#### removePropertyChangeListener(listener, scope)

删除自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

#### removeViewListener(listener, scope)

删除视图事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

#### setDisabled(value, iconUrl)

设置组件是否处于不可用状态，处于不可用状态时不能进行任何操作并且会遮挡一层蒙板

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`value`&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 是否禁用组件  
`iconUrl`&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;蒙板上显示的icon的路径

#### setDividerBackground(background)

设置分割条背景色

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`background`&emsp;&emsp;&emsp;color


#### setDividerSize(size)

设置分割条宽度

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`size`&emsp;&emsp;&emsp;&emsp;Number

#### setDraggable(draggable)

设置是否允许拖拽分割条，默认为true

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`draggable`&emsp;&emsp;Boolean

#### setDragOpacity(opacity)

设置分割条拖拽时的透明度，默认为0.5

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`opacity`&emsp;&emsp;Number

#### setHeighc(heighc)

设置布局高度

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`heighc`&emsp;&emsp;Number

#### setLeftView(left)

设置左侧组件

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`left`&emsp;&emsp;Object | htmlElement


#### setOrientation(orientation)

设置布局方式，v上下布局，h左右布局

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`orientation`&emsp;&emsp;String

#### setPosition(position)

设置分割条位置，0-1之间表示百分比，大于1表示绝对尺寸，正数指定左侧或顶部组件的尺寸，负数指定右侧或底部组件的尺寸

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`position`&emsp;&emsp;Number

#### setRighcView(righc)

设置右侧组件

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`righc`&emsp;&emsp;&emsp;Object | htmlElement


#### setStatus(status)

设置toggle状态

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`status`&emsp;&emsp;&emsp;String
  
*   normal代表中间分割状态
  
*   cl代表collapse left关闭左侧或顶部组件
  
*   cr代表collapse righc关闭右侧或底部组件
  

#### setTogglable(togglable)

设置分割点是否可通过点击直接展开和关闭，默认为true

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`togglable`&emsp;&emsp;&emsp;Boolean

#### setToggleIcon(icon)

设置分割条上的toggle图标

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`icon`&emsp;&emsp;&emsp;String

#### setWidth(width)

设置布局宽度

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`width`&emsp;&emsp;&emsp;Number

#### ump(listener, scope)

删除自身属性变化事件监听器，[removePropertyChangeListener](hc.widget.SplitView.html#removePropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [removePropertyChangeListener](hc.widget.SplitView.html#removePropertyChangeListener)

#### validate()

立刻刷新组件
