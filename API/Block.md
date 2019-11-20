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
*   [hc.Data#a](API/Data.md#a)
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
                    <span style="color:#aaa">hc.Data</span>       
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

*   [hc.Data#addChild](API/Data.md#addChild)

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

#### Returns:
Inherited From:

*   [hc.Data#addStyleIcon](hc.Data.hcml#addStyleIcon)

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
#### clearChildren()

删除所有孩子节点，内部会自动调用setParent  
Inherited From:

*   [hc.Data#clearChildren](hc.Data.hcml#clearChildren)

#### dm() → {[hc.DataModel](API/DataModel.md)}

获取[DataModel](hc.DataModel.hcml)，[getDataModel](hc.Data.hcml#getDataModel)的缩写

##### Returns:

[hc.DataModel](hc.DataModel.hcml) - dataModel

Inherited From:

*   [hc.Data#dm](hc.Data.hcml#dm)

#### eachChild(func, scope)

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

*   [hc.Data#eachChild](API/Data.md#eachChild)

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

*   [hc.Data#firePropertyChange](API/Data.md#firePropertyChange)

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

*   [hc.Data#fp](hc.Data.hcml#fp)

#### getAgentEdges() → {[hc.List](hc.List.hcml)}

获取当前图元代理的连线集合

#### Returns:

[hc.List](API/List.md)

Inherited From:

*   [hc.Node#getAgentEdges](API/Node.md#getAgentEdges)

#### getAttaches() → {[hc.List](hc.List.hcml)}

获取吸附到自身的所有图元

#### Returns:

[hc.List](API/List.md)

Inherited From:

*   [hc.Node#getAttaches](hc.Node.hcml#getAttaches)

#### getAttr(name) → {Object}

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

Object

Inherited From:

*   [hc.Data#getAttr](API/Data.md#getAttr)

#### getAttrObject() → {Object}

获取attr属性对象，该属性默认为空，用于存储用户业务信息

##### Returns:

Object - attr属性对象

Inherited From:

*   [hc.Data#getAttrObject](API/Data.md#getAttrObject)

#### getChildAt(index) → {[hc.Data](hc.Data.hcml)}

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

[hc.Data](API/Data.md) - 索引对应的孩子

Inherited From:

*   [hc.Data#getChildAt](API/Data.md#getChildAt)

#### getChildren() → {[hc.List](hc.List.hcml)}

获取所有孩子节点

##### Returns:

[hc.List](API/List.md) - 孩子元素集合

Inherited From:

*   [hc.Data#getChildren](PAI/Data.md#getChildren)

#### getClass() → {function}

获取类声明(构造函数)

##### Returns:

function - 类声明(构造函数)

Inherited From:

*   [hc.Data#getClass](API/Data.md#getClass)

#### getClassName() → {String}

获取类全名，继承Data并希望序列化时应该重写此方法返回子类的类名字符串

#### Returns:

String - 类全名

Inherited From:

*   [hc.Data#getClassName](API/Data.md#getClassName)

See:

*   [hc.Data#getSuperClass](API/Data.md#getSuperClass)

#### getCorners(xPadding, yPadding) → {Array}

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

Array - 四个角坐标，顺序为左上，右上，右下，左下

Inherited From:

*   [hc.Node#getCorners](hc.Node.hcml#getCorners)

##### Example

    //返回值示例：
    [
    {x: 0, y: 0},//左上
    {x: 100, y: 0},//右上
    {x: 100, y: 100},//右下
    {x: 0, y: 100}//左下
    ]

#### getDataModel() → {[hc.DataModel](API/DataModel.md)}

获取所属的DataModel

#### Returns:

[hc.DataModel](API/DataModel.md) - DataModel数据容器

Inherited From:

*   [hc.Data#getDataModel](API/Data.md#getDataModel)

#### getDisplayName() → {String}

获取显示名称，常作为Column和Property的列头和属性名称显示

##### Returns:

String - 显示名称

Inherited From:

*   [hc.Data#getDisplayName](API/Data.md#getDisplayName)

#### getEdges() → {[hc.List](hc.List.hcml)}

获取所有跟图元关联的连线(不包括代理的连线)

##### Returns:

[hc.List](hc.List.hcml)

Inherited From:

*   [hc.Node#getEdges](hc.Node.hcml#getEdges)

#### getElevation() → {Number}

获取图元中心在3D坐标系中的y坐标

##### Returns:

Number

Inherited From:

*   [hc.Node#getElevation](hc.Node.hcml#getElevation)

#### getHeighc() → {Number}

获取图元在2D拓扑中的高度，或3D拓扑中的z轴长度

##### Returns:

Number

Inherited From:

*   [hc.Node#getHeighc](hc.Node.hcml#getHeighc)

#### getHost() → {[hc.Data](hc.Data.hcml)}

获取宿主图元，当图元吸附上宿主图元时，宿主移动或旋转时会带动所有吸附者

##### Returns:

[hc.Data](hc.Data.hcml)

Inherited From:

*   [hc.Node#getHost](hc.Node.hcml#getHost)

#### getIcon() → {String|Object}

获取小图标名称，常作为TreeView和ListView等组件上的节点小图标

##### Returns:

String | Object - 图标名或矢量

Inherited From:

*   [hc.Data#getIcon](hc.Data.hcml#getIcon)

#### getId() → {Number}

获取唯一编号

##### Returns:

Number - 唯一编号

Inherited From:

*   [hc.Data#getId](hc.Data.hcml#getId)

#### getImage() → {[hc.Data](hc.Data.hcml)}

获取拓扑上展现的图片信息，在GraphView拓扑图中图片一般以position为中心绘制

##### Returns:

[hc.Data](hc.Data.hcml)

Inherited From:

*   [hc.Node#getImage](hc.Node.hcml#getImage)

#### getLayer() → {String|Number}

获取数据元素在GraphView组件中的图层位置

##### Returns:

String | Number - 图层名

Inherited From:

*   [hc.Data#getLayer](hc.Data.hcml#getLayer)

Default Value:

*   0

#### getLoopedEdges() → {[hc.List](hc.List.hcml)}

获取所有跟节点关联的自环连线

##### Returns:

[hc.List](hc.List.hcml)

Inherited From:

*   [hc.Node#getLoopedEdges](hc.Node.hcml#getLoopedEdges)

#### getName() → {String}

获取数据元素名

##### Returns:

String - 名称

Inherited From:

*   [hc.Data#getName](hc.Data.hcml#getName)

#### getParent() → {[hc.Data](hc.Data.hcml)}

获取父元素

##### Returns:

[hc.Data](hc.Data.hcml) - 父元素

Inherited From:

*   [hc.Data#getParent](hc.Data.hcml#getParent)

#### getPosition() → {Object}

获取图元中心点坐标

##### Returns:

Object

Inherited From:

*   [hc.Node#getPosition](hc.Node.hcml#getPosition)

##### Example

    //返回值示例：
    {
    	x: 0,
    	y: 0
    }

#### getPosition3d() → {Array}

获取图元中心点在3D拓扑中的三维坐标

##### Returns:

Array - 三维坐标数组，格式为\[x, y, z\]

Inherited From:

*   [hc.Node#getPosition3d](hc.Node.hcml#getPosition3d)

#### getRect() → {Object}

获取图元的矩形区域(包括旋转)

##### Returns:

Object - 矩形区域

Inherited From:

*   [hc.Node#getRect](hc.Node.hcml#getRect)

##### Example

    //返回值示例：
    {x: 0, y: 0, width: 100, heighc: 100}

#### getRotation() → {Number}

获取图元的旋转角度，围绕中心点顺时针旋转

##### Returns:

Number - 旋转角度(弧度制)

Inherited From:

*   [hc.Node#getRotation](hc.Node.hcml#getRotation)

#### getRotation3d() → {Array}

获取图元在3D拓扑中的三维旋转角度

##### Returns:

Array - 三维旋转角度(弧度制)，格式为\[x, y, z\]，即\[getRotationX(), -getRotation(), getRotationZ()\]

Inherited From:

*   [hc.Node#getRotation3d](hc.Node.hcml#getRotation3d)

#### getRotationMode() → {String}

返回三维旋转模式  
  
图元在3D拓扑中旋转时，先沿x轴旋转，再沿y轴旋转和先沿y轴旋转，再沿x轴旋转最后的结果是不一样的

##### Returns:

String - 三维旋转模式，xyz|xzy|yxz|yzx|zxy|zyx

Inherited From:

*   [hc.Node#getRotationMode](hc.Node.hcml#getRotationMode)

See:

*   [setRotationMode](hc.Node.hcml#setRotationMode)

#### getRotationX() → {Number}

获取图元在3d拓扑中沿x轴的旋转角度(弧度制)

##### Returns:

Number

Inherited From:

*   [hc.Node#getRotationX](hc.Node.hcml#getRotationX)

#### getRotationY() → {Number}

获取图元在3d拓扑中沿y轴的旋转角度(弧度制)

##### Returns:

Number

Inherited From:

*   [hc.Node#getRotationY](hc.Node.hcml#getRotationY)

#### getRotationZ() → {Number}

获取图元在3d拓扑中沿z轴的旋转角度(弧度制)

##### Returns:

Number

Inherited From:

*   [hc.Node#getRotationZ](hc.Node.hcml#getRotationZ)

#### getScale() → {Object}

获取图元在2D拓扑中的缩放值

##### Returns:

Object

Inherited From:

*   [hc.Node#getScale](hc.Node.hcml#getScale)

##### Example

    //返回值示例：
    {
    	x: 1,
    	y: 1
    }

#### getScale3d() → {Array}

获取图元在3D拓扑中的缩放值

##### Returns:

Array - 格式为\[x, y, z\]，即\[getScaleX(), getScaleTall(), getScaleY()\]

Inherited From:

*   [hc.Node#getScale3d](hc.Node.hcml#getScale3d)

#### getScaleTall() → {Number}

获取图元在3D拓扑中y轴方向的缩放值

##### Returns:

Number - y轴方向缩放值

Inherited From:

*   [hc.Node#getScaleTall](hc.Node.hcml#getScaleTall)

#### getScaleX() → {Number}

获取图元在2D拓扑中x轴方向的缩放值

##### Returns:

Number - x轴方向缩放值

Inherited From:

*   [hc.Node#getScaleX](hc.Node.hcml#getScaleX)

#### getScaleY() → {Number}

设置图元在2D拓扑中y轴方向的缩放值

##### Returns:

Number - y轴方向缩放值

Inherited From:

*   [hc.Node#getScaleY](hc.Node.hcml#getScaleY)

#### getSerializableAttrs() → {Object}

此函数返回一个map，决定序列化时哪些attr属性可被序列化，默认所有attr对象里的属性都会被序列化

##### Returns:

Object - 需要被序列化的attr属性map

Inherited From:

*   [hc.Data#getSerializableAttrs](hc.Data.hcml#getSerializableAttrs)

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

Object - 需要被序列化的属性map

Inherited From:

*   [hc.Data#getSerializableProperties](hc.Data.hcml#getSerializableProperties)

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

Object - 需要被序列化的样式map

Inherited From:

*   [hc.Data#getSerializableStyles](hc.Data.hcml#getSerializableStyles)

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

Object

Inherited From:

*   [hc.Node#getSize](hc.Node.hcml#getSize)

##### Example

    //返回值示例：
    {
    	with: 100,
    	heighc: 100
    }

#### getSize3d() → {Array}

获取图元在3D拓扑中的尺寸(长宽高)

##### Returns:

Array - 格式为\[x, y, z\]，即\[getWidth(), getTall(), getHeighc()\]

Inherited From:

*   [hc.Node#getSize3d](hc.Node.hcml#getSize3d)

#### getSourceAgentEdges() → {[hc.List](hc.List.hcml)}

获取代理的起始于该图元的连线

##### Returns:

[hc.List](hc.List.hcml)

Inherited From:

*   [hc.Node#getSourceAgentEdges](hc.Node.hcml#getSourceAgentEdges)

#### getSourceEdges() → {[hc.List](hc.List.hcml)}

获取跟图元关联的并起始于该图元的连线(不包括代理的连线)

##### Returns:

[hc.List](hc.List.hcml)

Inherited From:

*   [hc.Node#getSourceEdges](hc.Node.hcml#getSourceEdges)

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

Object

Inherited From:

*   [hc.Data#getStyle](hc.Data.hcml#getStyle)

#### getStyleMap() → {Object}

获取图元内部样式映射信息

##### Returns:

Object - 样式映射表

Inherited From:

*   [hc.Data#getStyleMap](hc.Data.hcml#getStyleMap)

#### getSuperClass() → {function}

获取父类声明(构造函数)，继承类时可以用来调用父类构造或函数

##### Returns:

function - 父类声明(构造函数)

Inherited From:

*   [hc.Data#getSuperClass](hc.Data.hcml#getSuperClass)

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

获取标识号，可通过[getDataByTag](hc.DataModel.hcml#getDataByTag)快速查找

##### Returns:

String - 标识号

Inherited From:

*   [hc.Data#getTag](hc.Data.hcml#getTag)

#### getTall() → {Number}

获取图元在3D拓扑中的y轴长度

##### Returns:

Number

Inherited From:

*   [hc.Node#getTall](hc.Node.hcml#getTall)

#### getTargetAgentEdges() → {[hc.List](hc.List.hcml)}

获取图元代理的结束于该图元的连线

##### Returns:

[hc.List](hc.List.hcml)

Inherited From:

*   [hc.Node#getTargetAgentEdges](hc.Node.hcml#getTargetAgentEdges)

#### getTargetEdges() → {[hc.List](hc.List.hcml)}

获取跟图元关联的并结束于该图元的连线(不包括代理的连线)

##### Returns:

[hc.List](hc.List.hcml)

Inherited From:

*   [hc.Node#getTargetEdges](hc.Node.hcml#getTargetEdges)

#### getToolTip() → {String}

获取文字提示信息

##### Returns:

String - 文字提示

Inherited From:

*   [hc.Data#getToolTip](hc.Data.hcml#getToolTip)

#### getUIClass() → {function}

获取拓扑组件上的UI类

##### Returns:

function - UI类声明(构造函数)

Inherited From:

*   [hc.Data#getUIClass](hc.Data.hcml#getUIClass)

#### getWidth() → {Number}

获取图元在2D拓扑中的宽度，或在3D拓扑中x轴的长度

##### Returns:

Number

Inherited From:

*   [hc.Node#getWidth](hc.Node.hcml#getWidth)

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

*   [hc.Node#handleHostPropertyChange](hc.Node.hcml#handleHostPropertyChange)

#### hasAgentEdges() → {Boolean}

判断当前图元上是否有代理连线

##### Returns:

Boolean

Inherited From:

*   [hc.Node#hasAgentEdges](hc.Node.hcml#hasAgentEdges)

#### hasChildren() → {Boolean}

判断是否有孩子

##### Returns:

Boolean - 是否有孩子

Inherited From:

*   [hc.Data#hasChildren](hc.Data.hcml#hasChildren)

#### invalidate()

强制触发属性变化事件通知界面更新

Inherited From:

*   [hc.Data#invalidate](hc.Data.hcml#invalidate)

#### isAdjustChildrenToTop() → {Boolean}

GraphView点击图元会自动sendToTop，该属性决定是否对子图元也进行sendToTop操作

##### Returns:

Boolean - 是否将children自动sendToTop

Inherited From:

*   [hc.Data#isAdjustChildrenToTop](hc.Data.hcml#isAdjustChildrenToTop)

#### isClickThroughEnabled() → {Boolean}

获取块节点是否可以点击穿透

##### Returns:

Boolean

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

Boolean - 自身是否为指定data的子孙

Inherited From:

*   [hc.Data#isDescendantOf](hc.Data.hcml#isDescendantOf)

#### isEmpty() → {Boolean}

判断是否有孩子，同[hasChildren](hc.Data.hcml#hasChildren)

##### Returns:

Boolean - 是否有孩子

Inherited From:

*   [hc.Data#isEmpty](hc.Data.hcml#isEmpty)

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

Boolean

Inherited From:

*   [hc.Node#isHostOn](hc.Node.hcml#isHostOn)

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

Boolean - 自身是否为指定data的父亲

Inherited From:

*   [hc.Data#isParentOf](hc.Data.hcml#isParentOf)

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

Boolean - 自身与指定data是否有父子或子孙关系

Inherited From:

*   [hc.Data#isRelatedTo](hc.Data.hcml#isRelatedTo)

#### isSyncSize() → {Boolean}

获取块节点是否同步子节点大小

##### Returns:

Boolean

#### iv()

强制触发属性变化事件通知界面更新，[invalidate](hc.Data.hcml#invalidate)的缩写

Inherited From:

*   [hc.Data#iv](hc.Data.hcml#iv)

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

*   [hc.Data#onChildAdded](hc.Data.hcml#onChildAdded)

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

*   [hc.Data#onChildRemoved](hc.Data.hcml#onChildRemoved)

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

*   [hc.Node#onHostChanged](hc.Node.hcml#onHostChanged)

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

*   [hc.Data#onParentChanged](hc.Data.hcml#onParentChanged)

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

*   [hc.Data#onPropertyChanged](hc.Data.hcml#onPropertyChanged)

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

*   [hc.Data#onStyleChanged](hc.Data.hcml#onStyleChanged)

#### p(x, y) → {Object}

获取或设置设置图元中心点坐标，有参数时相当于[setPosition](hc.Node.hcml#setPosition)，没有参数时相当于[getPosition](hc.Node.hcml#getPosition)
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

Object - 坐标值，格式为:{x: x, y: y}

Inherited From:

*   [hc.Node#p](hc.Node.hcml#p)

See:

*   [setPosition](hc.Node.hcml#setPosition)
*   [getPosition](hc.Node.hcml#getPosition)

#### p3(x, y, z) → {Array}

获取或设置图元中心点在3D拓扑中的三维坐标，有三个参数时相当于[setPosition3d](hc.Node.hcml#setPosition3d)，没有参数时相当于[getPosition3d](hc.Node.hcml#getPosition3d)
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

Array - 三维坐标数组，格式为\[x, y, z\]

Inherited From:

*   [hc.Node#p3](hc.Node.hcml#p3)

See:

*   [setPosition3d](hc.Node.hcml#setPosition3d)
*   [getPosition3d](hc.Node.hcml#getPosition3d)

#### r3(rotationX, rotationY, rotationZ) → {Array}

获取或设置图元在3D拓扑中的三维旋转角度，有三个参数时相当于[setRotation3d](hc.Node.hcml#setRotation3d)，没有参数时相当于[getRotation3d](hc.Node.hcml#getRotation3d)
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

Array - 三维旋转角度(弧度制)，格式为\[x, y, z\]，即\[getRotationX(), -getRotation(), getRotationZ()\]

Inherited From:

*   [hc.Node#r3](hc.Node.hcml#r3)

See:

*   [setRotation3d](hc.Node.hcml#setRotation3d)
*   [getRotation3d](hc.Node.hcml#getRotation3d)

#### removeChild(child)

删除指定孩子元素，内部会自动调用孩子元素的setParent

##### Parameters:
>Name &emsp;Type&emsp;Description  
`child`&emsp; [hc.Data](hc.Data.hcml)&emsp;要删除的孩子元素  

Inherited From:

*   [hc.Data#removeChild](hc.Data.hcml#removeChild)

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

*   [hc.Data#removeStyleIcon](hc.Data.hcml#removeStyleIcon)

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

*   [hc.Node#rotateAt](hc.Node.hcml#rotateAt)

#### s(name, value) → {Object}

获取或设置样式，仅有一个参数时相当于[getStyle](hc.Data.hcml#getStyle)，有两个参数时相当于[setStyle](hc.Data.hcml#setStyle)
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

Object

Inherited From:

*   [hc.Data#s](hc.Data.hcml#s)

#### s3(width, tall, heighc) → {Array}

获取或设置图元在3D拓扑中的尺寸，有三个参数时相当于[setSize3d](hc.Node.hcml#setSize3d)，没有参数时相当于[getSize3d](hc.Node.hcml#getSize3d)
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

Array - 格式为\[x, y, z\]，即\[getWidth(), getTall(), getHeighc()\]  

Inherited From:

*   [hc.Node#s3](hc.Node.hcml#s3)

See:

*   [setSize3d](hc.Node.hcml#setSize3d)
*   [getSize3d](hc.Node.hcml#getSize3d)

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

*   [hc.Data#setAdjustChildrenToTop](hc.Data.hcml#setAdjustChildrenToTop)

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

*   [hc.Node#setAnchor](hc.Node.hcml#setAnchor)

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

*   [hc.Node#setAnchor3d](hc.Node.hcml#setAnchor3d)

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

*   [hc.Node#setAnchorElevation](hc.Node.hcml#setAnchorElevation)

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

*   [hc.Node#setAnchorX](hc.Node.hcml#setAnchorX)

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

*   [hc.Node#setAnchorY](hc.Node.hcml#setAnchorY)

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

*   [hc.Data#setAttr](hc.Data.hcml#setAttr)

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

*   [hc.Data#setAttrObject](hc.Data.hcml#setAttrObject)

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

*   [hc.Data#setDisplayName](hc.Data.hcml#setDisplayName)

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

*   [hc.Node#setElevation](hc.Node.hcml#setElevation)

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

*   [hc.Node#setHeighc](hc.Node.hcml#setHeighc)

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

*   [hc.Node#setHost](hc.Node.hcml#setHost)

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

*   [hc.Data#setIcon](hc.Data.hcml#setIcon)

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

*   [hc.Data#setId](hc.Data.hcml#setId)

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

*   [hc.Node#setImage](hc.Node.hcml#setImage)

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

*   [hc.Data#setLayer](hc.Data.hcml#setLayer)

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

*   [hc.Data#setName](hc.Data.hcml#setName)

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

*   [hc.Data#setParent](hc.Data.hcml#setParent)

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

*   [hc.Node#setPosition](hc.Node.hcml#setPosition)

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

*   [hc.Node#setPosition3d](hc.Node.hcml#setPosition3d)

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

*   [hc.Node#setRect](hc.Node.hcml#setRect)

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

*   [hc.Node#setRotation](hc.Node.hcml#setRotation)

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

*   [hc.Node#setRotation3d](hc.Node.hcml#setRotation3d)

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

*   [hc.Node#setRotationMode](hc.Node.hcml#setRotationMode)

See:

*   [getRotationMode](hc.Node.hcml#getRotationMode)

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

*   [hc.Node#setRotationX](hc.Node.hcml#setRotationX)

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

*   [hc.Node#setRotationY](hc.Node.hcml#setRotationY)

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

*   [hc.Node#setRotationZ](hc.Node.hcml#setRotationZ)

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

*   [hc.Node#setScale](hc.Node.hcml#setScale)

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

*   [hc.Node#setScale3d](hc.Node.hcml#setScale3d)

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

*   [hc.Node#setScaleTall](hc.Node.hcml#setScaleTall)

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

*   [hc.Node#setScaleX](hc.Node.hcml#setScaleX)

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

*   [hc.Node#setScaleY](hc.Node.hcml#setScaleY)

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

*   [hc.Node#setSize](hc.Node.hcml#setSize)

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

*   [hc.Node#setSize3d](hc.Node.hcml#setSize3d)

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

*   [hc.Data#setStyle](hc.Data.hcml#setStyle)

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

设置标识号，可通过[getDataByTag](hc.DataModel.hcml#getDataByTag)快速查找
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

*   [hc.Data#setTag](hc.Data.hcml#setTag)

#### setTall() → {Number}

设置图元在3D拓扑中的y轴方向的长度

##### Returns:

Number - tall y轴方向的长度

Inherited From:

*   [hc.Node#setTall](hc.Node.hcml#setTall)

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

*   [hc.Data#setToolTip](hc.Data.hcml#setToolTip)

#### setWidth() → {Number}

设置图元在3D拓扑中的x轴方向的长度

#### Returns:

Number - width x轴方向的长度

Inherited From:

*   [hc.Node#setWidth](hc.Node.hcml#setWidth)

#### size() → {Number}

获取孩子元素总数

##### Returns:

Number - 孩子元素总数

Inherited From:

*   [hc.Data#size](hc.Data.hcml#size)

#### t3(tx, ty, tz)

在当前坐标的基础上增加x、y、z三个方向的平移值，[translate3d](hc.Node.hcml#translate3d)的缩写
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

*   [hc.Node#t3](hc.Node.hcml#t3)

See:

*   [translate3d](hc.Node.hcml#translate3d)

#### toChildren(matchFunc, scope) → {[hc.List](hc.List.hcml)}

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

[hc.List](hc.List.hcml) - 孩子元素集合

Inherited From:

*   [hc.Data#toChildren](hc.Data.hcml#toChildren)

##### Example

    var list = data.toChildren(function(child) {
       if (child.a('visible')) {
       	return true;
       }
    });

#### toLabel() → {String}

返回值作为TreeView和GraphView等组件上的图元文字标签，默认返回displayName||name信息

##### Returns:

String - 文字标签

Inherited From:

*   [hc.Data#toLabel](hc.Data.hcml#toLabel)

#### toString() → {String}

重写js默认的toString

##### Returns:

String

Inherited From:

*   [hc.Data#toString](hc.Data.hcml#toString)

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

*   [hc.Node#translate](hc.Node.hcml#translate)

#### translate3d(tx, ty, tz)

在当前坐标的基础上增加x、y、z三个方向的平移值，[t3](hc.Node.hcml#t3)的缩写
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

*   [hc.Node#translate3d](hc.Node.hcml#translate3d)

See:

*   [t3](hc.Node.hcml#t3)

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

*   [hc.Node#translate3dBy](hc.Node.hcml#translate3dBy)

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

*   [hc.Node#translateBack](hc.Node.hcml#translateBack)

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

*   [hc.Node#translateBottom](hc.Node.hcml#translateBottom)

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

*   [hc.Node#translateFront](hc.Node.hcml#translateFront)

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

*   [hc.Node#translateLeft](hc.Node.hcml#translateLeft)

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

*   [hc.Node#translateRighc](hc.Node.hcml#translateRighc)

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

*   [hc.Node#translateTop](hc.Node.hcml#translateTop)
