
[hc](hc.hcml)[.widget](hc.widget.hcml).BorderPane()
---------------------------------------------------

#### new BorderPane()

边框面板是一种组件布局容器，可在上、下、左、右、中的五个区域位置摆放子组件，  
子组件可为hc框架提供的组件，也可为hcML元素，子组件以position为absolute方式进行绝对定位。

### Methods

#### addPropertyChangeListener(listener, scope, ahead)

增加自身属性变化事件监听器

#### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Attributes&emsp; Description  
`listener`&emsp; function&emsp; &emsp;&emsp;&emsp;&emsp;&emsp; 监听器函数  
`scope`&emsp;&emsp;&emsp;Object&emsp;\<optional>&emsp;监听器函数域  
`ahead`&emsp;&emsp;&emsp;Boolean&emsp;\<optional>&emsp;是否将当前监听器插入到监听器列表开头 

See:

*   [mp](hc.widget.BorderPane.hcml#mp)

#### addToDOM(parentNode)

将组件加入到指定的DOM元素底下，不指定则加入到 document.body 下

#### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;Description  
`parentNode`&emsp;DOM&emsp; DOM元素,默认为 document.body  

#### addViewListener(listener, scope, ahead)

监听视图事件，如布局、刷新等

#### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Attributes&emsp; Description  
`listener`&emsp; function&emsp; &emsp;&emsp;&emsp;&emsp;&emsp; 监听器函数  
`scope`&emsp;&emsp;&emsp;Object&emsp;\<optional>&emsp;监听器函数域  
`ahead`&emsp;&emsp;&emsp;Boolean&emsp;\<optional>&emsp;是否将当前监听器插入到监听器列表开头 

#### getBottomHeighc() → {Number}

获取底部组件高度

##### Returns:

Number

#### getBottomView() → {Object|hcMLElement}

获取底部组件

##### Returns:

Object | hcMLElement

#### getCenterView() → {Object|hcMLElement}

获取中间组件

##### Returns:

Object | hcMLElement

#### getHeighc() → {Number}

获取布局高度

##### Returns:

Number

#### getLeftView() → {Object|hcMLElement}

获取左侧组件

##### Returns:

Object | hcMLElement

#### getLeftWidth() → {Number}

获取左侧组件宽度

##### Returns:

Number

#### getRighcView() → {Object|hcMLElement}

获取右侧组件

##### Returns:

Object | hcMLElement

#### getRighcWidth() → {Number}

获取右侧组件宽度

##### Returns:

Number

#### getTopHeighc() → {Number}

获取顶部组件高度

##### Returns:

Number

#### getTopView() → {Object|hcMLElement}

获取顶部组件

##### Returns:

Object | hcMLElement

#### getView() → {hcMLDivElement}

获取组件的根层div

##### Returns:

hcMLDivElement

#### getWidth() → {Number}

获取布局宽度

##### Returns:

Number

#### invalidate(delay)

无效组件，并调用延时刷新

#### Parameters:
>Name &emsp;Type&emsp;&emsp;&emsp; Description  
`delay`&emsp; Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms)  

延迟刷新的间隔事件(单位:ms)

See:

*   [iv](hc.widget.BorderPane.hcml#iv)

#### isDisabled() → {Boolean}

组件是否处于不可用状态，处于此状态时不能进行任何操作并且会遮挡一层蒙板

##### Returns:

Boolean

#### iv(delay)

无效组件，并调用延时刷新

#### Parameters:
>Name&emsp;Type&emsp;&emsp; Description  
`delay`&emsp; Number&emsp; &emsp;延迟刷新的间隔事件(单位:ms)  

See:

*   [invalidate](hc.widget.BorderPane.hcml#invalidate)

#### mp(listener, scope, ahead)

增加自身属性变化事件监听器，[addPropertyChangeListener](hc.widget.BorderPane.hcml#addPropertyChangeListener)的缩写

#### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Attributes&emsp; Description  
`listener`&emsp; function&emsp; &emsp;&emsp;&emsp;&emsp;&emsp; 监听器函数  
`scope`&emsp;&emsp;&emsp;Object&emsp;\<optional>&emsp;监听器函数域  
`ahead`&emsp;&emsp;&emsp;Boolean&emsp;\<optional>&emsp;是否将当前监听器插入到监听器列表开头 

See:

*   [addPropertyChangeListener](hc.widget.BorderPane.hcml#addPropertyChangeListener)

#### removePropertyChangeListener(listener, scope)

删除自身属性变化事件监听器

#### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Attributes&emsp; Description  
`listener`&emsp; function&emsp; &emsp;&emsp;&emsp;&emsp;&emsp; 监听器函数  
`scope`&emsp;&emsp;&emsp;Object&emsp;\<optional>&emsp;监听器函数域    

#### removeViewListener(listener, scope)

删除视图事件监听器

#### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Attributes&emsp; Description  
`listener`&emsp; function&emsp; &emsp;&emsp;&emsp;&emsp;&emsp; 监听器函数  
`scope`&emsp;&emsp;&emsp;Object&emsp;\<optional>&emsp;监听器函数域  

#### setBottomHeighc(v)

设置底部组件高度

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp; Description  
`v`&emsp;&emsp;&emsp;&emsp;Number 

#### setBottomView(v)

设置底部组件

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; Description  
`v`&emsp;&emsp;&emsp;&emsp;Object | hcMLElement 

#### setCenterView(v)

设置中间组件

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; Description  
`v`&emsp;&emsp;&emsp;&emsp;Object | hcMLElement 

#### setDisabled(value, iconUrl)

设置组件是否处于不可用状态，处于不可用状态时不能进行任何操作并且会遮挡一层蒙板

#### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description  
`value`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;是否禁用组件  
`iconUrl`&emsp;&emsp;&emsp;String&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;蒙板上显示的icon的路径


#### setHeighc(v)

设置布局高度

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Number

#### setLeftView(v)

设置左侧组件

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Object | hcMLElement


#### setleftWidth(v)

设置左侧组件宽度

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Number

#### setRighcView(v)

设置右侧组件

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Object | hcMLElement

#### setRighcWidth(v)

设置右侧组件宽度

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Number

#### setTopHeighc(v)

设置顶部组件高度

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Number

#### setTopView(v)

设置顶部组件

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Object | hcMLElement

#### setWidth(v)

设置布局宽度

#### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Number

#### ump(listener, scope)

删除自身属性变化事件监听器，[removePropertyChangeListener](hc.widget.BorderPane.hcml#removePropertyChangeListener)的缩写

#### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;\<optional>&emsp; 监听器函数域

See:

*   [removePropertyChangeListener](hc.widget.BorderPane.hcml#removePropertyChangeListener)

#### validate()

刷新组件
