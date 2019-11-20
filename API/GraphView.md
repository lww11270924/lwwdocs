
#### new GraphView(dataModel)

拓扑图形组件hc.graph.GraphView是hc框架中2D功能最丰富的组件，其相关类库都在hc.graph包下。  
  
GraphView具有基本图形的呈现和编辑、拓扑节点连线及自动布局功能；  
封装了电力和电信等行业预定义对象，具有动画渲染等特效， 因此其应用面很广泛，可作为监控领域的绘图工具和人机界面，或作为一般性的图形化编辑工具，或扩展成工作流和组织图等企业应用。

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`dataModel`&emsp;&emsp;[hc.DataModel](hc.DataModel.html)&emsp;&emsp;绑定的数据模型  

### Methods

#### addBottomPainter(painter)

增加底层Painter  
  
拓扑组件上提供Painter接口，开发者可以使用Canvas的画笔对象自由绘制任意形状，底层Painter绘制在拓扑最下面

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`painter`&emsp;&emsp;&emsp;function&emsp;&emsp;Painter类

##### Example

    //Painter示例：
    graphView.addBottomPainter(function(g){
        g.fillStyle = '#000000';
        g.fillRect(0, 0, 100, 100);
    });

#### addInteractorListener(listener, scope, ahead)

增加交互事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


See:

