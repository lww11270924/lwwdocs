[hc](API/hc.md).Block()
---
> <h3>new Block()</h3>
> 块节点类型，本身不绘制任何内容，用于作为其它的父节点，可以与子节点同步大小，当它隐藏|显示时，所有孩子节点都会跟着隐藏|显示
### <font color="#F17DA4">Extends</font>  
---
&emsp;&emsp;<font color=Blue>[hc.Node](API/Node.md)</font>  
### <font color="#F17DA4">Methods</font>  
---
#### <b>a</b>(name, value) → {Object}  
获取或设置attr属性，仅有一个参数时相当于[getAttr](API/Data.md#getAttr)，有两个参数时相当于[setAttr](API/Data.md#setAttr)
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Attributes</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">name</td>
                <td>    
                    <span style="color:#aaa">String</span>       
                </td>      
                    <td>         
                    </td>
                <td><p>属性名</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">value</td>
                <td>    
                    <span style="color:#aaa">Object</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td><p>属性值</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#a](API/Data.md#a)</font>  
#### <b>addChild</b>(child, index)
添加孩子节点，index为孩子插入索引，为空则插入作为最后的孩子，内部会自动调用child的setParent
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Attributes</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">child</td>
                <td>    
                    <span style="color:#aaa" >hc.Data</span>       
                </td>      
                    <td>         
                    </td>
                <td><p>孩子元素</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">index</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td><p>插入索引</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#addChild](API/Data.md#addChild)</font>  

#### <b>addStyleIcon</b>(name, icon)

增加icon，icon参数请参考beginner guide
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">name</td>
                <td>    
                    <span style="color:#aaa">String</span>       
                </td>      
                <td><p>icon名</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">icon</td>
                <td>    
                    <span style="color:#aaa">Object</span>       
                </td>      
                <td><p>icon参数</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#addStyleIcon](API/Data.md#addStyleIcon)</font>  

##### Example
```
data.addStyleIcon("arrow1", {
    position: 2,
    width: 50,
    heighc: 25,
    keepOrien: true,
    names: ['arrow']
});
```
#### <b>clearChildren()</b>

删除所有孩子节点，内部会自动调用setParent  
Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#clearChildren](API/Data.md#clearChildren)</font>  

#### <b>dm()</b> → {[hc.DataModel](API/DataModel.md)}

获取[DataModel](hc.DataModel.md)，[getDataModel](API/Data.md#getDataModel)的缩写

##### Returns:

&emsp;&emsp;[hc.DataModel](API/DataModel.md) - dataModel

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#dm](API/Data.md#dm)</font> 

#### <b>eachChild</b>(func, scope)

遍历孩子元素
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr style="color:#1F1F1F">
                <th>Name</th>
                <th>Type</th>
                <th>Attributes</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">func</td>
                <td>    
                    <span style="color:#aaa">function</span>       
                </td>      
                    <td>         
                    </td>
                <td style="color:#333"><p>遍历函数</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">scope</td>
                <td>    
                    <span style="color:#aaa">Object</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>函数域</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#eachChild](API/Data.md#eachChild)</font>

#### Example
```
data.eachChild(function(child) {
    console.log(child.getId());
});
```
#### <b>firePropertyChange</b>(property, oldValue, newValue)
派发属性变化事件
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr style="color:#1F1F1F">
                <th>Name</th>
                <th>Type</th>
                <th>Attributes</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">property</td>
                <td>    
                    <span style="color:#aaa">String</span>       
                </td>      
                    <td>         
                    </td>
                <td style="color:#333"><p>属性名</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">oldValue</td>
                <td>    
                    <span style="color:#aaa">Object</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>旧值</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">newValue</td>
                <td>    
                    <span style="color:#aaa">Object</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>新值</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#firePropertyChange](API/Data.md#firePropertyChange)</font>

#### <b>fp</b>(property, oldValue, newValue)

派发属性变化事件，同[firePropertyChange](API/Data.md#firePropertyChange)
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr style="color:#1F1F1F">
                <th>Name</th>
                <th>Type</th>
                <th>Attributes</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">property</td>
                <td>    
                    <span style="color:#aaa">String</span>       
                </td>      
                    <td>         
                    </td>
                <td style="color:#333"><p>属性名</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">oldValue</td>
                <td>    
                    <span style="color:#aaa">Object</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>旧值</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">newValue</td>
                <td>    
                    <span style="color:#aaa">Object</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>新值</p></td>
            </tr>
        </tbody>
    </table>
</div> 

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#fp](API/Data.md#fp)</font>

#### <b>getAgentEdges()</b> → {[hc.List](API/List.md)}

获取当前图元代理的连线集合

#### Returns:

&emsp;&emsp;[hc.List](API/List.md)

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getAgentEdges](API/Node.md#getAgentEdges)</font>

#### getAttaches() → {[hc.List](API/List.md)}

获取吸附到自身的所有图元

#### Returns:

&emsp;&emsp;[hc.List](API/List.md)

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getAttaches](API/Node.md#getAttaches)</font>

#### <b>getAttr</b>(name)</b> → {Object}

获取attr属性
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">property</td>
                <td>    
                    <span style="color:#aaa">Type</span>       
                </td>      
                <td><p>属性名</p></td>
            </tr>
        </tbody>
    </table>
</div>
#### Returns:

&emsp;&emsp;Object

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getAttr](API/Data.md#getAttr)</font>
#### <b>getAttrObject()</b> → {Object}

获取attr属性对象，该属性默认为空，用于存储用户业务信息

##### Returns:

&emsp;&emsp;Object - attr属性对象

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getAttrObject](API/Data.md#getAttrObject)</font>
#### <b>getChildAt</b>(index) → {[hc.Data](API/Data.md)}

返回指定索引位置的孩子
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">index</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>索引</p></td>
            </tr>
        </tbody>
    </table>
</div>
#### Returns:

&emsp;&emsp;[hc.Data](API/Data.md) - 索引对应的孩子

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getChildAt](API/Data.md#getChildAt)</font>

#### <b>getChildren()</b> → {[hc.List](API/List.md)}

获取所有孩子节点

##### Returns:

&emsp;&emsp;[hc.List](API/List.md) - 孩子元素集合

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getChildren](PAI/Data.md#getChildren)</font>
#### <b>getClass()</b> → {function}

获取类声明(构造函数)

##### Returns:

&emsp;&emsp;function - 类声明(构造函数)

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getClass](API/Data.md#getClass)</font>

#### <b>getClassName()</b> → {String}

获取类全名，继承Data并希望序列化时应该重写此方法返回子类的类名字符串

#### Returns:

&emsp;&emsp;String - 类全名

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getClassName](API/Data.md#getClassName)</font>  
See:  
&emsp;&emsp;<font color=Blue>[hc.Data#getSuperClass](API/Data.md#getSuperClass)</font> 

#### <b>getCorners</b>(xPadding, yPadding) → {Array}

获取图元四个角的实时坐标(包括旋转后的坐标)
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">xPadding</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>水平方向padding</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">yPadding</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>垂直方向padding</p></td>
            </tr>
        </tbody>
    </table>
</div>

#### Returns:

&emsp;&emsp;Array - 四个角坐标，顺序为左上，右上，右下，左下

Inherited From:
&emsp;&emsp;<font color=Blue>[hc.Node#getCorners](API/Node.md#getCorners)</font> 

##### Example

    //返回值示例：
    [
    {x: 0, y: 0},//左上
    {x: 100, y: 0},//右上
    {x: 100, y: 100},//右下
    {x: 0, y: 100}//左下
    ]

#### <b>getDataModel()</b> → {[hc.DataModel](API/DataModel.md)}

获取所属的DataModel

#### Returns:

&emsp;&emsp;[hc.DataModel](API/DataModel.md) - DataModel数据容器

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getDataModel](API/Data.md#getDataModel)</font>

#### <b>getDisplayName()</b> → {String}

获取显示名称，常作为Column和Property的列头和属性名称显示

##### Returns:

&emsp;&emsp;String - 显示名称

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getDisplayName](API/Data.md#getDisplayName)</font>  
#### <b>getEdges()</b> → {[hc.List](API/List.md)}

获取所有跟图元关联的连线(不包括代理的连线)

##### Returns:

&emsp;&emsp;[hc.List](API/List.md)

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getEdges](API/Node.md#getEdges)</font>  

#### <b>getElevation()</b> → {Number}

获取图元中心在3D坐标系中的y坐标

##### Returns:

&emsp;&emsp;Number

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getElevation](API/Node.md#getElevation)</font> 

#### <b>getHeighc()</b> → {Number}

获取图元在2D拓扑中的高度，或3D拓扑中的z轴长度

##### Returns:

&emsp;&emsp;Number

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getHeighc](API/Node.md#getHeighc)</font> 

#### <b>getHost()</b> → {[hc.Data](API/Data.md)}

获取宿主图元，当图元吸附上宿主图元时，宿主移动或旋转时会带动所有吸附者

##### Returns:
&emsp;&emsp;<font color=Blue>[hc.Data](API/Data.md)</font> 

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getHost](API/Node.md#getHost)</font>

#### <b>getIcon()</b> → {String|Object}

获取小图标名称，常作为TreeView和ListView等组件上的节点小图标

##### Returns:

&emsp;&emsp;String | Object - 图标名或矢量

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getIcon](API/Data.md#getIcon)</font>

#### <b>getId()</b> → {Number}

获取唯一编号

##### Returns:

&emsp;&emsp;Number - 唯一编号

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getId](API/Data.md#getId)</font>

#### <b>getImage()</b> → {[hc.Data](API/Data.md)}

获取拓扑上展现的图片信息，在GraphView拓扑图中图片一般以position为中心绘制

##### Returns:
&emsp;&emsp;<font color=Blue>[hc.Data](API/Data.md)</font>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getImage](API/Node.md#getImage)</font>

#### <b>getLayer()</b> → {String|Number}

获取数据元素在GraphView组件中的图层位置

##### Returns:

&emsp;&emsp;String | Number - 图层名

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getLayer](API/Data.md#getLayer)</font>
 
Default Value:

*   0

#### <b>getLoopedEdges()</b> → {[hc.List](API/List.md)}

获取所有跟节点关联的自环连线

##### Returns:
&emsp;&emsp;[hc.List](API/List.md)

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getLoopedEdges](API/Node.md#getLoopedEdges)</font>

#### <b>getName()</b> → {String}

获取数据元素名

##### Returns:

&emsp;&emsp;String - 名称

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getName](API/Data.md#getName)</font>

#### <b>getParent()</b> → {[hc.Data](API/Data.md)}

获取父元素

##### Returns:

[hc.Data](API/Data.md) - 父元素

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getParent](API/Data.md#getParent)</font>

#### <b>getPosition()</b> → {Object}

获取图元中心点坐标

##### Returns:

&emsp;&emsp;Object

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getPosition](API/Node.md#getPosition)</font>

##### Example

    //返回值示例：
    {
    	x: 0,
    	y: 0
    }

#### <b>getPosition3d()</b> → {Array}

获取图元中心点在3D拓扑中的三维坐标

##### Returns:

&emsp;&emsp;Array - 三维坐标数组，格式为\[x, y, z\]

Inherited From:
&emsp;&emsp;<font color=Blue>[hc.Node#getPosition3d](API/Node.md#getPosition3d)</font>

#### <b>getRect()</b> → {Object}

获取图元的矩形区域(包括旋转)

##### Returns:

&emsp;&emsp;Object - 矩形区域

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getRect](API/Node.md#getRect)</font>

##### Example

    //返回值示例：
    {x: 0, y: 0, width: 100, heighc: 100}

#### <b>getRotation()</b> → {Number}

获取图元的旋转角度，围绕中心点顺时针旋转

##### Returns:

&emsp;&emsp;Number - 旋转角度(弧度制)

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getRotation](API/Node.md#getRotation)</font>

#### <b>getRotation3d()</b> → {Array}

获取图元在3D拓扑中的三维旋转角度

##### Returns:

&emsp;&emsp;Array - 三维旋转角度(弧度制)，格式为\[x, y, z\]，即\[getRotationX(), -getRotation(), getRotationZ()\]

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getRotation3d](API/Node.md#getRotation3d)</font>

#### <b>getRotationMode()</b> → {String}

返回三维旋转模式  
  
图元在3D拓扑中旋转时，先沿x轴旋转，再沿y轴旋转和先沿y轴旋转，再沿x轴旋转最后的结果是不一样的

##### Returns:

&emsp;&emsp;String - 三维旋转模式，xyz|xzy|yxz|yzx|zxy|zyx

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getRotationMode](API/Node.md#getRotationMode)</font>

See:  
&emsp;&emsp;<font color=Blue>[setRotationMode](API/Node.md#setRotationMode)</font>

#### getRotationX() → {Number}

获取图元在3d拓扑中沿x轴的旋转角度(弧度制)

##### Returns:

&emsp;&emsp;Number

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getRotationX](API/Node.md#getRotationX)</font>

#### getRotationY() → {Number}

获取图元在3d拓扑中沿y轴的旋转角度(弧度制)

##### Returns:

&emsp;&emsp;Number

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getRotationY](API/Node.md#getRotationY)</font>

#### getRotationZ() → {Number}

获取图元在3d拓扑中沿z轴的旋转角度(弧度制)

##### Returns:

&emsp;&emsp;Number

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getRotationZ](API/Node.md#getRotationZ)</font>

#### getScale() → {Object}

获取图元在2D拓扑中的缩放值

##### Returns:

&emsp;&emsp;Object

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getScale](API/Node.md#getScale)</font>

##### Example

    //返回值示例：
    {
    	x: 1,
    	y: 1
    }

#### getScale3d() → {Array}

获取图元在3D拓扑中的缩放值

##### Returns:

&emsp;&emsp;Array - 格式为\[x, y, z\]，即\[getScaleX(), getScaleTall(), getScaleY()\]

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getScale3d](API/Node.md#getScale3d)</font>

#### getScaleTall() → {Number}

获取图元在3D拓扑中y轴方向的缩放值

##### Returns:

&emsp;&emsp;Number - y轴方向缩放值

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getScaleTall](API/Node.md#getScaleTall)</font>

#### getScaleX() → {Number}

获取图元在2D拓扑中x轴方向的缩放值

##### Returns:

&emsp;&emsp;Number - x轴方向缩放值

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getScaleX](API/Node.md#getScaleX)</font>

#### getScaleY() → {Number}

设置图元在2D拓扑中y轴方向的缩放值

##### Returns:

&emsp;&emsp;Number - y轴方向缩放值

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getScaleY](API/Node.md#getScaleY)</font>

#### getSerializableAttrs() → {Object}

此函数返回一个map，决定序列化时哪些attr属性可被序列化，默认所有attr对象里的属性都会被序列化

##### Returns:

&emsp;&emsp;Object - 需要被序列化的attr属性map

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getSerializableAttrs](API/Data.md#getSerializableAttrs)</font>

##### Example

    function(){
        var name, map = {};
        for (name in this._attrObject) {
            map[name] = 1;
        }
        return map;
    }

#### getSerializableProperties() → {Object}

此函数返回一个map，决定序列化时哪些属性可被序列化，如果有自定义的get/set属性并且需要序列化，应该重写此方法

##### Returns:

&emsp;&emsp;Object - 需要被序列化的属性map

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getSerializableProperties](API/Data.md#getSerializableProperties)</font>

##### Example

    function(){
        return {
            name: 1,
            displayName: 1,
            icon: 1,
            toolTip: 1,
            parent: 1,
            layer: 1,
            tag: 1,
            adjustChildrenToTop: 1
        };
    }

#### getSerializableStyles() → {Object}

此函数返回一个map，决定序列化时哪些样式可被序列化，默认所有样式都会被序列化

##### Returns:

&emsp;&emsp;Object - 需要被序列化的样式map

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getSerializableStyles](API/Data.md#getSerializableStyles)</font>
##### Example

    function(){
        var name, map = {};
        for (name in this._styleMap) {
            map[name] = 1;
        }
        return map;
    }

#### getSize() → {Object}

获取图元在2D拓扑中的尺寸(宽高)

##### Returns:

&emsp;&emsp;Object

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getSize](API/Node.md#getSize)</font>

##### Example

    //返回值示例：
    {
    	with: 100,
    	heighc: 100
    }

#### getSize3d() → {Array}

获取图元在3D拓扑中的尺寸(长宽高)

##### Returns:

&emsp;&emsp;Array - 格式为\[x, y, z\]，即\[getWidth(), getTall(), getHeighc()\]

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getSize3d](API/Node.md#getSize3d)</font> 

#### getSourceAgentEdges() → {[hc.List](API/List.md)}

获取代理的起始于该图元的连线

##### Returns:

[hc.List](API/List.md)

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getSourceAgentEdges](API/Node.md#getSourceAgentEdges)</font> 
#### getSourceEdges() → {[hc.List](API/List.md)}

获取跟图元关联的并起始于该图元的连线(不包括代理的连线)

##### Returns:

&emsp;&emsp;[hc.List](API/List.md)

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getSourceEdges](API/Node.md#getSourceEdges)</font> 

#### getStyle(name) → {Object}

获取样式属性
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">name</td>
                <td>    
                    <span style="color:#aaa">String</span>       
                </td>      
                <td><p>样式名</p></td>
            </tr>
        </tbody>
    </table>
</div>

#### Returns:

&emsp;&emsp;Object

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getStyle](API/Data.md#getStyle)</font> 

#### getStyleMap() → {Object}

获取图元内部样式映射信息

##### Returns:

&emsp;&emsp;Object - 样式映射表

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getStyleMap](API/Data.md#getStyleMap)</font> 

#### getSuperClass() → {function}

获取父类声明(构造函数)，继承类时可以用来调用父类构造或函数

##### Returns:

&emsp;&emsp;function - 父类声明(构造函数)

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getSuperClass](API/Data.md#getSuperClass)</font> 

##### Example

    function MyNode() {
         this.getSuperClass().call(this);//调用父类构造函数
    }
    hc.Default.def(MyNode, hc.Data, {
       setName: function(name) {
       	this.getSuperClass().prototype.setName.call(this, name);//调用父类的setName函数
       	this._username = name;
       }
    });

#### getTag() → {String}

获取标识号，可通过[getDataByTag](API/DataModel.md#getDataByTag)快速查找

##### Returns:

&emsp;&emsp;String - 标识号

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getTag](API/Data.md#getTag)</font> 

#### getTall() → {Number}

获取图元在3D拓扑中的y轴长度

##### Returns:

&emsp;&emsp;Number

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getTall](API/Node.md#getTall)</font> 

#### getTargetAgentEdges() → {[hc.List](API/List.md)}

获取图元代理的结束于该图元的连线

##### Returns:

&emsp;&emsp;[hc.List](API/List.md)

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getTargetAgentEdges](API/Node.md#getTargetAgentEdges)</font> 

#### getTargetEdges() → {[hc.List](API/List.md)}

获取跟图元关联的并结束于该图元的连线(不包括代理的连线)

##### Returns:

&emsp;&emsp;[hc.List](API/List.md)

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getTargetEdges](API/Node.md#getTargetEdges)</font> 

#### getToolTip() → {String}

获取文字提示信息

##### Returns:

&emsp;&emsp;String - 文字提示

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getToolTip](API/Data.md#getToolTip)</font> 

#### getUIClass() → {function}

获取拓扑组件上的UI类

##### Returns:

&emsp;&emsp;function - UI类声明(构造函数)

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#getUIClass](API/Data.md#getUIClass)</font> 

#### getWidth() → {Number}

获取图元在2D拓扑中的宽度，或在3D拓扑中x轴的长度

##### Returns:

&emsp;&emsp;Number

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#getWidth](API/Node.md#getWidth)</font> 

#### handleHostPropertyChange(event)

当吸附宿主对象属性发生变化时回调该函数，可重载做后续处理
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">event</td>
                <td>    
                    <span style="color:#aaa">Event</span>       
                </td>      
                <td><p>事件对象</p></td>
            </tr>
        </tbody>
    </table>
</div> 

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#handleHostPropertyChange](API/Node.md#handleHostPropertyChange)</font> 

#### hasAgentEdges() → {Boolean}

判断当前图元上是否有代理连线

##### Returns:

&emsp;&emsp;Boolean

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#hasAgentEdges](API/Node.md#hasAgentEdges)</font> 

#### hasChildren() → {Boolean}

判断是否有孩子

##### Returns:

&emsp;&emsp;Boolean - 是否有孩子

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#hasChildren](API/Data.md#hasChildren)</font> 

#### invalidate()

强制触发属性变化事件通知界面更新

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#invalidate](API/Data.md#invalidate)</font> 

#### isAdjustChildrenToTop() → {Boolean}

GraphView点击图元会自动sendToTop，该属性决定是否对子图元也进行sendToTop操作

##### Returns:

&emsp;&emsp;Boolean - 是否将children自动sendToTop

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#isAdjustChildrenToTop](API/Data.md#isAdjustChildrenToTop)</font> 

#### isClickThroughEnabled() → {Boolean}

获取块节点是否可以点击穿透

##### Returns:

&emsp;&emsp;Boolean

#### isDescendantOf(data) → {Boolean}

判断自身是否为指定data的子孙
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">data</td>
                <td>    
                    <span style="color:#aaa">hc.Data</span>       
                </td>      
                <td><p>要对比的数据元素</p></td>
            </tr>
        </tbody>
    </table>
</div> 

##### Returns:

&emsp;&emsp;Boolean - 自身是否为指定data的子孙

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#isDescendantOf](API/Data.md#isDescendantOf)</font> 

#### isEmpty() → {Boolean}

判断是否有孩子，同[hasChildren](API/Data.md#hasChildren)

##### Returns:

&emsp;&emsp;Boolean - 是否有孩子

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#isEmpty](API/Data.md#isEmpty)</font> 

#### isHostOn(node) → {Boolean}

判断当前图元是否吸附到指定图元对象上
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">node</td>
                <td>    
                    <span style="color:#aaa">hc.Node</span>       
                </td>      
                <td><p>指定的图元</p></td>
            </tr>
        </tbody>
    </table>
</div> 

#### Returns:
&emsp;&emsp;Boolean

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#isHostOn](API/Node.md#isHostOn)</font> 

#### isParentOf(data) → {Boolean}

判断自身是否为指定data的父亲
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">data</td>
                <td>    
                    <span style="color:#aaa">hc.Data</span>       
                </td>      
                <td><p>要对比的数据元素</p></td>
            </tr>
        </tbody>
    </table>
</div> 

#### Returns:
&emsp;&emsp;Boolean - 自身是否为指定data的父亲

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#isParentOf](API/Data.md#isParentOf)</font> 

#### isRelatedTo(data) → {Boolean}

判断自身与指定data是否有父子或子孙关系
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">data</td>
                <td>    
                    <span style="color:#aaa">hc.Data</span>       
                </td>      
                <td><p>要对比的数据元素</p></td>
            </tr>
        </tbody>
    </table>
</div> 

#### Returns:

&emsp;&emsp;Boolean - 自身与指定data是否有父子或子孙关系

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#isRelatedTo](API/Data.md#isRelatedTo)</font> 

#### isSyncSize() → {Boolean}

获取块节点是否同步子节点大小

##### Returns:

&emsp;&emsp;Boolean

#### iv()

强制触发属性变化事件通知界面更新，[invalidate](API/Data.md#invalidate)的缩写

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#iv](API/Data.md#iv)</font> 

#### onChildAdded(child, index)

添加孩子时的回调函数，可重载做后续处理
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">child</td>
                <td>    
                    <span style="color:#aaa">hc.Data</span>       
                </td>      
                <td><p>新增加的孩子元素</p></td>
            </tr>
             <tr>  
                <td style="color:#F17DA4">index</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>索引</p></td>
            </tr>
        </tbody>
    </table>
</div> 

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#onChildAdded](API/Data.md#onChildAdded)</font> 

#### onChildRemoved(child, index)

删除孩子时的回调函数，可重载做后续处理
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">child</td>
                <td>    
                    <span style="color:#aaa">hc.Data</span>       
                </td>      
                <td><p>被删除的孩子元素</p></td>
            </tr>
             <tr>  
                <td style="color:#F17DA4">index</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>索引</p></td>
            </tr>
        </tbody>
    </table>
</div> 

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#onChildRemoved](API/Data.md#onChildRemoved)</font> 

#### onHostChanged(oldHost, newHost)

当吸附的宿主对象发生变化时回调该函数，可重载做后续处理
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">oldHost</td>
                <td>    
                    <span style="color:#aaa">hc.Node</span>       
                </td>      
                <td><p>旧的宿主</p></td>
            </tr>
             <tr>  
                <td style="color:#F17DA4">newHost</td>
                <td>    
                    <span style="color:#aaa">hc.Node</span>       
                </td>      
                <td><p>新的宿主</p></td>
            </tr>
        </tbody>
    </table>
</div> 

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#onHostChanged](API/Node.md#onHostChanged)</font> 
#### onParentChanged(oldParent, parent)

改变父亲元素时的回调函数，可重载做后续处理
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">oldParent</td>
                <td>    
                    <span style="color:#aaa">hc.Data</span>       
                </td>      
                <td><p>旧的父元素</p></td>
            </tr>
             <tr>  
                <td style="color:#F17DA4">parent</td>
                <td>    
                    <span style="color:#aaa">hc.Data</span>       
                </td>      
                <td><p>新的父元素</p></td>
            </tr>
        </tbody>
    </table>
</div> 

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#onParentChanged](API/Data.md#onParentChanged)</font> 

#### onPropertyChanged(event)

属性变化回调函数，可重载做后续处理
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">event</td>
                <td>    
                    <span style="color:#aaa">Object</span>       
                </td>      
                <td><p>属性变化事件</p></td>
            </tr>
        </tbody>
    </table>
</div> 

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#onPropertyChanged](API/Data.md#onPropertyChanged)</font> 

##### Example

    //event格式：
    {
    	property: 'name',//发生变化的属性
    	oldValue: 'oldValue',//旧值
    	newValue: 'newValue',''新值
    	data: data//发生变化的data
    }

#### onStyleChanged(name, oldValue, newValue)

样式属性变化时会回调该函数，可重载做后续处理
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">name</td>
                <td>    
                    <span style="color:#aaa">String</span>       
                </td>      
                <td><p>样式名</p></td>
            </tr>
             <tr>  
                <td style="color:#F17DA4">oldValue</td>
                <td>    
                    <span style="color:#aaa">Object</span>       
                </td>      
                <td><p>旧的样式值</p></td>
            </tr>
             <tr>  
                <td style="color:#F17DA4">newValue</td>
                <td>    
                    <span style="color:#aaa">Object</span>       
                </td>      
                <td><p>新的样式值</p></td>
            </tr>
        </tbody>
    </table>
</div> 

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#onStyleChanged](API/Data.md#onStyleChanged)</font> 

#### p(x, y) → {Object}

获取或设置设置图元中心点坐标，有参数时相当于[setPosition](hc.Node.md#setPosition)，没有参数时相当于[getPosition](hc.Node.md#getPosition)
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr style="color:#1F1F1F">
                <th>Name</th>
                <th>Type</th>
                <th>Attributes</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">x</td>
                <td>    
                    <span style="color:#aaa">Number | Obejct</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>单个参数时，为 {x ,y} 对象，两个参数时为 x 坐标</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">y</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>y坐标</p></td>
            </tr>
        </tbody>
    </table>
</div>

#### Returns:
&emsp;&emsp;Object - 坐标值，格式为:{x: x, y: y}

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#p](API/Node.md#p)</font>   
See:  
&emsp;&emsp;<font color=Blue>[setPosition](API/Node.md#setPosition)</font> 

#### p3(x, y, z) → {Array}

获取或设置图元中心点在3D拓扑中的三维坐标，有三个参数时相当于[setPosition3d](API/Node.md#setPosition3d)，没有参数时相当于[getPosition3d](API/Node.md#getPosition3d)
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr style="color:#1F1F1F">
                <th>Name</th>
                <th>Type</th>
                <th>Attributes</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">x</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>x坐标</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">y</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>y坐标</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">z</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>z坐标</p></td>
            </tr>
        </tbody>
    </table>
</div>

#### Returns:

&emsp;&emsp;Array - 三维坐标数组，格式为\[x, y, z\]

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#p3](API/Node.md#p3)</font> 

See:  
&emsp;&emsp;<font color=Blue>[setPosition3d](API/Node.md#setPosition3d)</font> 

#### r3(rotationX, rotationY, rotationZ) → {Array}

获取或设置图元在3D拓扑中的三维旋转角度，有三个参数时相当于[setRotation3d](API/Node.md#setRotation3d)，没有参数时相当于[getRotation3d](API/Node.md#getRotation3d)
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr style="color:#1F1F1F">
                <th>Name</th>
                <th>Type</th>
                <th>Attributes</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">rotationX</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>沿x轴的旋转角度(弧度制)</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">rotationY</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>沿y轴的旋转角度(弧度制)</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">rotationZ</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>沿z轴的旋转角度(弧度制)</p></td>
            </tr>
        </tbody>
    </table>
</div>

#### Returns:  
&emsp;&emsp;Array - 三维旋转角度(弧度制)，格式为\[x, y, z\]，即\[getRotationX(), -getRotation(), getRotationZ()\]

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#r3](API/Node.md#r3)</font> 

See:  
&emsp;&emsp;<font color=Blue>[setRotation3d](API/Node.md#setRotation3d)</font> 

#### removeChild(child)

删除指定孩子元素，内部会自动调用孩子元素的setParent

##### Parameters:
>Name &emsp;Type&emsp;Description  
`child`&emsp; [hc.Data](API/Data.md)&emsp;要删除的孩子元素  

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#removeChild](API/Data.md#removeChild)</font> 

#### removeStyleIcon(name)

删除icon
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">name</td>
                <td>    
                    <span style="color:#aaa">String</span>       
                </td>      
                <td><p>要删除的icon名</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#removeStyleIcon](API/Data.md#removeStyleIcon)</font> 

#### rotateAt(x, y, angle)

以指定的坐标为中心旋转图元
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">x</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>指定x坐标</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">y</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>指定y坐标</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">angle</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>旋转角度(弧度制)</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#rotateAt](API/Node.md#rotateAt)</font> 

#### s(name, value) → {Object}

获取或设置样式，仅有一个参数时相当于[getStyle](API/Data.md#getStyle)，有两个参数时相当于[setStyle](API/Data.md#setStyle)
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr style="color:#1F1F1F">
                <th>Name</th>
                <th>Type</th>
                <th>Attributes</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">name</td>
                <td>    
                    <span style="color:#aaa">String</span>       
                </td>      
                    <td>         
                    </td>
                <td style="color:#333"><p>样式名</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">value</td>
                <td>    
                    <span style="color:#aaa">Object</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>样式值</p></td>
            </tr>
        </tbody>
    </table>
</div>

#### Returns:

&emsp;&emsp;Object

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#s](API/Data.md#s)</font> 

#### s3(width, tall, heighc) → {Array}

获取或设置图元在3D拓扑中的尺寸，有三个参数时相当于[setSize3d](API/Node.md#setSize3d)，没有参数时相当于[getSize3d](API/Node.md#getSize3d)
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">width</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>x轴方向的长度</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">tall</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y轴方向的长度</p></td>
            </tr>
             <tr>  
                <td style="color:#F17DA4">heighc</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>z轴方向的长度</p></td>
            </tr>
        </tbody>
    </table>
</div>

#### Returns:

&emsp;&emsp;Array - 格式为\[x, y, z\]，即\[getWidth(), getTall(), getHeighc()\]  

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#s3](API/Node.md#s3)</font> 

See:  
&emsp;&emsp;<font color=Blue>[setSize3d](API/Node.md#setSize3d)</font>  

#### setAdjustChildrenToTop(adjustToTop)

GraphView点击图元会自动sendToTop，该属性决定是否对子图元也进行sendToTop操作
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">adjustToTop</td>
                <td>    
                    <span style="color:#aaa">Boolean</span>       
                </td>      
                <td><p>是否将children自动sendToTop</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#setAdjustChildrenToTop](API/Data.md#setAdjustChildrenToTop)</font>

#### setAnchor(x, y)

设置图元中心点
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">x</td>
                <td>    
                    <span style="color:#aaa">Number | Object</span>       
                </td>      
                <td><p>x轴方向的中心点比例，当仅有一个参数时，可为 {x: 0, y: 0} 的对象格式</p></td>
            </tr>
             <tr>  
                <td style="color:#F17DA4">y</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y轴方向的中心点比例</p></td>
            </tr>
        </tbody>
    </table>
</div>  

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setAnchor](API/Node.md#setAnchor)</font>

#### setAnchor3d(x, y, z)

设置图元在3D坐标系中的中心点
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">x</td>
                <td>    
                    <span style="color:#aaa">Number | Array</span>       
                </td>      
                <td><p>x轴方向的中心点比例，当仅有一个参数时，可为 \[x, y, z\] 的数组格式</p></td>
            </tr>
             <tr>  
                <td style="color:#F17DA4">y</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y轴方向的中心点比例</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">z</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>z轴方向的中心点比例</p></td>
            </tr>
        </tbody>
    </table>
</div>  

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setAnchor3d](API/Node.md#setAnchor3d)</font>

#### setAnchorElevation(y)

设置图元在3D坐标系中的y轴方向的中心点比例
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">y</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y轴方向的中心点比例</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setAnchorElevation](API/Node.md#setAnchorElevation)</font>
#### setAnchorX(x)

设置图元x轴方向的中心点比例
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">x</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>x轴方向的中心点比例</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setAnchorX](API/Node.md#setAnchorX)</font>

#### setAnchorY(y)

设置图元y轴方向的中心点比例
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">y</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y轴方向的中心点比例</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setAnchorY](API/Node.md#setAnchorY)</font>

#### setAttr(name, value)

设置attr属性
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">name</td>
                <td>    
                    <span style="color:#aaa">String</span>       
                </td>      
                <td><p>属性名</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">value</td>
                <td>    
                    <span style="color:#aaa">Object</span>       
                </td>      
                <td><p>属性值</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#setAttr](API/Data.md#setAttr)</font>

#### setAttrObject(attrObject)

设置attr属性对象，该属性默认为空，用于存储用户业务信息
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">attrObject</td>
                <td>    
                    <span style="color:#aaa">Object</span>       
                </td>      
                <td><p>attr属性对象</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#setAttrObject](API/Data.md#setAttrObject)</font>

#### setClickThroughEnabled(clickThroughEnabled)

设置块节点是否可以点击穿透（选中 block 前提下，再次点击可以选中子节点）
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">clickThroughEnabled</td>
                <td>    
                    <span style="color:#aaa">Boolean</span>       
                </td>      
                <td></td>
            </tr>
        </tbody>
    </table>
</div>
#### setDisplayName(displayName)

设置显示名称，常作为Column和Property的列头和属性名称显示
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">displayName</td>
                <td>    
                    <span style="color:#aaa">String</span>       
                </td>      
                <td><p>显示名称</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#setDisplayName](API/Data.md#setDisplayName)</font>

#### setElevation(elevation)

设置图元中心在3D坐标系中的y坐标
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">elevation</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y轴方向的坐标值</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setElevation](API/Node.md#setElevation)</font>

#### setHeighc(heighc)

设置图元在2D拓扑中的高度，或3D拓扑中的z轴长度
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">heighc</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>2D拓扑中的高度，或3D拓扑中的z轴</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setHeighc](API/Node.md#setHeighc)</font>

#### setHost(data)

设置宿主图元，当图元吸附上宿主图元时，宿主移动或旋转时会带动所有吸附者
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">data</td>
                <td>    
                    <span style="color:#aaa">hc.Data</span>       
                </td>      
                <td><p>宿主图元</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setHost](API/Node.md#setHost)</font>
#### setIcon(icon)

设置小图标名称，常作为TreeView和ListView等组件上的节点小图标
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">icon</td>
                <td>    
                    <span style="color:#aaa">String | Object</span>       
                </td>      
                <td><p>图标名或矢量</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#setIcon](API/Data.md#setIcon)</font>

#### setId(id)

设置唯一编号，如果手工设置，一定要确保在data加入到DataModel之前设置并且唯一不重复
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">id</td>
                <td>    
                    <span style="color:#aaa">String | Number</span>       
                </td>      
                <td><p>唯一编号</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#setId](API/Data.md#setId)</font>

#### setImage(image)

设置拓扑上展现的图片信息，在GraphView拓扑图中图片一般以position为中心绘制
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">image</td>
                <td>    
                    <span style="color:#aaa">String | Object</span>       
                </td>      
                <td><p>注册的图片名或url或矢量对象</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setImage](API/Node.md#setImage)</font>

#### setLayer(layer)

设置数据元素在GraphView组件中的图层位置
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">layer</td>
                <td>    
                    <span style="color:#aaa">String | Number</span>       
                </td>      
                <td><p>图层名</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#setLayer](API/Data.md#setLayer)</font>

#### setName(name)

设置数据元素名称
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">name</td>
                <td>    
                    <span style="color:#aaa">String</span>       
                </td>      
                <td><p>数据元素名称</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#setName](API/Data.md#setName)</font>

#### setParent(parent)

设置父元素
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">parent</td>
                <td>    
                    <span style="color:#aaa">hc.Data</span>       
                </td>      
                <td><p>父元素</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#setParent](API/Data.md#setParent)</font>

#### setPosition(x, y)

设置图元中心点坐标
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">x</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>x坐标</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">y</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y坐标</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setPosition](API/Node.md#setPosition)</font>

#### setPosition3d(x, y, z)

设置图元中心点在3D拓扑中的三维坐标
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">x</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>x坐标</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">y</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y坐标</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">z</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>z坐标</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setPosition3d](API/Node.md#setPosition3d)</font>

#### setRect(x, y, width, heighc)

设置图元矩形区域
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">x</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>x坐标</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">y</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y坐标</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">width</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>宽度</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">heighc</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>高度</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setRect](API/Node.md#setRect)</font>

#### setRotation(rotation)

设置图元的旋转角度，围绕中心点顺时针旋转
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">rotation</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>旋转角度(弧度制)</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setRotation](API/Node.md#setRotation)</font>

#### setRotation3d(x, y, z)

设置图元在3D拓扑中的三维旋转角度
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">rotationX</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>沿x轴的旋转角度(弧度制)</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">rotationY</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>沿y轴的旋转角度(弧度制)</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">rotationZ</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>沿z轴的旋转角度(弧度制)</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setRotation3d](API/Node.md#setRotation3d)</font>

#### setRotationMode(rotationMode)

设置三维旋转模式  
  
图元在3D拓扑中旋转时，先沿x轴旋转，再沿y轴旋转和先沿y轴旋转，再沿x轴旋转最后的结果是不一样的
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">rotationMode</td>
                <td>    
                    <span style="color:#aaa">String</span>       
                </td>      
                <td><p>旋转模式，可选值如下：</p></td>
            </tr>
            <tr>  
                <td></td>
                <td></td>      
                <td><p>xyz:先进行x轴旋转，再进行y轴旋转，最后进行z轴旋转<br>yxz:先进行y轴旋转，再进行x轴旋转，最后进行z轴旋转<br>yzx:先进行y轴旋转，再进行z轴旋转，最后进行x轴旋转<br>zxy:先进行z轴旋转，再进行x轴旋转，最后进行y轴旋转<br>zyx:先进行z轴旋转，再进行y轴旋转，最后进行x轴旋转</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setRotationMode](API/Node.md#setRotationMode)</font>

See:  
&emsp;&emsp;<font color=Blue>[getRotationMode](API/Node.md#getRotationMode)</font>

#### setRotationX(rotationX)

设置图元在3D拓扑中沿x轴的旋转角度(弧度制)
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">rotationX</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>旋转角度(弧度制)</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setRotationX](API/Node.md#setRotationX)</font>

#### setRotationY(rotationY)

设置图元在3D拓扑中沿y轴的旋转角度(弧度制)
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">rotationY</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>旋转角度(弧度制)</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setRotationY](API/Node.md#setRotationY)</font>
#### setRotationZ(rotationZ)

设置图元在3D拓扑中沿z轴的旋转角度(弧度制)
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">rotationZ</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>旋转角度(弧度制)</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setRotationZ](API/Node.md#setRotationZ)</font>

#### setScale(x, y)

设置图元在2D拓扑中的缩放值
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">x</td>
                <td>    
                    <span style="color:#aaa">Number | Object</span>       
                </td>      
                <td><p>x轴方向缩放值,当仅有一个参数时，可传入{x, y}格式的对象</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">y</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y轴方向缩放值</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setScale](API/Node.md#setScale)</font>

#### setScale3d(x, y, z)

设置图元在3D拓扑中的缩放值
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">x</td>
                <td>    
                    <span style="color:#aaa">Number | Array</span>       
                </td>      
                <td><p>x轴方向缩放值,当仅有一个参数时，可传入[x, y]格式的对象</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">y</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y轴方向缩放值</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">z</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>z轴方向缩放值</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setScale3d](API/Node.md#setScale3d)</font>

#### setScaleTall(y)

设置图元在3D拓扑中y轴方向的缩放值
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">y</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y轴方向缩放值</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setScaleTall](API/Node.md#setScaleTall)</font>

#### setScaleX(x)

设置图元在2D拓扑中x轴方向的缩放值
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">x</td>
                <td>    
                    <span style="color:#aaa">Number | Array</span>       
                </td>      
                <td><p>x轴方向缩放值</p></td>
            </tr>
        </tbody>
    </table>
</div>  

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setScaleX](API/Node.md#setScaleX)</font>

#### setScaleY(y)

设置图元在2D拓扑中y轴方向的缩放值
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">y</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y轴方向缩放值</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setScaleY](API/Node.md#setScaleY)</font>

#### setSize(width, heighc)

设置图元在2D拓扑中的尺寸(宽高)
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">width</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>宽度</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">heighc</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>高度</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setSize](API/Node.md#setSize)</font>

#### setSize3d(width, tall, heighc)

设置图元在3D拓扑中的尺寸
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">width</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>x轴方向的长度</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">tall</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y轴方向的长度</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">heighc</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>z轴方向的长度</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setSize3d](API/Node.md#setSize3d)</font>

#### setStyle(name, value)

设置样式
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">name</td>
                <td>    
                    <span style="color:#aaa">String</span>       
                </td>      
                <td><p>样式名</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">value</td>
                <td>    
                    <span style="color:#aaa">Object</span>       
                </td>      
                <td><p>样式值</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#setStyle](API/Data.md#setStyle)</font>

#### setSyncSize(clickThroughEnabled)

设置块节点是否同步子节点大小
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">clickThroughEnabled</td>
                <td>    
                    <span style="color:#aaa">Boolean</span>       
                </td>      
                <td><p></p></td>
            </tr>
        </tbody>
    </table>
</div>
#### setTag(tag)

设置标识号，可通过[getDataByTag](API/DataModel.md#getDataByTag)快速查找
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">tag</td>
                <td>    
                    <span style="color:#aaa">String</span>       
                </td>      
                <td><p>标识号</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#setTag](API/Data.md#setTag)</font>

#### setTall() → {Number}

设置图元在3D拓扑中的y轴方向的长度

##### Returns:

&emsp;&emsp;Number - tall y轴方向的长度

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setTall](API/Node.md#setTall)</font>

#### setToolTip(toolTip)

设置文字提示信息
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">toolTip</td>
                <td>    
                    <span style="color:#aaa">String</span>       
                </td>      
                <td><p>文字提示</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#setToolTip](API/Data.md#setToolTip)</font>

#### setWidth() → {Number}

设置图元在3D拓扑中的x轴方向的长度

#### Returns:

&emsp;&emsp;Number - width x轴方向的长度

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#setWidth](API/Node.md#setWidth)</font>

#### size() → {Number}

获取孩子元素总数

##### Returns:

&emsp;&emsp;Number - 孩子元素总数

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#size](API/Data.md#size)</font>

#### t3(tx, ty, tz)

在当前坐标的基础上增加x、y、z三个方向的平移值，[translate3d](API/Node.md#translate3d)的缩写
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">tx</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>x轴方向的平移值</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">ty</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y轴方向的平移值</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">tz</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>z轴方向的平移值</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#t3](API/Node.md#t3)</font>
See:  
&emsp;&emsp;<font color=Blue>[translate3d](API/Node.md#translate3d)</font>

#### toChildren(matchFunc, scope) → {[hc.List](API/List.md)}

以matchFunc为过滤函数构建新的孩子元素集合
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr style="color:#1F1F1F">
                <th>Name</th>
                <th>Type</th>
                <th>Attributes</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">matchFunc</td>
                <td>    
                    <span style="color:#aaa">function</span>       
                </td>      
                    <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>过滤函数</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">scope</td>
                <td>    
                    <span style="color:#aaa">Object</span>       
                </td>      
                <td style="color:#aaa">&lt;optional&gt;</td>
                <td style="color:#333"><p>函数域</p></td>
            </tr>
        </tbody>
    </table>
</div>
#### Returns:

&emsp;&emsp;[hc.List](API/List.md) - 孩子元素集合

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#toChildren](API/Data.md#toChildren)</font>

##### Example

    var list = data.toChildren(function(child) {
       if (child.a('visible')) {
       	return true;
       }
    });

#### toLabel() → {String}

返回值作为TreeView和GraphView等组件上的图元文字标签，默认返回displayName||name信息

##### Returns:

&emsp;&emsp;String - 文字标签

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Data#toLabel](API/Data.md#toLabel)</font>

#### toString() → {String}

重写js默认的toString

##### Returns:

&emsp;&emsp;String

Inherited From:    
&emsp;&emsp;<font color=Blue>[hc.Data#toString](API/Data.md#toString)</font>

#### translate(tx, ty)

在当前坐标的基础上增加x、y两个方向的平移值
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">tx</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>x轴方向的平移值</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">ty</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y轴方向的平移值</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#translate](API/Node.md#translate)</font>

#### translate3d(tx, ty, tz)

在当前坐标的基础上增加x、y、z三个方向的平移值，[t3](API/Node.md#t3)的缩写
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">tx</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>x轴方向的平移值</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">ty</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>y轴方向的平移值</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">tz</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>z轴方向的平移值</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#translate3d](API/Node.md#translate3d)</font>

See:  
&emsp;&emsp;<font color=Blue>[t3](API/Node.md#t3)</font>

#### translate3dBy(direction, distance)

沿向量平移
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">direction</td>
                <td>    
                    <span style="color:#aaa">Array</span>       
                </td>      
                <td><p>方向向量</p></td>
            </tr>
            <tr>  
                <td style="color:#F17DA4">distance</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>平移距离</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#translate3dBy](API/Node.md#translate3dBy)</font>

#### translateBack(distance)

沿向量\[0, 0, -1\]平移
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">distance</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>平移距离</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#translateBack](API/Node.md#translateBack)</font>

#### translateBottom(distance)

沿向量\[0, -1, 0\]平移
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">distance</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>平移距离</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#translateBottom](API/Node.md#translateBottom)</font>

#### translateFront(distance)

沿向量\[0, 0, 1\]平移
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">distance</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>平移距离</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#translateFront](API/Node.md#translateFront)</font>

#### translateLeft(distance)

沿向量\[-1, 0, 0\]平移
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">distance</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>平移距离</p></td>
            </tr>
        </tbody>
    </table>
</div>  

Inherited From:    
&emsp;&emsp;<font color=Blue>[hc.Node#translateLeft](API/Node.md#translateLeft)</font>

#### translateRighc(distance)

沿向量\[1, 0, 0\]平移
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">distance</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>平移距离</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#translateRighc](API/Node.md#translateRighc)</font>

#### translateTop(distance)

沿向量\[0, 1, 0\]平移

##### Parameters:
<h5>Parameters:</h5>
<div style="width:100%;background-color:#f4f7f8">
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>  
                <td style="color:#F17DA4">distance</td>
                <td>    
                    <span style="color:#aaa">Number</span>       
                </td>      
                <td><p>平移距离</p></td>
            </tr>
        </tbody>
    </table>
</div>

Inherited From:  
&emsp;&emsp;<font color=Blue>[hc.Node#translateTop](API/Node.md#translateTop)</font>
