<h3>hc.widget.TabView()</h3>   

---
#### new TabView()

页签组件，以页签的方式呈现多组件，页签支持拖拽和关闭等功能

### Methods

#### addPropertyChangeListener(listener, scope, ahead)

增加自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [mp](hc.widget.TabView.html#mp)

#### addToDOM(parentNode)

将组件加入到指定的DOM元素底下，不指定则加入到 document.body 下

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`parentNode`&emsp;DOM&emsp;&emsp;DOM元素,默认为 document.body 

#### addViewListener(listener, scope, ahead)

监听视图事件，如布局、刷新等

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


#### get(nameOrIndex)

获取指定的Tab对象，参数可为Tab的标签文字或索引

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`nameOrIndex`&emsp;&emsp;&emsp;String | Number&emsp;&emsp;标签文字或索引 

#### getContentDiv() → {htmlDivElement}

获取组件的内容区域Div

##### Returns:

htmlDivElement

#### getCurrentTab() → {[hc.Tab](hc.Tab.html)}

获取当前选中的Tab对象

##### Returns:

[hc.Tab](hc.Tab.html)

#### getHeighc() → {Number}

获取布局高度

##### Returns:

Number

#### getInsertColor() → {color}

获取提示插入位置颜色

##### Returns:

color

#### getLabel(tab) → {String}

获取tab对象显示的文字，默认返回tab.toLabel()，可重载自定义

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`tab`&emsp;&emsp;&emsp;[hc.Tab](hc.Tab.html)

##### Returns:

String

#### getLabelColor() → {color}

获取页签文字颜色，可重载自定义

##### Returns:

color

#### getLabelFont() → {String}

获取页签文字字体，可重载自定义

##### Returns:

String

#### getLogicalPoint(event) → {Object}

传入html事件对象，将事件坐标转换为组件中的逻辑坐标

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`event`&emsp;&emsp;Event&emsp;&emsp;&emsp;事件对象

##### Returns:

Object

See:

*   [lp](hc.widget.TabView.html#lp)

#### getMoveBackground() → {color}

获取移动时的页签背景色

##### Returns:

color

#### getSelectBackground() → {color}

获取页签选中线条背景色

##### Returns:

color

#### getSelectWidth() → {Number}

获取页签选中的线条宽度，默认值为3

##### Returns:

Number

#### getTabBackground() → {color}

获取页签背景色

##### Returns:

color

#### getTabGap() → {Number}

获取页签间隔，默认值为1

##### Returns:

Number

#### getTabHeighc() → {Number}

获取页签高度

##### Returns:

Number

#### getTabModel() → {[hc.DataModel](hc.DataModel.html)}

获取页签模型容器，用于增删Tab页签

##### Returns:

[hc.DataModel](hc.DataModel.html)

#### getTabPosition() → {String}

获取页签位置，可用值有：top|bottom|left|righc|left-vertical|righc-vertical，默认值为top

##### Returns:

String

#### getTabWidth(tab) → {Number}

获取页签宽度，可重载自定义

##### Parameters:
>Name&emsp;Type&emsp;&emsp;&emsp;Description  
`tab`&emsp;&emsp;[hc.Tab](hc.Tab.html)&emsp;&emsp;&emsp;页签

##### Returns:

Number

#### getTitleDiv() → {htmlDivElement}

获取页签的div容器

##### Returns:

htmlDivElement

#### getTranslateX() → {Number}

获取水平平移(滚动)值

##### Returns:

Number

#### getTranslateY() → {Number}

获取垂直平移(滚动)值

##### Returns:

Number

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
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms)  

See:

*   [iv](hc.widget.TabView.html#iv)

#### isDisabled() → {Boolean}

组件是否处于不可用状态，处于此状态时不能进行任何操作并且会遮挡一层蒙板

##### Returns:

Boolean

#### isMovable() → {Boolean}

获取页签是否可拖拽移动改变显示顺序，默认值为true

##### Returns:

Boolean

#### iv(delay)

无效组件，并调用延时刷新，[invalidate](hc.widget.TabView.html#invalidate)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms)  

See:

*   [invalidate](hc.widget.TabView.html#invalidate)

#### lp(event) → {Object}

传入html事件对象，将事件坐标转换为组件中的逻辑坐标，[getLogicalPoint](hc.widget.TabView.html#getLogicalPoint)的缩写

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`event`&emsp;&emsp;Event&emsp;&emsp;事件对象  

##### Returns:

Object

See:

*   [getLogicalPoint](hc.widget.TabView.html#getLogicalPoint)

#### mp(listener, scope, ahead)

增加自身属性变化事件监听器，[addPropertyChangeListener](hc.widget.TabView.html#addPropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [addPropertyChangeListener](hc.widget.TabView.html#addPropertyChangeListener)

#### onTabChanged(oldTab, newTab)

当前选中Tab对象变化时回调，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`oldTab`&emsp;&emsp;&emsp;[hc.Tab](hc.Tab.html)&emsp;&emsp;旧页签  
`newTab`&emsp;&emsp;&emsp;[hc.Tab](hc.Tab.html)&emsp;&emsp;新选中的页签 

#### onTabClosed(tab, index)

关闭Tab页签回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`tab`&emsp;&emsp;&emsp;&emsp;[hc.Tab](hc.Tab.html)&emsp;&emsp;被关闭的页签  
`index`&emsp;&emsp;&emsp;Number&emsp;&emsp;索引 

#### remove(tab)

删除指定的Tab

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`tab`&emsp;&emsp;&emsp;&emsp;[hc.Tab](hc.Tab.html) | Number | String&emsp;&emsp;Tab对象，或整数类型的索引，或页签文字  


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

#### select(tab)

选中指定的Tab

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`tab`&emsp;&emsp;&emsp;&emsp;[hc.Tab](hc.Tab.html) | Number | String&emsp;&emsp;Tab对象，或整数类型的索引，或页签文字  

#### setDisabled(value, iconUrl)

设置组件是否处于不可用状态，处于不可用状态时不能进行任何操作并且会遮挡一层蒙板

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`value`&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;是否禁用组件  
`iconUrl`&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;蒙板上显示的icon的路径


#### setHeighc(heighc)

设置布局高度

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`heighc`&emsp;&emsp;&emsp;Number&emsp;&emsp;高度值 

#### setInsertColor(color)

设置提示插入位置颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color


#### setLabelColor(color)

设置页签文字颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color

#### setLabelFont(font)

设置页签文字字体

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`font`&emsp;&emsp;&emsp;String

#### setMovable(v)

设置页签是否可拖拽移动改变显示顺序，默认值为true

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Boolean

#### setMoveBackground(color)

设置移动时的页签背景色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color

#### setSelectBackground(color)

设置页签选中线条背景色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color

#### setSelectWidth(width)

设置页签选中的线条宽度，默认值为3

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`width`&emsp;&emsp;&emsp;Number

#### setTabBackground(color)

设置页签背景色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color

#### setTabGap(v)

设置页签间隔，默认值为1

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Number

#### setTabHeighc(v)

设置页签高度

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Number


#### setTabPosition(v)

设置页签位置，可用值有：top|bottom|left|righc|left-vertical|righc-vertical，默认值为top

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;String


#### setTranslateX(x)

设置组件水平平移(滚动)值

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp; 水平平移(滚动)值

#### setTranslateY(y)

设置组件垂直平移(滚动)值

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp; 垂直平移(滚动)值

#### setWidth(width)

设置布局宽度

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`width`&emsp;&emsp;Number

#### tx(value)

获取或设置水平平移(滚动)值，没有参数时相当于[getTranslateX](hc.widget.TabView.html#getTranslateX)，有参数时相当于[setTranslateX](hc.widget.TabView.html#setTranslateX)

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`value`&emsp;&emsp;Number&emsp; 平移(滚动)值


#### ty(value)

获取或设置垂直平移(滚动)值，没有参数时相当于[getTranslateY](hc.widget.TabView.html#getTranslateY)，有参数时相当于[setTranslateY](hc.widget.TabView.html#setTranslateY)

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`value`&emsp;&emsp;Number&emsp; 平移(滚动)值

#### ump(listener, scope)

删除自身属性变化事件监听器，[removePropertyChangeListener](hc.widget.TabView.html#removePropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [removePropertyChangeListener](hc.widget.TabView.html#removePropertyChangeListener)

#### validate()

立刻刷新组件
