
#### new TouchInteractor(graphView, params)

实现触摸屏上Touch交互

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description 
`graphView`&emsp;&emsp;[hc.graph.GraphView](hc.graph.GraphView.html)&emsp;&emsp;绑定拓扑组件  
`params`&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;交互参数 

##### Example

    //params参数格式：
    {
    	selectable: true|false,//是否启用选择功能
    	movable: true|false,//是否启用移动功能
    	pannable: true|false,//是否启用pan功能
    	pinchable: true|false,//是否启用双指pinch缩放
    	editable: true|false,//是否启用编辑功能
    }

### Extends

*   [hc.graph.Interactor](hc.graph.Interactor.html)
