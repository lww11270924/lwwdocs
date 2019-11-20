
#### new Graph3dView(dataModel)

3D渲染引擎组件，可视化呈现数据模型的三维环境场景

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`dataModel`&emsp;&emsp;[hc.DataModel](hc.DataModel.html)&emsp;&emsp;绑定的数据模型

### Methods

#### addInteractorListener(listener, scope, ahead)

增加交互事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


See:

*   [mi](hc.graph3d.Graph3dView.html#mi)

##### Example

    //示例：
    graph3dView.addInteractorListener(function(event) {
    		//event格式：
    		{
    			kind: 'clickData',//事件类型
    			data: data,//事件相关的数据元素
    			part: "part",//事件的区域,icon、label等
    			event: e//html原生事件
    		}
    });

#### addPropertyChangeListener(listener, scope, ahead)

增加自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


See:

*   [mp](hc.graph3d.Graph3dView.html#mp)

#### addToDOM(parentNode)

将组件加入到指定的DOM元素底下，不指定则加入到 document.body 下

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`parentNode`&emsp;&emsp;DOM&emsp;&emsp;&emsp;DOM元素,默认为 document.body

#### addViewListener(listener, scope, ahead)

监听视图事件，如布局、刷新等

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


#### deserialize(jsonUrl, callback)

根据 json 路径请求并反序列场景

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`jsonUrl`&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;场景 json 路径  
`callback`&emsp;&emsp;&emsp;function&emsp;&emsp;回调函数

##### Example

    //示例:
    g3d.deserialize('previews/index.json', function(json, dm, g3d, datas){
    
    });

#### disableToolTip()

关闭ToolTip功能

#### dm(dataModel) → {[hc.DataModel](hc.DataModel.html)}

获取或设置数据模型，没有参数时相当于[getDataModel](hc.graph3d.Graph3dView.html#getDataModel)，有参数时相当于[setDataModel](hc.graph3d.Graph3dView.html#setDataModel)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`dataModel`&emsp;&emsp;[hc.DataModel](hc.DataModel.html)&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;数据模型

##### Returns:

[hc.DataModel](hc.DataModel.html) - dataModel

#### enableToolTip()

启用ToolTip

#### flyTo(target, options)

相机看向具体的节点或者节点列表

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`target`&emsp;&emsp;[hc.Node](hc.Node.html) | Array | null&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;数据模型  
`options`&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;可选属性,属性包括有：
  
animation：默认false，是否启用动画，可以设置为true或者false或者animation动画对象  
center：默认undefined，新的场景center点，形如 \[0,0,0\]（空的话，target为一个则看向node中心，target为列表则看向根据节点列表计算出来的中心）  
direction：默认undefined，眼睛处于目标的方向（相对目标，受到目标自身旋转影响），例如\[0,1,5\]在目标正面的斜向上  
worldDirection ：默认undefined，眼睛处于目标的方向（相对场景，不受目标旋转影响），例如\[0,1,5\]在目标所在位置的斜向上  
distance ：默认undefined（未定义的话则使用下面的ratio模式计算距离），浮点类型，表示眼睛跟中心的固定距离  
ratio：默认0.8，浮点类型，表示眼睛跟中心的距离动态计算（例如 0.8 表示眼睛在上述方向上动态计算距离以将目标包围盒的8个角全部适配到屏幕80%范围内）

#### getAspect() → {Number}

获取截头锥体的宽高比

##### Returns:

Number

#### getAxisXColor() → {color}

获取x轴线颜色

##### Returns:

color

#### getAxisYColor() → {color}

获取y轴线颜色

##### Returns:

color

#### getAxisZColor() → {color}

获取z轴线颜色

##### Returns:

color

#### getBoundaries() → {Array}

获取碰撞边界

##### Returns:

Array

#### getBrighcness(data) → {Number}

获取图元最终亮度，默认为1,大于1变亮，小于1变暗

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元  

##### Returns:

Number

#### getCanvas() → {htmlCanvasElement}

获取渲染的画布

##### Returns:

htmlCanvasElement - 画布

#### getCenter() → {Array}

获取拓扑中心点

##### Returns:

Array - 中心点坐标，格式：\[x, y, z\]

#### getCurrentSubGraph() → {[hc.SubGraph](hc.SubGraph.html)}

获取当前子网

##### Returns:

[hc.SubGraph](hc.SubGraph.html) - 子网对象

#### getDataAt(pointOrEvent) → {[hc.Data](hc.Data.html)}

传入逻辑坐标点或者交互event事件参数，返回当前点下的图元

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`pointOrEvent`&emsp;&emsp;Object | Event&emsp;&emsp;逻辑坐标点或交互事件对象(如鼠标事件对象)  

##### Returns:

[hc.Data](hc.Data.html) - 点下的图元

#### getDataInfoAt(pointOrEvent) → {Object}

传入逻辑坐标点或者交互event事件参数，返回当前点下的图元及part信息

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`pointOrEvent`&emsp;&emsp;Object | Event&emsp;&emsp;逻辑坐标点或交互事件对象(如鼠标事件对象)  

##### Returns:

Object - 图元和part信息

#### getDataModel() → {[hc.DataModel](hc.DataModel.html)}

获取绑定的数据模型

##### Returns:

[hc.DataModel](hc.DataModel.html) - 数据模型

#### getDatasInRect(rect) → {[hc.List](hc.List.html)}

获取矩形区域内的图元

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`rect`&emsp;&emsp;&emsp;&emsp;rect&emsp;&emsp;&emsp;逻辑坐标区域 

##### Returns:

[hc.List](hc.List.html)

#### getEditableFunc() → {function}

获取编辑过滤器函数

##### Returns:

function

#### getEditSizeColor() → {color}

获取大小编辑控制条的颜色

##### Returns:

color

#### getEye() → {Array}

获取眼睛（或Camera）所在位置，默认值为\[0, 300, 1000\]

##### Returns:

Array - 眼睛位置坐标，格式\[x, y, z\]

#### getFar() → {Number}

获取远端截面位置，默认值为10000

##### Returns:

Number

#### getFovy() → {Number}

获取垂直方向的视觉张角弧度，默认值为Math.PI/4

##### Returns:

Number

#### getGridColor() → {color}

获取网格线颜色

##### Returns:

color

#### getGridGap() → {Number}

获取网格线间距

##### Returns:

Number

#### getGridSize() → {Number}

获取网格行列数，默认为40

##### Returns:

Number

#### getHeighc() → {Number}

获取拓扑组件的布局高度

##### Returns:

Number

#### getInteractors() → {[hc.List](hc.List.html)}

获取交互器

##### Returns:

[hc.List](hc.List.html)

#### getLabel(data) → {String}

获取图元的label，用于在拓扑上显示文字信息，可重载返回自定义文字

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 

##### Returns:

String - 图元label文字，默认返回data.s('label')||data.getName();

#### getLabel2(data) → {String}

获取图元的第二个label，用于在拓扑上显示文字，可重载返回自定义文字

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 

##### Returns:

String - 图元第二个label的文字，默认返回data.s('label2')

#### getLabel2Background(data) → {color}

获取图元的第二个label的背景色，可重载返回自定义颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 

##### Returns:

color - 图元第二个label的背景色，默认返回data.s('label2.background')

#### getLabel2Color(data) → {color}

获取图元的第二个label的文字颜色，可重载返回自定义颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 

##### Returns:

color -

图元第二个label的文字颜色，默认返回data.s('label2.color')

#### getLabelBackground(data) → {color}

获取图元label的背景色，可重载返回自定义颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 

##### Returns:

color - 图元label的背景色，默认返回data.s('label.background')

#### getLabelColor(data) → {color}

获取图元label的文字颜色，可重载返回自定义颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 

##### Returns:

color - 图元label的文字颜色，默认返回data.s('label.color')

#### getLineLength(edgeOrPolyLine) → {Number}

获取连线或者管道长度

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`edgeOrPolyLine`&emsp;&emsp;[hc.Edge](hc.Edge.html) | [hc.PolyLine](hc.PolyLine.html)&emsp;&emsp;连线或者管道 

##### Returns:

Number - 长度

#### getLineOffset(edgeOrPolyLine, offset) → {Object}

获取连线或者管道指定比例的偏移信息

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`edgeOrPolyLine`&emsp;&emsp;[hc.Edge](hc.Edge.html) | [hc.PolyLine](hc.PolyLine.html)&emsp;&emsp;连线或者管道  
`offset`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;偏移百分比  

##### Returns:

Object - 返回 {point, tangent} 这样的对象，其中 point 是 3D 坐标，tangent 是切线方向

#### getMovableFunc() → {function}

获取移动过滤器函数

##### Returns:

function

#### getMoveStep() → {Number}

获取移动漫游步进

##### Returns:

Number

#### getNear() → {Number}

获取近端截面位置，默认值为10

##### Returns:

Number

#### getNote(data) → {String}

获取图元的note，用于在拓扑上显示标注信息，可重载返回自定义文字

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 

##### Returns:

String - 图元note文字，默认返回data.s('note')

#### getNote2(data) → {String}

获取图元的第二个note，用于在拓扑上显示标注信息，可重载返回自定义文字

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 

##### Returns:

String - 图元第二个note文字，默认返回data.s('note2')

#### getNote2Background(data) → {color}

获取图元的第二个note的背景色，可重载返回自定义颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 

##### Returns:

color - 图元第二个note的背景色，默认返回data.s('note2.background')

#### getNoteBackground(data) → {color}

获取图元note的文字颜色，可重载返回自定义颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 

##### Returns:

color - 图元note的文字颜色，默认返回data.s('note.background')

#### getOpacity(data) → {Number}

获取图元的透明度，可重载返回自定义透明度

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 

##### Returns:

Number - 图元透明度，默认返回data.s('opacity')

#### getOrthoWidth() → {Number}

获取正交投影宽度，默认为2000

##### Returns:

Number

#### getRectSelectBackground() → {color}

获取框选选择框的背景色

##### Returns:

color

#### getRotateStep() → {Number}

获取旋转步进

##### Returns:

Number

#### getRotationEditableFunc() → {function}

获取旋转编辑过滤器函数

##### Returns:

function

#### getSelectableFunc() → {function}

获取选择过滤器函数

##### Returns:

function

#### getSelectionModel() → {[hc.SelectionModel](hc.SelectionModel.html)}

获取选中模型

##### Returns:

[hc.SelectionModel](hc.SelectionModel.html)

See:

*   [sm](hc.graph3d.Graph3dView.html#sm)

#### getSizeEditableFunc() → {function}

获取大小编辑过滤器

##### Returns:

function

#### getTextureMap() → {Object}

获取组件内部的贴图映射表

##### Returns:

Object

#### getToolTip(e) → {String}

获取ToolTip文字，可重载返回自定义的toolTip文字

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`e`&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;鼠标或Touch事件对象 

##### Returns:

String - toolTip文字，默认取出鼠标下的图元，然后返回其getToolTip()

#### getUp() → {Array}

获取摄像头正上方向，该参数一般较少改动，默认值为\[0, 1, 0\]

##### Returns:

Array - 格式：\[x, y, z\]

#### getView() → {htmlDivElement}

获取拓扑组件的根层div

##### Returns:

htmlDivElement

#### getVisibleFunc() → {function}

获取可见过滤器函数

##### Returns:

function

#### getWidth() → {Number}

获取拓扑组件的布局宽度

##### Returns:

Number

#### getWireframe(data) → {Object}

定义图元立体线框效果

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;数据元素 

##### Returns:

Object

##### Example

    //示例:
    g3d.getWireframe = function(data){
    var visible = data.s('wf.visible');
     if(visible === true || (visible === 'selected' && this.isSelected(data))){
         return {
             color: data.s('wf.color'),
             width: data.s('wf.width'),
             short: data.s('wf.short'),
             mat: data.s('wf.mat')
         };
     }
    },

#### invalidate(delay)

无效拓扑，并调用延时刷新

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms)

See:

*   [iv](hc.graph3d.Graph3dView.html#iv)

#### invalidateAll()

无效拓扑中的所有图元

#### invalidateData(data)

无效拓扑中的图元

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;要无效的图元

#### invalidateSelection()

无效选中模型中的图元

#### isAutoMakeVisible() → {Boolean}

选中图元时，是否自动平移拓扑以确保该图元出现在可见区域内

##### Returns:

Boolean

#### isCenterAxisVisible() → {Boolean}

是否显示中心点轴线

##### Returns:

Boolean

#### isDashDisabled() → {Boolean}

组件是否禁用虚线效果

##### Returns:

Boolean

#### isDisabled() → {Boolean}

组件是否处于不可用状态，处于此状态时不能进行任何操作并且会遮挡一层蒙板

##### Returns:

Boolean

#### isEditable(data) → {Boolean}

判断图元是否可被编辑

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元

##### Returns:

Boolean

#### isFirstPersonMode() → {Boolean}

是否是第一人称模式

##### Returns:

Boolean

#### isGridVisible() → {Boolean}

是否显示网格

##### Returns:

Boolean

#### isMouseRoamable() → {Boolean}

是否使用鼠标漫游，默认为true, 如果改为false, 则鼠标左键右键都不支持前进后退的操作功能，  
但左键可拖拽编辑图元，右键可改变视角方向，采用这样的方式一般会结合键盘w|s|a|d按键进行漫游操作

##### Returns:

Boolean

#### isMovable(data) → {Boolean}

判断图元是否可移动

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元


##### Returns:

Boolean

#### isOriginAxisVisible() → {Boolean}

是否显示坐标原点\[0,0,0\]轴线

##### Returns:

Boolean

#### isOrtho() → {Boolean}

是否使用正交投影

##### Returns:

Boolean

#### isPannable() → {Boolean}

是否允许平移操作

##### Returns:

Boolean

#### isRectSelectable() → {Boolean}

是否允许框选操作

##### Returns:

Boolean

#### isResettable() → {Boolean}

判断是否允许通过空格将拓扑复位

##### Returns:

Boolean

#### isRotatable() → {Boolean}

是否可旋转

##### Returns:

Boolean

#### isRotationEditable(data) → {Boolean}

判断图元是否可编辑旋转

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元

##### Returns:

Boolean

#### isSelectable(data) → {Boolean}

判断图元是否可被选中

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元


##### Returns:

Boolean

#### isSelected(data) → {Boolean}

判断图元是否被选中

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元


##### Returns:

Boolean

#### isSelectedById(id) → {Boolean}

根据id判断图元是否被选中

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`id`&emsp;&emsp;&emsp;&emsp;String | Number&emsp;&emsp;图元id

##### Returns:

Boolean

#### isSelectionModelShared() → {Boolean}

当前拓扑是否共享选中模型

##### Returns:

Boolean

#### isSizeEditable(data) → {Boolean}

图元是否可编辑大小

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元


##### Returns:

Boolean

#### isVisible(data) → {Boolean}

判断图元是否可见

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元


##### Returns:

Boolean

#### isWalkable() → {Boolean}

是否可进退

##### Returns:

Boolean

#### isZoomable() → {Boolean}

是否可缩放

##### Returns:

Boolean

#### iv(delay)

无效拓扑，并调用延时刷新，[invalidate](hc.graph3d.Graph3dView.html#invalidate)的缩写

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms)

See:

*   [invalidate](hc.graph3d.Graph3dView.html#invalidate)

#### makeVisible(data)

平移拓扑以确保该图元在可见区域内

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元


#### mi(listener, scope, ahead)

增加交互事件监听器，[addInteractorListener](hc.graph3d.Graph3dView.html#addInteractorListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


See:

*   [addInteractorListener](hc.graph3d.Graph3dView.html#addInteractorListener)

##### Example

    //示例：
    graph3dView.mi(function(event) {
    		//event格式：
    		{
    			kind: 'clickData',//事件类型
    			data: data,//事件相关的数据元素
    			part: "part",//事件的区域,icon、label等
    			event: e//html原生事件
    		}
    });

#### moveCamera(eye, center, anim)

移动场景相机中心点位置

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`eye`&emsp;&emsp;&emsp;&emsp;Array&emsp;&emsp;&emsp;相机位置坐标  
`center`&emsp;&emsp;&emsp;Array&emsp;&emsp;&emsp;中心点位置坐标  
`anim`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;是否使用动画

#### moveSelection(dx, dy, dz)

移动选中模型中图元的位置

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`dx`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;x轴方向移动值  
`dy`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;y轴方向移动值  
`dz`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;z轴方向移动值


#### mp(listener, scope, ahead)

增加自身属性变化事件监听器，[addPropertyChangeListener](hc.graph3d.Graph3dView.html#addPropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域  
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [addPropertyChangeListener](hc.graph3d.Graph3dView.html#addPropertyChangeListener)

#### onAutoLayoutEnded()

自动布局动画结束后时回调，可重载做后续处理

#### onBackgroundClicked(event)

单击拓扑背景时回调，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`event`&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;事件对象  

#### onBackgroundDoubleClicked(event)

双击拓扑背景时回调，默认调用upSubGraph()进入上一层子网，可重载改变默认逻辑或做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`event`&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;事件对象  

#### onDataClicked(data, e, part)

图元被点击时回调，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;被点击的图元  
`e`&emsp;&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;事件对象   
`part`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;区域   

#### onDataDoubleClicked(data, e, part)

图元被双击时回调，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;被点击的图元  
`e`&emsp;&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;事件对象   
`part`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;区域  

#### onEdgeDoubleClicked(edge, e, part)

连线图元被双击时回调，默认调用edge.toggle()，可重载改变默认逻辑或做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`edge`&emsp;&emsp;&emsp;[hc.Edge](hc.Edge.html)&emsp;&emsp;&emsp;连线  
`e`&emsp;&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;事件对象   
`part`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;区域  


#### onGroupDoubleClicked(group, e, part)

组类型图元被双击时回调，默认实现调用group.toggle()，可重载改变默认逻辑或做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`group`&emsp;&emsp;&emsp;[hc.Group](hc.Group.html)&emsp;Group对象  
`e`&emsp;&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;事件对象   
`part`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;区域  

#### onMoveEnded()

移动图元位置结束时回调，可重载做后续处理

#### onPanEnded()

手抓图平移拓扑图结束时回调，可重载做后续处理

#### onPinchEnded()

触屏进行双指缩放结束时回调，可重载做后续处理

#### onRectSelectEnded()

框选结束时回调，可重载做后续处理

#### onRotateEnded()

旋转结束时回调，可重载做后续处理

#### onSelectionChanged(event)

选中变化时回调，默认实现会使得该选中图元出现在拓扑图上的可见范围

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description    
`event`&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;选中变化事件对象  

#### onSubGraphDoubleClicked(subGraph, event, part)

子网图元被双击时回调，默认实现进入子网

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`subGraph`&emsp;&emsp;&emsp; [hc.SubGraph](hc.SubGraph.html)&emsp;&emsp;子网对象  
`event`&emsp;&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;&emsp;&emsp;事件对象   
`part`&emsp;&emsp;&emsp;&emsp;&emsp; Object&emsp;&emsp;&emsp;&emsp;&emsp;区域  


#### onWalkEnded(subGraph, event)

进退操作结束时回调，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`subGraph`&emsp;&emsp;&emsp; [hc.SubGraph](hc.SubGraph.html)&emsp;&emsp;子网对象  
`event`&emsp;&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;&emsp;&emsp;事件对象   

#### onZoomEnded()

缩放动画结束时回调

#### pan(dx, dy, anim, firstPersonMode)

上下左右四个方向的平移，本质为eye和center同时做四个方向的相同偏移量，  
dx左右偏移参数，dy上下偏移参数，dx和dy一般代表屏幕移动像素，  
Graph3dView自动会换算成合理的3D空间逻辑坐标偏移量。  
  
firstPersonMode参数为空时则默认采用Graph3dView#isFirstPersonMode()当前值，  
如果为第一人称模式调用pan操作，该函数会考虑Graph3dView#getBoundaries()边界限制。

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`dx`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;dx&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;x轴方向的偏移量  
`dy`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;dy&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;y轴方向的偏移量    
`anim`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;是否使用动画  
`firstPersonMode`&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;是否第一人称模式


#### redraw()

重绘拓扑

#### removeInteractorListener(listener, scope)

删除交互事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [umi](hc.graph3d.Graph3dView.html#umi)

#### removePropertyChangeListener(listener, scope)

删除自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

#### removeSelection()

删除所有选中的图元

#### removeViewListener(listener, scope)

删除视图事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

#### reset()

复位函数，调用该函数将eye、center和up三个变量设置为hc.Default上对应的 graph3dViewCenter、graph3dViewEye和graph3dViewUp初始默认值。

#### rotate(leftRighc, upDown, anim, firstPersonMode)

上下左右四个方位旋转一定角度

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`leftRighc`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;水平旋转弧度  
`value`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;垂直旋转弧度  
`anim`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;是否使用动画  
`firstPersonMode`&emsp;&emsp;Boolean&emsp;&emsp;是否第一人称模式，为空时则采用Graph3dView#isFirstPersonMode()，该参数将影响旋转移动的参照标准，为默认非第一人称模式时， 旋转是以center为中心进行旋转，也就是围绕中心物体旋转，当为第一人称时旋转以eye为中心进行旋转，也就是旋转眼睛朝向方向。

#### selectAll()

选中拓扑中所有图元

#### setAspect(v)

设置截头锥体的宽高比，该参数默认自动根据屏幕的宽高比决定，一般不需要设置。

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Number

#### setAutoMakeVisible(v)

设置当选中图元时，是否自动平移拓扑以确保该图元出现在可见区域内

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setAxisXColor(color)

设置x轴线颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color

#### setAxisYColor(color)

设置y轴线颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color

#### setAxisZColor(color)

设置z轴线颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color

#### setBoundaries(boundaries)

设置碰撞边界

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`boundaries`&emsp;&emsp;&emsp;Array&emsp;&emsp;边界数组

##### Example

    //示例：
    g3d.setBoundaries([
      [
          p0.x, p0.y,
          p1.x, p1.y,
          p2.x, p2.y,
          p3.x, p3.y            
      ],
      [
          p4.x, p4.y,
          p5.x, p5.y,
          p6.x, p6.y            
      ]
    ]);    

#### setCenter(center)

设置中心点

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`center`&emsp;&emsp;&emsp;Array&emsp;&emsp;中心点坐标，格式：\[x, y, z\]


#### setCenterAxisVisible(v)

设置是否显示中心点轴线

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setCurrentSubGraph(subGraph)

设置当前子网

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`subGraph`&emsp;&emsp;&emsp;[hc.SubGraph](hc.SubGraph.html)&emsp;&emsp;子网对象

#### setDashDisabled(v)

设置是否禁用虚线效果

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setDataModel() → {[hc.DataModel](hc.DataModel.html)}

设置绑定的数据模型

##### Returns:

[hc.DataModel](hc.DataModel.html) - 数据模型

#### setDisabled(value, iconUrl)

设置组件是否处于不可用状态，处于不可用状态时不能进行任何操作并且会遮挡一层蒙板

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`value`&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 是否禁用组件  
`iconUrl`&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;蒙板上显示的icon的路径

#### setEditable(editable)

设置拓扑中的图元是否可编辑

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`editable`&emsp;&emsp;&emsp;Boolean&emsp;&emsp;icon名  

#### setEditableFunc(func)

设置编辑过滤器函数

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function&emsp;&emsp;过滤器函数 

#### setEditSizeColor(color)

设置大小编辑控制条的颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color

#### setEye(eye)

设置眼睛（或Camera）所在位置，默认值为\[0, 300, 1000\]

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`eye`&emsp;&emsp;&emsp;&emsp;Array &emsp;&emsp;眼睛位置坐标，格式\[x, y, z\]

#### setFar(far)

设置远端截面位置，默认值为10000

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`far`&emsp;&emsp;&emsp;&emsp;Number

#### setFirstPersonMode(mode)

设置第一人称模式

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`mode`&emsp;&emsp;&emsp;&emsp;Boolean

#### setFovy(fovy)

设置垂直方向的视觉张角弧度，默认值为Math.PI/4

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`fovy`&emsp;&emsp;&emsp;&emsp;Number

#### setGridColor(color)

设置网格线颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color


#### setGridGap(gap)

设置网格线间距

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`gap`&emsp;&emsp;&emsp;&emsp;Number


#### setGridSize(size)

设置网格行列数，默认为40

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`size`&emsp;&emsp;&emsp;&emsp;Number

#### setGridVisible(v)

设置是否显示网格

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean


#### setHeighc(heighc)

设置布局高度

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`heighc`&emsp;&emsp;Number&emsp;&emsp;&emsp;高度值

#### setInteractors(interactors)

设置交互器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`interactors`&emsp;&emsp;[hc.List](hc.List.html)&emsp;&emsp;&emsp;交互器对象集合

#### setMouseRoamable(v)

设置是否使用鼠标漫游，默认为true, 如果改为false, 则鼠标左键右键都不支持前进后退的操作功能，  
但左键可拖拽编辑图元，右键可改变视角方向，采用这样的方式一般会结合键盘w|s|a|d按键进行漫游操作

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setMovableFunc(func)

设置移动过滤器函数

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;过滤器函数


#### setMoveStep(v)

设置移动漫游步进

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Number

#### setNear(v)

设置近端截面位置，默认值为10

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Number

#### setOriginAxisVisible(v)

设置是否显示坐标原点\[0,0,0\]轴线

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setOrtho(v)

设置是否使用正交投影

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setOrthoWidth(width)

设置正交投影宽度，默认为2000

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`width`&emsp;&emsp;&emsp;Number

#### setPannable(v)

设置是否允许平移操作

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;是否可平移

#### setRectSelectable(v)

设置拓扑上是否允许框选操作

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setRectSelectBackground(color)

设置框选选择框的背景色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color&emsp;&emsp;&emsp;&emsp;颜色值


#### setResettable(v)

设置是否允许通过空格将拓扑复位

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setRotatable(v)

设置是否可旋转

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setRotateStep(v)

设置旋转步进

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Number

#### setRotationEditableFunc(func)

设置图元是否可编辑旋转过滤器

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function


#### setSelectionModelShared(v)

设置拓扑是否共享选中模型

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setSizeEditableFunc(func)

设置大小编辑过滤器

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function

#### setSkyBox(sky)

设置场景的天空盒节点

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`sky`&emsp;&emsp;&emsp;&emsp;[hc.Node](hc.Node.html)&emsp;&emsp;天空盒节点

##### Example

    var sky = new hc.Node();
    sky.s({
        'top.image': 'images/1.png',
        'left.image': 'images/2.png',
        'front.image': 'images/3.png',
        'righc.image': 'images/4.png',
        'back.image': 'images/5.png',
        'bottom.image': 'images/6.png',
        'all.reverse.flip': true
    });
    g3d.setSkyBox(sky);

#### setUp(up)

设置摄像头正上方向，该参数一般较少改动，默认值为\[0, 1, 0\]

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`up`&emsp;&emsp;&emsp;&emsp;Array&emsp;&emsp;格式：\[x, y, z\]

#### setVisibleFunc(func)

设置可见过滤器

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function&emsp;&emsp;过滤器函数

#### setWalkable(walkable)

设置是否可进退

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`walkable`&emsp;&emsp;Boolean

#### setWidth(width)

设置布局宽度

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`width`&emsp;&emsp;Number

#### setZoom(increment, anim)

缩放操作，默认操作模式意味着eye离center的远近变化，如果在Graph3dView#isOrtho()为true的正交投影情况下，缩放意味着改变Graph3dView#setOrthoWidth(width)的可视宽度范围。

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`increment`&emsp;&emsp;Number&emsp;&emsp;步进的比例，调用zoomIn(anim)和zoomOut(anim)，等同于调用了setZoom(1.3, anim)和setZoom(1/1.3, anim)。  
`anim`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;是否使用动画

#### setZoomable(v)

设置是否可缩放

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Boolean

#### sm() → {[hc.SelectionModel](hc.SelectionModel.html)}

获取选中模型，[getSelectionModel](hc.graph3d.Graph3dView.html#getSelectionModel)的缩写

##### Returns:

[hc.SelectionModel](hc.SelectionModel.html)

See:

*   [getSelectionModel](hc.graph3d.Graph3dView.html#getSelectionModel)

#### toCanvas(background) → {htmlCanvasElement}

将拓扑导出为canvas

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp; Type&emsp;&emsp;&emsp;Description  
`background`&emsp;&emsp;color&emsp;&emsp;背景色

##### Returns:

htmlCanvasElement

#### toDataURL(background) → {String}

将拓扑导出为base64格式字符串

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp; Type&emsp;&emsp;&emsp;Description  
`background`&emsp;&emsp;color&emsp;&emsp;背景色


##### Returns:

String

#### umi(listener, scope)

删除交互事件监听器，[removeInteractorListener](hc.graph3d.Graph3dView.html#removeInteractorListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [removeInteractorListener](hc.graph3d.Graph3dView.html#removeInteractorListener)

#### ump(listener, scope)

删除自身属性变化事件监听器，[removePropertyChangeListener](hc.graph3d.Graph3dView.html#removePropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [removePropertyChangeListener](hc.graph3d.Graph3dView.html#removePropertyChangeListener)

#### validate()

立刻刷新拓扑

#### walk(step, anim, firstPersonMode)

同时改变eye和center的位置，也就是eye和center在两点建立的矢量方向上同时移动相同的偏移量。  
如果为第一人称模式调用walk操作，该函数会考虑Graph3dView#getBoundaries()边界限制

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`step`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;偏移的矢量长度值  
`anim`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;是否使用动画  
`firstPersonMode`&emsp;Boolean&emsp;&emsp;&emsp;是否是第一人称模式，为空时则采用Graph3dView#isFirstPersonMode()  


#### zoomIn(anim)

相当于调用setZoom(1.3, anim)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`anim`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否使用动画

See:

*   [setZoom](hc.graph3d.Graph3dView.html#setZoom)

#### zoomOut(anim)

相当于调用setZoom(1/1.3, anim)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`anim`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否使用动画


See:

*   [setZoom](hc.graph3d.Graph3dView.html#setZoom)
