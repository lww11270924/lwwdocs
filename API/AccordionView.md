
[hc](hc.hcml)[.widget](hc.widget.hcml).AccordionView()
------------------------------------------------------

#### new AccordionView()

折叠组件，用于多组件的折叠展开效果，提供水平和垂直两种布局方式

### Methods

**add**(title, content, expand, icon)

添加组件

##### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`title`&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;组件的标题文字信息，不同组件不得相同     
`content`&emsp;Object | hcMLElement&emsp;&emsp;组件内容，可为hc框架提供的组件对象，也可为原生hcML元素  
`expand`&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;组件是否展开，默认为false  
`icon`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;组件标题中显示的图标     


#### addPropertyChangeListener(listener, scope, ahead)

增加自身属性变化事件监听器

#### Parameters:
>Name &emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp; function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数     
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;\<optional> &emsp; 监听器函数域  
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp; \<optional> &emsp; 是否将当前监听器插入到监听器列表开头


See:

*   [mp](hc.widget.AccordionView.hcml#mp)

#### addToDOM(parentNode)

将组件加入到指定的DOM元素底下，不指定则加入到 document.body 下

#### Parameters:
>Name &emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`parentNode`&emsp;&emsp;DOM&emsp;DOM元素,默认为 document.body    

#### addViewListener(listener, scope, ahead)

监听视图事件，如布局、刷新等

##### Parameters:
>Name &emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp; function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数     
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;\<optional> &emsp; 监听器函数域  
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp; \<optional> &emsp; 是否将当前监听器插入到监听器列表开头

#### clear()

清除所有组件

#### collapse()

合并当前展开的组件

#### expand(title)

根据标题找到组件并展开

#### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`title`&emsp;&emsp; String&emsp;&emsp;标题文字     

#### getCollapseIcon() → {String}

获取合并图标

##### Returns:

String

#### getCurrentTitle() → {String}

获取当前展开组件的标题

##### Returns:

String

#### getExpandIcon() → {String}

获取展开图标

##### Returns:

String

#### getHeighc() → {Number}

获取布局高度

##### Returns:

Number

#### getLabelColor() → {color}

获取标题文字颜色

##### Returns:

color

#### getLabelFont() → {String}

获取标题文字字体

##### Returns:

String

#### getOrientation() → {String}

获取布局方式，默认为vertical或v，可设置为horizontal或h

##### Returns:

String

#### getSelectBackground() → {color}

获取标题选中背景色

##### Returns:

color

#### getSelectWidth() → {Number}

获取标题选中边框宽度

##### Returns:

Number

#### getSeparatorColor() → {color}

获取分割线的颜色

##### Returns:

color

#### getTitleBackground() → {color}

获取标题背景色

##### Returns:

color

#### getTitleHeighc() → {Number}

获取标题高度

##### Returns:

Number

#### getTitles() → {[hc.List](hc.List.hcml)}

获取所有标题

##### Returns:

[hc.List](hc.List.hcml)

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
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`delay`&emsp;&emsp; Number&emsp;延迟刷新的间隔事件(单位:ms)    

延迟刷新的间隔事件(单位:ms)

See:

*   [iv](hc.widget.AccordionView.hcml#iv)

#### isDisabled() → {Boolean}

组件是否处于不可用状态，处于此状态时不能进行任何操作并且会遮挡一层蒙板

##### Returns:

Boolean

#### isExpanded(title) → {Boolean}

判断指定的title是否处于展开状态

##### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`title`&emsp;&emsp; String&emsp;标题文字  

##### Returns:

Boolean

#### iv(delay)

无效组件，并调用延时刷新

##### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`delay`&emsp;&emsp; String&emsp;延迟刷新的间隔事件(单位:ms)  

See:

*   [invalidate](hc.widget.AccordionView.hcml#invalidate)

#### mp(listener, scope, ahead)

增加自身属性变化事件监听器，[addPropertyChangeListener](hc.widget.AccordionView.hcml#addPropertyChangeListener)的缩写

#### Parameters:
>Name &emsp;&emsp;&emsp; Type&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp; 监听器函数  
`scope`&emsp;&emsp;&emsp; Object&emsp;&emsp;\<optional>&emsp;&emsp;&emsp;监听器函数  
`ahead`&emsp;&emsp;&emsp; Boolean&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头 

See:

*   [addPropertyChangeListener](hc.widget.AccordionView.hcml#addPropertyChangeListener)

#### onCollapsed(title)

合并标题时调用，可重载做后续处理

#### Parameters:
>Name &emsp;&emsp;Type&emsp;Description  
`title`&emsp;&emsp;String&emsp; 标题  

#### onExpanded(title)

展开标题时调用，可重载做后续处理

##### Parameters:
>Name &emsp;&emsp;Type&emsp;Description  
`title`&emsp;&emsp;String&emsp; 标题  

#### remove(title)

根据标题找到组件并删除

#### Parameters:
>Name &emsp;&emsp;Type&emsp;Description  
`title`&emsp;&emsp;String&emsp; 标题  

#### removePropertyChangeListener(listener, scope)

删除自身属性变化事件监听器

#### Parameters:
>Name &emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp; &emsp;&emsp;&emsp;&emsp;&emsp;监听器函数   
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;\<optional>&emsp;监听器函数域 

#### removeViewListener(listener, scope)

删除视图事件监听器

#### Parameters:
>Name &emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp; &emsp;&emsp;&emsp;&emsp;&emsp;监听器函数   
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;\<optional>&emsp;监听器函数域  

#### setCollapseIcon(icon)

设置合并图标

#### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`icon`&emsp;&emsp;&emsp;String&emsp;&emsp;图标   

#### setDisabled(value, iconUrl)

设置组件是否处于不可用状态，处于不可用状态时不能进行任何操作并且会遮挡一层蒙板

#### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Attributes&emsp;&emsp;Description  
`value`&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;是否禁用组件   
`iconUrl`&emsp;String&emsp;&emsp;\<optional>&emsp;蒙板上显示的icon的路径    
#### setExpandIcon(icon)

设置展开图标

#### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`icon`&emsp;&emsp;&emsp;String&emsp;&emsp;图标 

#### setHeighc(v)

设置布局高度

#### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;Number&emsp;&emsp;高度值 

#### setLabelColor(color)

设置标题文字颜色

#### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;color&emsp;&emsp;颜色值  


#### setLabelFont(font)

设置标题文字字体

##### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`font`&emsp;&emsp;String&emsp;&emsp;字体  

#### setOrientation(v)

设置布局方式，默认为vertical或v，可设置为horizontal或h

#### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;String&emsp;&emsp;布局方式 

#### setSelectBackground(color)

设置标题选中背景色

#### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;color&emsp;&emsp;颜色值 

#### setSelectWidth(v)

设置标题选中边框宽度

#### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;Number  

#### setSeparatorColor(color)

设置分割线颜色

#### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;color&emsp;&emsp;颜色值 

#### setTitleBackground(color)

设置标题背景色

#### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;color&emsp;&emsp;颜色值 

#### setTitleHeighc(v)

设置标题高度

#### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;Number&emsp;&emsp;高度值 

#### setWidth(v)

设置布局宽度

#### Parameters:
>Name &emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;Number&emsp;&emsp;高度值 

#### ump(listener, scope)

删除自身属性变化事件监听器，[removePropertyChangeListener](hc.widget.AccordionView.hcml#removePropertyChangeListener)的缩写

#### Parameters:
>Name &emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Attributes&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;Object&emsp;&emsp;\<optional> 监听器函数域

See:

*   [removePropertyChangeListener](hc.widget.AccordionView.hcml#removePropertyChangeListener)

#### validate()

刷新组件
