[hc](hc.hcml)[.widget](hc.widget.hcml).ContextMenu(items)
---------------------------------------------------------

#### new ContextMenu(items)

右击菜单组件类，可以使任意hcML元素响应右键菜单，支持任意层次子菜单。使用组件需引入hc-contextmenu.js

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Attributes&emsp;&emsp;Description  
`items`&emsp;&emsp;Arrar&emsp;\<optional>&emsp;&emsp;菜单项配置, 为JSON对象


### Methods

#### addTo(container)

指定右击菜单相应的 DOM 节点

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`container`&emsp;&emsp;DOM  

#### addViewListener(listener, scope, ahead)

监听视图事件，如布局、刷新等

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

#### afterHide()

菜单隐藏之后被调用，可以重写此方法

#### afterShow(event)

菜单显示之后被调用，可以重写此方法

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`event`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;如鼠标事件对象  

#### beforeShow(event)

菜单显示之前被调用，可以重写此方法实现动态菜单功能

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`event`&emsp;&emsp;&emsp;Event&emsp;如鼠标事件对象  

#### disableGlobalKey()

禁用全局快捷键

#### dispose()

销毁此右键菜单

#### enableGlobalKey()

启用全局快捷键，一旦启用此选项，菜单不再使用时需要显式调用[dispose](hc.widget.ContextMenu.hcml#dispose)销毁菜单

#### getHeighc() → {Number}

获取布局高度

##### Returns:

Number

#### getItemById(id) → {Object}

根据 id 查找菜单项

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`id`&emsp;&emsp;&emsp;String&emsp;&emsp;要查找的 id  

##### Returns:

Object - 菜单项对象

#### getItemByProperty(property, value) → {Object}

查找属性名为property，值为value的菜单项，只返回第一个查找结果，注意：如果菜单显示时修改此查找结果，则菜单界面在下次显示时更新

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`property`&emsp;&emsp;String&emsp;&emsp;属性名  
`value`&emsp;&emsp;&emsp;Object&emsp;&emsp;菜单项 

##### Returns:

Object -

菜单项对象

#### getRelatedView() → {hcMLDivElement}

获取右击菜单组件响应的 dom

##### Returns:

hcMLDivElement

#### getView() → {hcMLDivElement}

获取组件的根层div

##### Returns:

hcMLDivElement

#### getWidth() → {Number}

获取布局宽度

##### Returns:

Number

#### hide()

隐藏菜单

#### invalidate(delay)

无效组件，并调用延时刷新

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms)  

See:

*   [iv](hc.widget.ContextMenu.hcml#iv)

#### isDisabled() → {Boolean}

组件是否处于不可用状态，处于此状态时不能进行任何操作并且会遮挡一层蒙板

##### Returns:

Boolean

#### isShowing() → {Boolean}

组件是否处于可见状态

##### Returns:

Boolean

#### iv(delay)

无效组件，并调用延时刷新，[invalidate](hc.widget.ContextMenu.hcml#invalidate)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms)  

See:

*   [invalidate](hc.widget.ContextMenu.hcml#invalidate)

#### setDisabled(value, iconUrl)

设置组件是否处于不可用状态，处于不可用状态时不能进行任何操作并且会遮挡一层蒙板

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`value`&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;是否禁用组件  
`iconUrl`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;\<optional> &emsp;蒙板上显示的icon的路径


#### setHeighc(v)

设置布局高度

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;高度值  

#### setItems(items)

设置菜单项，参数为JSON对象

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`items`&emsp;&emsp;&emsp;&emsp;&emsp;Array&emsp;&emsp;菜单项配置数组  

##### Example

    //参数示例：
    [{
         label: '', //菜单文字
         icon: '', //菜单图片ICON
         type: "check" | "radio", //可多选的菜单项 | 单选菜单项
         groupId: 1 //菜单项分组, 当 type 为 radio 有用
         disabled: true //禁用菜单项，可以是函数，由返回值决定是否禁用
         href: "hctp://www.highcopo.com", //超链到某个URL
         linkTarget: "_blank", //超链目标，默认_self
         key: [Key.ctrl, Key.enter], //实际响应的快捷键
         suffix: "Ctrl+Enter", //在菜单上显示的提示文字
         preventDefault: false, //是否阻止快捷键默认的行为，默认为true
         visible: true, //是否可见，可为 boolean，也可以是 function
    }]

#### setItemVisible(id, visible)

设置指定 id 的菜单项是否可见

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`id`&emsp;&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;菜单项id  
`visible`&emsp;&emsp;&emsp;Boolean&emsp;&emsp;是否可见 

#### setLabelMaxWidth(maxWidth)

设置菜单中label的最大宽度，如果label过长会出现跑马灯效果

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`maxWidth`&emsp;&emsp;&emsp;Number&emsp;最大宽度  


#### setVisibleFunc(func)

设置可见过滤器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function&emsp;过滤器函数

#### setWidth(func)

设置布局宽度

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function&emsp;过滤器函数

#### show(x, y, mouseOffset)

显示菜单, x,y为菜单显示页面在中的坐标

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;&emsp;Number | Event&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;x坐标，当仅有一个参数可以传入鼠标事件  
`y`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;y坐标
`mouseOffset`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;\<optional> &emsp;&emsp;是否默认相对传入位置偏移


#### showOnView(view, x, y)

在对应组件上显示菜单

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`view`&emsp;&emsp;&emsp;&emsp;DOM&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;组件，可以是 DOM 或者 hc 组件
`x`&emsp;&emsp;&emsp;&emsp;&emsp;Number | Event&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;x坐标，当仅有二个参数可以传入鼠标事件 
`y`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;y坐标

#### validate()

立刻刷新组件
