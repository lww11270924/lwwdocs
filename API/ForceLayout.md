
#### new ForceLayout(modelOrView, options)

提供2D弹力布局，即3D的xz面布局，构造函数可传入DataModel、GraphView和Graph3dView三种参数  
使用需引入 hc-forcelayout.js

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`modelOrView`&emsp;&emsp;[hc.graph.GraphView](hc.graph.GraphView.html) | [hc.graph3d.Graph3dView](hc.graph3d.Graph3dView.html) | [hc.DataModel](hc.DataModel.html)&emsp;&emsp;&emsp;拓扑组件或者数据容器  
`options`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;选项, 目前选项有：gap布局间距、hgap横向布局间距、vgap纵向布局间距。

### Methods

#### setEdgeRepulsion(nodeRepulsion)

改变节点间斥力，值越大连线节点间斥力越大，连线节点布局越分散。

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; Type&emsp;&emsp;&emsp;&emsp;Description    
`nodeRepulsion`&emsp;&emsp;Number&emsp;&emsp;0~1 

#### setNodeRepulsion(nodeRepulsion)

改变节点间斥力，值越大节点间斥力越大，节点布局越分散。

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; Type&emsp;&emsp;&emsp;&emsp;Description    
`nodeRepulsion`&emsp;&emsp;Number&emsp;&emsp;0~1 

#### start()

启动弹力布局

#### stop()

停止弹力布局
