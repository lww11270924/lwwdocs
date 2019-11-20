
#### new Overview(graphView)

鹰眼组件为hc.graph.GraphView组件提供了全局鸟瞰图的功能，并支持在鹰眼上直接定位、缩放等导航功能。  
使用鹰眼组件需要在引入hc.js核心库之后，再引入一个hc-overview.js的鹰眼插件库。

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`graphView`&emsp;&emsp;&emsp;hc.widget.GraphView&emsp;&emsp;所绑定的hc.graph.GraphView组件对象 

### Methods

#### addPropertyChangeListener(listener, scope, ahead)

增加自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


See:

*   [mp](hc.graph.Overview.html#mp)

#### addToDOM(parentNode)

将组件加入到指定的DOM元素底下，不指定则加入到 document.body 下

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp; Description  
`parentNode`&emsp;&emsp;DOM&emsp;&emsp;DOM元素,默认为 document.body

#### dispose()

销毁组件

#### firePropertyChange(property, oldValue, newValue)

派发属性变化事件

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp; Description  
`property`&emsp;&emsp;&emsp;String&emsp;&emsp;属性名  
`oldValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;旧值  
`newValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;新值

See:

*   [fp](hc.graph.Overview.html#fp)

#### fp(property, oldValue, newValue)

派发属性变化事件

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp; Description  
`property`&emsp;&emsp;&emsp;String&emsp;&emsp;属性名  
`oldValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;旧值  
`newValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;新值

See:

*   [firePropertyChange](hc.graph.Overview.html#firePropertyChange)

#### getCanvas() → {htmlCanvasElement}

获取海创的画布

##### Returns:

htmlCanvasElement - 画布

#### getContentBackground() → {color}

获取内容背景颜色

##### Returns:

color - 背景颜色

#### getContentBorderColor() → {color}

获取内容边框颜色

##### Returns:

color - 边框颜色

#### getFixToRect() → {Rect|false}

获取指定绘制的矩形区域

##### Returns:

Rect | false

#### getGraphView() → {[hc.graph.GraphView](hc.graph.GraphView.html)}

获取显示的海创组件

##### Returns:

[hc.graph.GraphView](hc.graph.GraphView.html) - 海创组件

#### getHeighc() → {Number}

获取组件的布局高度

##### Returns:

Number - 海创组件

#### getMask() → {DOM}

获取显示可见区域的 dom 节点

##### Returns:

DOM - 海创组件

#### getMaskBackground() → {color}

获取显示可见区域的背景颜色

##### Returns:

color - 可见区域的背景颜色

#### getView() → {htmlDivElement}

获取拓扑组件的根层div

##### Returns:

htmlDivElement

#### getWidth() → {Number}

获取组件的布局宽度

##### Returns:

Number

#### invalidate(delay)

无效组件，并调用延时刷新

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms) 

See:

*   [iv](hc.graph.Overview.html#iv)

#### isAutoUpdate() → {Boolean}

获取组件是否跟随拓扑刷新

##### Returns:

Boolean

#### isDisabled() → {Boolean}

获取组件是否禁用

##### Returns:

Boolean

#### iv(delay)

无效组件，并调用延时刷新，[invalidate](hc.graph.Overview.html#invalidate)的缩写

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms) 

See:

*   [invalidate](hc.graph.Overview.html#invalidate)

#### mp(listener, scope, ahead)

增加自身属性变化事件监听器，[addPropertyChangeListener](hc.graph.Overview.html#addPropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


See:

*   [addPropertyChangeListener](hc.graph.Overview.html#addPropertyChangeListener)

#### redraw()

重绘组件

#### removeViewListener(listener, scope)

删除视图事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

#### setAutoUpdate(组件是否跟随拓扑刷新)

设置组件是否跟随海创刷新

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`组件是否跟随海创刷新`&emsp;&emsp;Boolean

#### setContentBackground(contentBackground)

设置内容区域背景颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`contentBackground`&emsp;&emsp;color

#### setContentBorderColor(contentBorderColor)

设置内容区域背景颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`contentBorderColor`&emsp;&emsp;color

#### setDisabled(disabled)

设置是否禁用组件

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`disabled`&emsp;&emsp;Boolean

#### setFixToRect(fixToRect)

设置指定绘制的矩形区域，如果传入true则默认绘制[getContentRect](hc.graph.GraphView.html#getContentRect)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`fixToRect`&emsp;&emsp;Boolean | Rect

#### setGraphView(graphView)

设置显示的拓扑

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`graphView`&emsp;&emsp;[hc.graph.GraphView](hc.graph.GraphView.html)&emsp;&emsp;拓扑组件

#### setHeighc(heighc)

设置布局高度

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`heighc`&emsp;&emsp;Number&emsp;&emsp;高度值

#### setMaskBackground(maskBackground)

设置可见区域背景颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`maskBackground`&emsp;&emsp;Color&emsp;&emsp;&emsp;可见区域背景颜色

#### setWidth(width)

设置布局宽度

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`width`&emsp;&emsp;Number&emsp;&emsp;&emsp;宽度值

#### ump(listener, scope)

删除自身属性变化事件监听器，removePropertyChangeListener的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   removePropertyChangeListener

#### validate()

立刻刷新组件
