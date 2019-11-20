
#### new AutoLayout(modelOrView, options)

自动布局类，提供2D的自动布局，即3D的xz面的布局  
自动布局不是银弹，复杂的情况还是需要手工布局，或业务上做必要的妥协，甚至根据业务编写特殊的排布算法才能达到最佳效果。  
使用徐引入 hc-autolayout.js

#### Parameters:
>Name &emsp;&emsp;Type&emsp;Attributes&emsp;Description  
`title`&emsp;&emsp; String&emsp;&emsp;标题文字     
Name

Type

Attributes

Description

`modelOrView`

[hc.graph.GraphView](hc.graph.GraphView.hcml) | [hc.graph3d.Graph3dView](hc.graph3d.Graph3dView.hcml) | [hc.DataModel](hc.DataModel.hcml)

拓扑组件或者数据容器

`options`

Object

<optional>  

选项, 目前选项有：gap布局间距、hgap横向布局间距、vgap纵向布局间距。

### Methods

#### getDuration() → {Number}

获取动画周期毫秒数

##### Returns:

Number

#### getEasing() → {function}

获取动画缓动函数

##### Returns:

function

#### getInterval() → {Number}

获取帧间隔毫秒数

##### Returns:

Number

#### getNodeSize(node)

自动布局时根据getNodeSize(node)函数的返回值，如{width: 100, heighc: 100}结构决定图元大小，可重载自定义

##### Parameters:

Name

Type

Description

`node`

[hc.Data](hc.Data.hcml)

节点

#### getOffsetX() → {Number}

获取布局横偏移

##### Returns:

Number

#### getOffsetY() → {Number}

获取布局纵偏移

##### Returns:

Number

#### getType() → {String}

获取当前布局类型

##### Returns:

String -

circular|symmetric|towardnorth|towardsouth|towardeast|towardwest|hierarchical

#### isAnimate() → {Boolean}

获取是否使用动画

##### Returns:

Boolean

#### layout(type, finishFunc)

##### Parameters:

Name

Type

Attributes

Description

`type`

String

布局类型,可为circular|symmetric|towardnorth|towardsouth|towardeast|towardwest|hierarchical七种自动布局类型

`finishFunc`

function

<optional>  

布局结束的回调函数

#### setAnimate(animate)

设置是否使用动画

##### Parameters:

Name

Type

Description

`animate`

Boolean

是否使用动画

#### setDuration(duration)

设置动画周期毫秒数控制Time-Based的动画效果

##### Parameters:

Name

Type

Description

`duration`

Number

动画周期毫秒数

#### setEasing(easing)

设置缓动函数

##### Parameters:

Name

Type

Description

`easing`

function

缓动函数

#### setInterval(interval)

设置帧间隔毫秒数控制Frame-Based的动画效果

##### Parameters:

Name

Type

Description

`interval`

Number

帧间隔毫秒数

#### setOffsetX(easing)

设置横偏移值

##### Parameters:

Name

Type

Description

`easing`

function

横偏移值

#### setOffsetY(offsetY)

设置纵偏移值

##### Parameters:

Name

Type

Description

`offsetY`

function

纵偏移值

![](./img/logo.png)

NHN Entertainment. Frontend Development Lab

prettyPrint(); var id = 'hc.layout.AutoLayout\_sub'.replace(/"/g, '\_'); var selectedApi = document.getElementById(id); // do not use jquery selector var $selectedApi = $(selectedApi); $selectedApi.removeClass('hidden'); $selectedApi.parent().find('.glyphicon').removeClass('glyphicon-plus').addClass('glyphicon-minus'); showLnbApi();