*   [mi](hc.graph.GraphView.html#mi)

##### Example

    //示例：
    graphView.addInteractorListener(function(event) {
    		//event格式：
    		{
    			//clickData, doubleClickData, clickBackground, doubleClickBackground, 
    			//beginRectSelect, betweenRectSelect, endRectSelect, beginMove, betweenMove, endMove,
    			//beginPan, betweenPan, endPan, beginEditRect, betweenEditRect, endEditRect, beginEditPoint, betweenEditPoint, endEditPoint
    			//beginEditRotation, betweenEditRotation, endEditRotation, moveLeft, moveRighc, moveUp, moveDown, toggleNote, toggleNote2
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

*   [mp](hc.graph.GraphView.html#mp)

#### addToDOM(parentNode)

将组件加入到指定的DOM元素底下，不指定则加入到 document.body 下

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`parentNode`&emsp;&emsp;&emsp;&emsp;DOM&emsp;&emsp;DOM元素,默认为 document.body 

#### addTopPainter(painter)

增加顶层Painter  
  
拓扑组件上提供Painter接口，开发者可以使用Canvas的画笔对象自由绘制任意形状，顶层Painter绘制在拓扑最上面

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`painter`&emsp;&emsp;&emsp;function&emsp;&emsp;Painter类 

##### Example

    //Painter示例：
    graphView.addTopPainter(function(g){
        g.fillStyle = '#000000';
        g.fillRect(0, 0, 100, 100);
    });

#### addViewListener(listener, scope, ahead)

监听视图事件，如布局、刷新等

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


#### adjustTranslateX(value) → {Number}

传入即将设置的水平平移值，返回最终设置值，可重载限制水平平移范围

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp; Description  
`value`&emsp;&emsp;Number&emsp;&emsp;原始水平平移值  


##### Returns:

Number - 新的水平平移值

#### adjustTranslateY(value) → {Number}

传入即将设置的垂直平移值，返回最终设置值，可重载限制垂直平移范围

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp; Description  
`value`&emsp;&emsp;Number&emsp;&emsp;原始垂直平移值  

##### Returns:

Number - 新的垂直平移值

#### adjustZoom(value) → {Number}

传入即将修改的缩放值，返回最终运行设置的缩放值，可重载进行自定义

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp; Description  
`value`&emsp;&emsp;Number&emsp;&emsp;原始缩放值
 
##### Returns:

Number -

最终缩放值

#### deserialize(jsonUrl, callback)

根据 json 路径请求并反序列图纸

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp; Description  
`jsonUrl`&emsp;&emsp;String&emsp;&emsp;&emsp;图纸 json 路径  
`callback`&emsp;&emsp;function&emsp;&emsp;回调函数

##### Example

    //示例:
    g3d.deserialize('previews/index.json', function(json, dm, gv, datas){
    
    });

#### disableDashFlow()

停止虚线流动，hc-dashflow.js 扩展的 API

#### disableFlow()

停止流动，hc-flow.js 扩展的 API

#### disableToolTip()

关闭ToolTip功能

#### dm(dataModel) → {[hc.DataModel](hc.DataModel.html)}

获取或设置数据模型，没有参数时相当于[getDataModel](hc.graph.GraphView.html#getDataModel)，有参数时相当于[setDataModel](hc.graph.GraphView.html#setDataModel)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`dataModel`&emsp;&emsp;[hc.DataModel](hc.DataModel.html)&emsp;&emsp;\<optional> &emsp;&emsp;数据模型


##### Returns:

[hc.DataModel](hc.DataModel.html) - dataModel

#### each(func, scope)

提供一个回调函数遍历此拓扑中的图元，与DataModel上的each方法不同，此方法还考虑了拓扑中的Layer，从低Layer向高Layer遍历

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;&emsp; function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;遍历函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域


##### Example

    graphView.each(function(data) {
      console.log(data);
    });

#### enableDashFlow(interval)

启动虚线流动，hc-dashflow.js 扩展的 API

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`interval`&emsp;&emsp;Number&emsp;&emsp;流动的时间间隔 

#### enableFlow(interval)

启动流动，hc-flow.js 扩展的 API

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`interval`&emsp;&emsp;Number&emsp;&emsp;流动的时间间隔 

#### enableToolTip()

启用ToolTip

#### firePropertyChange(property, oldValue, newValue)

派发属性变化事件

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp; Description  
`property`&emsp;&emsp;&emsp;String&emsp;&emsp;属性名  
`oldValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;旧值  
`newValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;新值

See:

*   [fp](hc.graph.GraphView.html#fp)

#### fitContent(anim, padding, notZoomIn)

缩放平移整个拓扑以展示所有的图元

##### Parameters:
>Name&emsp;&emsp;&emsp; Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp; Description  
`anim`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否使用动画  
`padding`&emsp;&emsp; Number&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;缩放后图元区域与拓扑边缘的距离，默认为20  
`notZoomIn`&emsp; Boolean&emsp;&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;是否将最小缩放值限定为1


#### fitData(data, anim, padding, notZoomIn, retry)

缩放平移整个拓扑以展示参数Data

##### Parameters:
>Name&emsp;&emsp;&emsp; Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp; Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; &emsp;&emsp;要显示的data  
`anim`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否使用动画   
`padding`&emsp;&emsp; Number&emsp;&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;缩放后图元区域与拓扑边缘的距离，默认为20  
`notZoomIn`&emsp; Boolean&emsp;&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;是否将最小缩放值限定为1  
`retry`&emsp;&emsp;&emsp; Boolean&emsp;&emsp;&emsp;&emsp;\<optional>&emsp;&emsp; 当拓扑状态异常时，是否延时重试fitData，默认为true


#### fitRect(rect, anim, notZoomIn)

缩放平移整个拓扑以展示矩形范围内的图元

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description  
`rect`&emsp;&emsp;&emsp;&emsp; Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;矩形范围  
`anim`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否使用动画  
`notZoomIn` &emsp;Boolean&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将最小缩放值限定为1

#### fp(property, oldValue, newValue)

派发属性变化事件

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp; Description  
`property`&emsp;&emsp;&emsp;String&emsp;&emsp;属性名  
`oldValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;旧值  
`newValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;新值

See:

*   [firePropertyChange](hc.graph.GraphView.html#firePropertyChange)

#### getAutoScrollZone() → {Number}

获取自动滚动区域，当鼠标距离拓扑边缘小于这个值时，拓扑自动滚动(调整translateX或translateY)

##### Returns:

Number - 自动滚动区域

#### getBodyColor(data) → {color}

获取图元body的染色，可重载此方法返回自定义的颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;   Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;要染色的图元  

##### Returns:

color - 最终颜色，默认为data.s('body.color')

#### getBorderColor(data) → {color}

获取图元边框颜色，可重载此方法返回自定义的颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;   Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;要染色的图元  

##### Returns:

color - 最终颜色，默认为data.s('border.color')

#### getBoundsForGroup(child) → {Object}

获取Group内child的尺寸范围，这个尺寸参与计算Group的大小

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;   Description  
`child`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;子节点  

##### Returns:

Object - 子节点的尺寸范围

#### getCanvas() → {htmlCanvasElement}

获取拓扑的画布

##### Returns:

htmlCanvasElement - 画布

#### getContentRect() → {Object}

获取拓扑中所有图元占用的矩形区域

##### Returns:

Object - 内容区域

#### getCurrentSubGraph() → {[hc.SubGraph](hc.SubGraph.html)}

获取当前子网

##### Returns:

[hc.SubGraph](hc.SubGraph.html) - 子网对象

#### getDashFlowInterval()

获取虚线流动的时间间隔，hc-dashflow.js 扩展的 API

#### getDataAt(pointOrEvent, filter, range) → {[hc.Data](hc.Data.html)}

传入逻辑坐标点或者交互event事件参数，返回当前点下的图元，filter可进行过滤

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description  
`pointOrEvent`&emsp;&emsp;Object | Event&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;逻辑坐标点或交互事件对象(如鼠标事件对象)  
`filter`&emsp;&emsp;&emsp;&emsp;&emsp; Functoin&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;过滤器函数，传入data,自定义逻辑返回true或false判断此data是否可被getDataAt返回  
`range`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;扩大点范围

##### Returns:

[hc.Data](hc.Data.html) - 点下的图元

#### getDataModel() → {[hc.DataModel](hc.DataModel.html)}

获取绑定的数据模型

##### Returns:

[hc.DataModel](hc.DataModel.html) - 数据模型

#### getDatasInRect(rect, intersects, selectable) → {[hc.List](hc.List.html)}

获取逻辑坐标区域内的图元

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description  
`rect`&emsp;&emsp;&emsp;&emsp;&emsp;rect&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;逻辑坐标区域   
`intersects`&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;指定相交选中还是包含选中，true表示相交，false表示包含。  
`selectable`&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否只返回可被选中的图元，可否被选中通过isSelectable判断

##### Returns:

[hc.List](hc.List.html)

#### getDataUI(data) → {Object}

获取图元的UI类

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 

##### Returns:

Object

#### getDataUIBounds(data) → {Object}

获取图元UI的绘制范围

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 

##### Returns:

Object

#### getEditableFunc() → {function}

获取编辑过滤器函数

##### Returns:

function

#### getEditInteractor() → {[hc.graph.EditInteractor](hc.graph.EditInteractor.html)|hc.graph.XEditInteractor}

获取编辑交互器

##### Returns:

[hc.graph.EditInteractor](hc.graph.EditInteractor.html) | hc.graph.XEditInteractor

#### getEditPointBackground() → {color}

获取编辑交互器中编辑点的背景色

##### Returns:

color

#### getEditPointBorderColor() → {color}

获取编辑交互器中编辑点的边框颜色

##### Returns:

color

#### getEditPointSize() → {Object}

获取编辑交互器中编辑点的尺寸

##### Returns:

Object

#### getFlowInterval()

获取流动的时间间隔，hc-flow.js 扩展的 API

#### getHeighc() → {Number}

获取拓扑组件的布局高度

##### Returns:

Number

#### getIconInfoAt(pointOrEvent) → {Object}

传入逻辑坐标点或者交互event事件参数、图元对象，判断当前点下的icon信息

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`pointOrEvent`&emsp;&emsp;Object | Event&emsp;&emsp;逻辑坐标点或交互事件对象(如鼠标事件对象) 

##### Returns:

Object

##### Example

    //返回值示例：
    {
    	data: data,//相关数据元素 
    	key: 'key',//styleIcon名
    	index: 0,//styleIcon中第几个icon
    	name: 'name'//styleIcon中相应icon的名字
    }

#### getInteractors() → {[hc.List](hc.List.html)}

获取交互器

##### Returns:

[hc.List](hc.List.html)

#### getLabel(data) → {String}

获取图元的label，用于在拓扑上显示文字信息，可重载返回自定义文字

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;图元

##### Returns:

String - 图元label文字，默认返回data.s('label')||data.getName();

#### getLabel2(data) → {String}

获取图元的第二个label，用于在拓扑上显示文字，可重载返回自定义文字

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;图元

##### Returns:

String - 图元第二个label的文字，默认返回data.s('label2')

#### getLabel2Background(data) → {color}

获取图元的第二个label的背景色，可重载返回自定义颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;图元

##### Returns:

color - 图元第二个label的背景色，默认返回data.s('label2.background')

#### getLabel2Color(data) → {color}

获取图元的第二个label的文字颜色，可重载返回自定义颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;图元

##### Returns:

color - 图元第二个label的文字颜色，默认返回data.s('label2.color')

#### getLabelBackground(data) → {color}

获取图元label的背景色，可重载返回自定义颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;图元

##### Returns:

color - 图元label的背景色，默认返回data.s('label.background')

#### getLabelColor(data) → {color}

获取图元label的文字颜色，可重载返回自定义颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;图元

##### Returns:

color - 图元label的文字颜色，默认返回data.s('label.color')

#### getLayers() → {Array}

获取拓扑中已定义的层

##### Returns:

Array

#### getLogicalPoint(event) → {Object}

传入html事件对象，将事件坐标转换为拓扑中的逻辑坐标

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp; Description  
`event`&emsp;&emsp;&emsp; Event&emsp;&emsp;事件对象

##### Returns:

Object

See:

*   [lp](hc.graph.GraphView.html#lp)

#### getMovableFunc() → {function}

获取移动过滤器函数

##### Returns:

function

#### getNote(data) → {String}

获取图元的note，用于在拓扑上显示标注信息，可重载返回自定义文字

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;图元

##### Returns:

String -

图元note文字，默认返回data.s('note')

#### getNote2(data) → {String}

获取图元的第二个note，用于在拓扑上显示标注信息，可重载返回自定义文字

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;图元

##### Returns:

String - 图元第二个note文字，默认返回data.s('note2')

#### getNote2Background(data) → {color}

获取图元的第二个note的背景色，可重载返回自定义颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;图元

##### Returns:

color - 图元第二个note的背景色，默认返回data.s('note2.background')

#### getNoteBackground(data) → {color}

获取图元note的文字颜色，可重载返回自定义颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;图元

##### Returns:

color - 图元note的文字颜色，默认返回data.s('note.background')

#### getOpacity(data) → {Number}

获取图元的透明度，可重载返回自定义透明度

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;图元

##### Returns:

Number - 图元透明度，默认返回data.s('opacity')

#### getPointEditableFunc() → {function}

获取点编辑(Shape、Edge等)过滤器函数

##### Returns:

function

#### getRectEditableFunc() → {function}

获取大小编辑过滤器函数

##### Returns:

function

#### getRectSelectBackground() → {color}

获取框选选择框的背景色

##### Returns:

color

#### getRectSelectBorderColor() → {color}

获取框选选择框的边框颜色

##### Returns:

color

#### getRotationEditableFunc() → {function}

获取旋转编辑过滤器函数

##### Returns:

function

#### getRotationPoint(data) → {Object}

获取图元编辑时的旋转控制点坐标

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;图元

##### Returns:

Object - 旋转控制点坐标

#### getScrollBarColor() → {color}

获取滚动条颜色

##### Returns:

color

#### getScrollBarSize() → {Number}

获取滚动条宽度

##### Returns:

Number

#### getScrollRect() → {Object}

获取拓扑的滚动区域，即contentRect + viewRect

##### Returns:

Object - 矩形区域

#### getSelectableFunc() → {function}

获取选择过滤器函数

##### Returns:

function

#### getSelectedDataAt(pointOrEvent) → {[hc.Data](hc.Data.html)}

传入逻辑坐标点或者交互event事件参数，返回当前点下已选中的图元

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`pointOrEvent`&emsp;&emsp;Object | Event&emsp;&emsp;逻辑坐标点或交互事件对象(如鼠标事件对象) 

##### Returns:

[hc.Data](hc.Data.html)

#### getSelectionModel() → {[hc.SelectionModel](hc.SelectionModel.html)}

获取选中模型

##### Returns:

[hc.SelectionModel](hc.SelectionModel.html)

See:

*   [sm](hc.graph.GraphView.html#sm)

#### getSelectWidth(data) → {Number}

获取节点选中边框宽度，可重载自定义逻辑

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;节点

##### Returns:

Number - 边框宽度

##### Example

    //示例：重载，隐藏所有节点的选中边框
    graphView.getSelectWidth = function() {return 0};

#### getToolTip(e) → {String}

获取ToolTip文字，可重载返回自定义的toolTip文字

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`e`&emsp;&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;鼠标或Touch事件对象

##### Returns:

String - toolTip文字，默认取出鼠标下的图元，然后返回其getToolTip()

#### getTranslateX() → {Number}

获取水平平移值

##### Returns:

Number - 水平平移值

See:

*   [tx](hc.graph.GraphView.html#tx)

#### getTranslateY() → {Number}

获取垂直平移值

##### Returns:

Number - 垂直平移值

See:

*   [ty](hc.graph.GraphView.html#ty)

#### getView() → {htmlDivElement}

获取拓扑组件的根层div

##### Returns:

htmlDivElement

#### getViewRect() → {Object}

获取拓扑组件中可见区域的逻辑尺寸

##### Returns:

Object

#### getVisibleFunc() → {function}

获取可见过滤器函数

##### Returns:

function

#### getWidth() → {Number}

获取拓扑组件的布局宽度

##### Returns:

Number

#### getZoom() → {Number}

获取拓扑整体缩放值

##### Returns:

Number

#### handleDelete()

处理删除节点，可重载为空函数，阻止按Delete删除节点

#### handlePinch(centerPoint, dist, lastDist)

处理touch上双指操作，可重载重新定义缩放逻辑，一般用于touch上禁用缩放

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`centerPoint`&emsp;&emsp;Object&emsp;&emsp;&emsp;中心的坐标  
`dist`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;起始双指距离  
`lastDist`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;结束双指距离

##### Example

    //示例：将其重载为空函数,禁用touch上双指操作缩放
    graphView.handlePinch = function() {};

#### handleScroll(e, delta)

处理鼠标滚轮缩放，可重载重新定义缩放逻辑，一般用于禁用缩放

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`e`&emsp;&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;&emsp;鼠标滚轮事件  
`delta`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;滚轮增量  

##### Example

    //示例：将其重载为空函数,禁用鼠标滚轮缩放
    graphView.handleScroll = function() {};

#### invalidate(delay)

无效拓扑，并调用延时刷新

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms) 
See:

*   [iv](hc.graph.GraphView.html#iv)

#### invalidateAll()

无效拓扑中的所有图元

#### invalidateData(data)

无效拓扑中的图元

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;要无效的图元 

#### invalidateSelection()

无效选中模型中的图元

#### isAutoHideScrollBar() → {Boolean}

是否自动隐藏滚动条

##### Returns:

Boolean

#### isAutoMakeVisible() → {Boolean}

选中图元时，是否自动平移拓扑以确保该图元出现在可见区域内

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

#### isEditVisible(data) → {Boolean}

图元编辑点是否可见，默认当拓扑缩放值大于0.15时可见

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 


##### Returns:

Boolean

#### isLabelVisible(data) → {Boolean}

判断图元label是否可见，默认当拓扑缩放值大于0.15时可见

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 


##### Returns:

Boolean

#### isMovable(data) → {Boolean}

判断图元是否可移动

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 


##### Returns:

Boolean

#### isNoteVisible(data) → {Boolean}

判断图元note是否可见，默认当拓扑缩放值大于0.15时可见

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 


##### Returns:

Boolean

#### isPannable() → {Boolean}

拓扑是否可以通过鼠标拖拽进行平移操作

##### Returns:

Boolean

#### isPointEditable(data) → {Boolean}

判断图元(Shape、Edge等)的点是否可编辑

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 


##### Returns:

Boolean

#### isRectEditable(data) → {Boolean}

判断图元大小是否可编辑

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 


##### Returns:

Boolean

#### isRectSelectable() → {Boolean}

判断拓扑上是否允许框选操作

##### Returns:

Boolean

#### isResettable() → {Boolean}

判断拓扑上是否允许通过空格将拓扑的缩放和平移值复位

##### Returns:

Boolean

#### isRotationEditable(data) → {Boolean}

判断图元是否可编辑旋转

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 


##### Returns:

Boolean

#### isScrollBarVisible() → {Boolean}

判断拓扑滚动条是否可见

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
>Name&emsp;&emsp; Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`id`&emsp;&emsp;&emsp;&emsp;String | Number&emsp;&emsp;图元id 

##### Returns:

Boolean

#### isSelectionModelShared() → {Boolean}

当前拓扑是否共享选中模型

##### Returns:

Boolean

#### isVisible(data) → {Boolean}

判断图元是否可见

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;图元 

##### Returns:

Boolean

#### iv(delay)

无效拓扑，并调用延时刷新，[invalidate](hc.graph.GraphView.html#invalidate)的缩写

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms) 

See:

*   [invalidate](hc.graph.GraphView.html#invalidate)

#### layouthtml(data, html, bound)

对渲染在节点上的dom|hc.widget组件|hc.ui组件进行布局

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp; [hc.Node](hc.Node.html)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;节点  
`html`&emsp;&emsp;&emsp; DOM | Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;dom|hc.widget组件|hc.ui组件  
`bound`&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否不使用使用css transform进行缩放


#### lp(event) → {Object}

传入html事件对象，将事件坐标转换为拓扑中的逻辑坐标，[getLogicalPoint](hc.graph.GraphView.html#getLogicalPoint)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`event`&emsp;&emsp;&emsp;Event&emsp;&emsp; 事件对象  

##### Returns:

Object

See:

*   [getLogicalPoint](hc.graph.GraphView.html#getLogicalPoint)

#### makeVisible(data)

平移拓扑以确保该图元在可见区域内

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp; 图元  

#### mi(listener, scope, ahead)

增加交互事件监听器，[addInteractorListener](hc.graph.GraphView.html#addInteractorListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [addInteractorListener](hc.graph.GraphView.html#addInteractorListener)

##### Example

    //示例：
    graphView.mi(function(event) {
    		//event格式：
    		{
    			//clickData, doubleClickData, clickBackground, doubleClickBackground, 
    			//beginRectSelect, betweenRectSelect, endRectSelect, beginMove, betweenMove, endMove,
    			//beginPan, betweenPan, endPan, beginEditRect, betweenEditRect, endEditRect, beginEditPoint, betweenEditPoint, endEditPoint
    			//beginEditRotation, betweenEditRotation, endEditRotation, moveLeft, moveRighc, moveUp, moveDown, toggleNote, toggleNote2
    			kind: 'clickData',//事件类型
    			data: data,//事件相关的数据元素
    			part: "part",//事件的区域,icon、label等
    			event: e//html原生事件
    		}
    });

#### moveSelection(offsetX, offsetY)

移动选中模型中图元的位置

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp; Description  
`offsetX`&emsp;&emsp;&emsp;Number&emsp;&emsp;水平移动值  
`offsetY`&emsp;&emsp;&emsp;Number&emsp;&emsp;垂直移动值

#### mp(listener, scope, ahead)

增加自身属性变化事件监听器，[addPropertyChangeListener](hc.graph.GraphView.html#addPropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [addPropertyChangeListener](hc.graph.GraphView.html#addPropertyChangeListener)

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

#### onCurrentSubGraphChanged(event)

当前子网变化时回调，默认实现调用reset()恢复默认缩放和平移值，可重载改变默认逻辑或做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`event`&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;事件对象  

#### onDataClicked(data, e)

图元被点击时回调，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;被点击的图元  
`e`&emsp;&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;&emsp;事件对象    

#### onDataDoubleClicked(data, e)

图元被双击时回调，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;被点击的图元  
`e`&emsp;&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;&emsp;事件对象    

#### onEdgeDoubleClicked(edge, e)

连线图元被双击时回调，默认调用edge.toggle()，可重载改变默认逻辑或做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`edge`&emsp;&emsp;&emsp;[hc.Edge](hc.Edge.html)&emsp;&emsp;&emsp;连线  
`e`&emsp;&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;&emsp;事件对象    

#### onGroupDoubleClicked(group, e)

组类型图元被双击时回调，默认实现调用group.toggle()，可重载改变默认逻辑或做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`group`&emsp;&emsp;&emsp;[hc.Group](hc.Group.html)&emsp;&emsp;&emsp;Group对象  
`e`&emsp;&emsp;&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;&emsp;事件对象   

#### onMoveEnded()

移动图元位置结束时回调，可重载做后续处理

#### onPanEnded()

手抓图平移拓扑图结束时回调，可重载做后续处理

#### onPinchEnded()

触屏进行双指缩放结束时回调，可重载做后续处理

#### onRectSelectEnded()

框选结束时回调，可重载做后续处理

#### onSelectionChanged(event)

选中变化时回调，默认实现会使得该选中图元出现在拓扑图上的可见范围

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`event`&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;选中变化事件对象 

#### onSubGraphDoubleClicked(subGraph, event)

子网图元被双击时回调，默认实现进入子网

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description   
`subGraph`&emsp;&emsp;[hc.SubGraph](hc.SubGraph.html)&emsp;&emsp;&emsp;子网对象  
`event`&emsp;&emsp;&emsp;Event&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;事件对象 

#### onTranslateEnded()

平移动画结束时回调，可重载做后续处理

#### onVisibleChanged(data, newVisible)

图元可见状态发生变化时回调，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description   
`data`&emsp;&emsp;&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;&emsp;图元  
`newVisible`&emsp;&emsp;Boolean&emsp;&emsp;&emsp;新的可见状态 

#### onZoomEnded()

缩放动画结束时回调

#### rectContains(data, rect) → {Boolean}

判断图元是否在矩形范围内

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description   
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;&emsp;图元  
`rect`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;矩形 


##### Returns:

Boolean

#### rectIntersects(data, rect) → {Boolean}

判断图元与矩形范围是否相交

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description   
`data`&emsp;&emsp;&emsp; [hc.Data](hc.Data.html)&emsp;&emsp;&emsp;图元  
`rect`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;矩形 

##### Returns:

Boolean

#### redraw(rect)

重绘拓扑，rect参数为空时重绘拓扑中的所有图元，否则重绘矩形范围内的图元

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description   
`rect`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;矩形范围

#### removeBottomPainter(painter)

删除底层Painter

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`painter`&emsp;&emsp;&emsp;Object&emsp;&emsp;Painter类 

#### removeInteractorListener(listener, scope)

删除交互事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [umi](hc.graph.GraphView.html#umi)

#### removePropertyChangeListener(listener, scope)

删除自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [ump](hc.graph.Overview.html#ump)

#### removePropertyChangeListener(listener, scope)

删除自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

#### removeSelection()

删除所有选中的图元

#### removeTopPainter(painter)

删除顶层Painter

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`painter`&emsp;&emsp;&emsp;Object&emsp;&emsp;Painter类 

#### removeViewListener(listener, scope)

删除视图事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

#### reset()

重置拓扑状态，将zoom设为1，translate设为0

#### reverseEach(func, scope)

提供一个回调函数倒序遍历此拓扑中的图元，与DataModel上的each方法不同，此方法还考虑了拓扑中的Layer，从高Layer向低Layer遍历

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;&emsp; function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;遍历函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域


##### Example

    graphView.reverseEach(function(data) {
      console.log(data);
    });

#### selectAll()

选中拓扑中所有图元

#### setAutoHideScrollBar(v)

设置是否自动隐藏滚动条

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setAutoMakeVisible(v)

设置当选中图元时，是否自动平移拓扑以确保该图元出现在可见区域内

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean


#### setAutoScrollZone(v)

设置自动滚动区域大小，当鼠标距离拓扑边缘小于这个值时，拓扑自动滚动(调整translateX或translateY)

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean


#### setCurrentSubGraph(subGraph)

设置当前子网

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`subGraph`&emsp;&emsp;&emsp;[hc.SubGraph](hc.SubGraph.html)&emsp;&emsp;子网对象

#### setDashFlowInterval(interval)

设置虚线流动的时间间隔，hc-dashflow.js 扩展的 API

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`interval`&emsp;&emsp;&emsp;Number&emsp;&emsp;流动的时间间隔

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
`editable`&emsp;&emsp;&emsp;Boolean

#### setEditableFunc(func)

设置编辑过滤器函数

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function&emsp;&emsp;过滤器函数

##### Example

    graphView.setEditableFunc(function(data) {
       if (data instanceof hc.Edge) return true
       else return false // 除了 hc.Edge 类型其它类型都不可编辑
    })

#### setEditPointBackground(color)

设置编辑交互器中编辑点的背景色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color&emsp;&emsp;颜色值

#### setEditPointBorderColor(color)

设置编辑交互器中编辑点的边框颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color&emsp;&emsp;颜色值

#### setEditPointSize(size)

设置编辑交互器中编辑点的尺寸

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`size`&emsp;&emsp;&emsp;Number&emsp;&emsp;编辑点尺寸

#### setFlowInterval(interval)

设置流动的时间间隔，hc-flow.js 扩展的 API

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`interval`&emsp;&emsp;&emsp;Number&emsp;&emsp;流动的时间间隔

#### setHeighc(heighc)

设置布局高度

##### Parameters:
>Name&emsp;&emsp;&emsp; Type&emsp;&emsp;&emsp;Description  
`heighc`&emsp;&emsp;&emsp;Number&emsp;&emsp;高度值

#### setInteractors(interactors)

设置交互器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp; &emsp;Type&emsp;&emsp;&emsp;Description  
`interactors`&emsp;&emsp;[hc.List](hc.List.html)&emsp;&emsp;交互器对象集合


#### setLayers(layers)

定义拓扑中的层，参数为数组，数组中每个元素代表一个层，层在数组中的索引越大，在拓扑中就越靠上显示  
  
注意，图元的默认layer是0，因此如果定义的层中不包含0，所有的图元默认将不可见

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`layers`&emsp;&emsp;Array&emsp;&emsp;层数组

##### Example

    graphView.setLayers([0, 1, 'Layer2']);
    node.setLayer(1);
    node2.setLayer('Layer2');

#### setMovableFunc(func)

设置移动过滤器函数

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function&emsp;&emsp;过滤器函数

#### setPannable(v)

设置是否可以通过鼠标拖拽进行平移操作

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;是否可平移

#### setPointEditableFunc(func)

设置点编辑(Shape、Edge等)过滤器函数

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function&emsp;&emsp;过滤器函数

#### setRectEditableFunc(func)

设置大小编辑过滤器函数

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function&emsp;&emsp;过滤器函数

#### setRectSelectable(v)

设置拓扑上是否允许框选操作

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setRectSelectBackground(color)

设置框选选择框的背景色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color&emsp;&emsp;颜色值


#### setRectSelectBorder(color)

设置框选选择框的边框颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color&emsp;&emsp;颜色值


#### setResettable(v)

设置拓扑上是否允许通过空格将拓扑的缩放和平移值复位

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setRotationEditableFunc(func)

设置旋转编辑过滤器函数

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function&emsp;&emsp;过滤器函数

#### setScrollBarColor(color)

设置滚动条颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`color`&emsp;&emsp;&emsp;color&emsp;&emsp;&emsp;颜色值

#### setScrollBarSize(size)

设置滚动条宽度

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`size`&emsp;&emsp;&emsp;Number&emsp;&emsp;宽度值

#### setScrollBarVisible(visible)

设置滚动条是否可见

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`visible`&emsp;&emsp;&emsp;Boolean

#### setSelectableFunc(func)

设置选择过滤器函数

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;func&emsp;&emsp;过滤器函数

#### setSelectionModelShared(v)

设置拓扑是否共享选中模型

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;Boolean

#### setTranslate(x, y, anim)

设置拓扑水平和垂直平移值

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;水平平移值  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;垂直平移值  
`anim`&emsp;&emsp;Boolean&emsp;&emsp; \<optional> &emsp;&emsp;是否使用动画

#### setTranslateX(x)

设置拓扑水平平移值

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;水平平移值 

#### setTranslateY(y)

设置拓扑垂直平移值

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`y`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;垂直平移值 

#### setVisibleFunc(func)

设置可见过滤器

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function&emsp;&emsp;过滤器函数 

#### setWidth(width)

设置布局宽度

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`width`&emsp;&emsp;&emsp;Number&emsp;&emsp;宽度值 

#### setZoom(value, anim, point)

设置拓扑缩放值

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description  
`value`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;缩放值  
`anim`&emsp;&emsp;&emsp;&emsp; Boolean&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否使用动画  
`point`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp; \<optional> &emsp;&emsp;缩放中心点的坐标

#### showScrollBar()

显示滚动条

#### sm() → {[hc.SelectionModel](hc.SelectionModel.html)}

获取选中模型，[getSelectionModel](hc.graph.GraphView.html#getSelectionModel)的缩写

##### Returns:

[hc.SelectionModel](hc.SelectionModel.html)

See:

*   [getSelectionModel](hc.graph.GraphView.html#getSelectionModel)

#### toCanvas(background) → {htmlCanvasElement}

将拓扑导出为canvas

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp; Description  
`background`&emsp;&emsp;&emsp;&emsp;color&emsp;&emsp;背景色

##### Returns:

htmlCanvasElement

#### toDataURL(background, type, zoom) → {String}

将拓扑导出为base64格式字符串

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`background`&emsp;&emsp;color&emsp;&emsp;&emsp; \<optional> &emsp;&emsp;背景色  
`type`&emsp;&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp; \<optional> &emsp;&emsp;图片类型 image/jpeg | image/png  
`zoom`&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp; \<optional> &emsp;&emsp;缩放比例


##### Returns:

String

#### translate(x, y, anim)

在当前值基础上增加水平和垂直平移值

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`x`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;新增的水平平移值  
`y`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;新增的垂直平移值  
`anim`&emsp;&emsp;Boolean&emsp;&emsp; \<optional> &emsp;&emsp;是否使用动画


#### tx(value)

获取或设置水平平移值，没有参数时相当于[getTranslateX](hc.graph.GraphView.html#getTranslateX)，有参数时相当于[setTranslateX](hc.graph.GraphView.html#setTranslateX)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`value`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移值  

#### ty(value)

获取或设置垂直平移值，没有参数时相当于[getTranslateY](hc.graph.GraphView.html#getTranslateY)，有参数时相当于[setTranslateY](hc.graph.GraphView.html#setTranslateY)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`value`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;平移值  

#### umi(listener, scope)

删除交互事件监听器，[removeInteractorListener](hc.graph.GraphView.html#removeInteractorListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [removeInteractorListener](hc.graph.GraphView.html#removeInteractorListener)

#### ump(listener, scope)

删除自身属性变化事件监听器，[removePropertyChangeListener](hc.graph.GraphView.html#removePropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [removePropertyChangeListener](hc.graph.GraphView.html#removePropertyChangeListener)

#### upSubGraph()

进入上一级子网

#### validate()

立刻刷新拓扑

#### zoomIn(anim, point)

放大拓扑

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description  
`anim`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;\<optional>&emsp;&emsp;是否使用动画   
`point`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;缩放中心点的坐标

##### Example

    graphView.zoomIn(true, {x: 0, y: 0});

#### zoomOut(anim, point)

缩小拓扑

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description  
`anim`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;\<optional>&emsp;&emsp;是否使用动画   
`point`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;缩放中心点的坐标

##### Example

    graphView.zoomOut(true, {x: 0, y: 0});

#### zoomReset(anim, point)

将拓扑缩放值改为1

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;Description  
`anim`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;\<optional>&emsp;&emsp;是否使用动画   
`point`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;缩放中心点的坐标

