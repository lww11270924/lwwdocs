
#### new DataModel()

数据容器hc.DataModel作为承载Data数据的模型，  
管理着Data数据的增删以及变化事件派发，  
HT框架所有组件都是通过绑定DataModel，以不同的形式呈现到用户界面；  
同时组件也会监听DataModel模型的变化事件， 实时同步更新界面数据信息，  
掌握了DataModel的操作就掌握了所有组件的模型驱动方式。

### Methods

#### a(name, value) → {Object}

获取或设置attr属性，仅有一个参数时相当于[getAttr](hc.DataModel.html#getAttr)，有两个参数时相当于[setAttr](hc.DataModel.html#setAttr)

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;属性名  
`value`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;属性值


##### Returns:

Object

#### add(data, index)

增加数据元素

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;数据元素  
`index`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;插入索引


#### addDataModelChangeListener(listener, scope, ahead)

增加数据模型增删变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


See:

*   [mm](hc.DataModel.html#mm)

##### Example

    dataModel.addDataModelChangeListener(function(event) {
         //event格式：
         {
         	kind: "add"|"remove"|"clear",//事件类型
         	data: data//事件相关data
         }
    });

#### addDataPropertyChangeListener(listener, scope, ahead)

增加模型中Data元素属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


See:

*   [md](hc.DataModel.html#md)

##### Example

    dataModel.addDataPropertyChangeListener(function(event) {
         //event格式：
         {
         	property: "name",//发生变化的属性
         	data: data,//属性发生变化的data
         	oldValue: 0,//旧值
         	newValue: 1//新值
         }
    });

#### addHierarchyChangeListener(listener, scope, ahead)

增加监听器，监听Data在DataModel中的层次(用于TreeView、TreeTableView等)变化事件

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


See:

*   [mh](hc.DataModel.html#mh)

##### Example

    dataModel.addHierarchyChangeListener(function(event) {
         //event格式：
         {
         	data: data,//事件相关Data
         	oldIndex: 0,//旧层次
         	newIndex: 1//新层次
         }
    });

#### addIndexChangeListener(listener, scope, ahead)

增加监听器，监听Data在DataModel中的索引(用于拓扑组件)变化事件

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

##### Example

    dataModel.addIndexChangeListener(function(event) {
         //event格式：
         {
         	data: data,//事件相关Data
         	oldIndex: 0,//旧索引
         	newIndex: 1//新索引
         }
    });

#### clear()

删除容器中所有Data对象，该操作一次性清空，没有逐个remove的过程，不会影响Data父子关系

#### contains(data) → {Boolean}

判断容器是否包含该data对象

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp; Description  
`data`&emsp;&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;要判断的数据元素


##### Returns:

Boolean -

容器是否包含参数data

#### deserialize(json, rootParent, setId) → {[hc.List](hc.List.html)}

反序列化数据到数据容器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;  Description  
`json`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp; 要被反序列化的json字符串
`rootParent`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;指定反序列化的数据元素的父元素
`setId`&emsp;&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;反序列化后的数据元素是否保留原id

##### Returns:

[hc.List](hc.List.html) -

被反序列化的数据元素集合

#### each(func, scope)

提供一个回调函数遍历此容器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;遍历函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域

##### Example

    dataModel.each(function(data) {
      console.log(data);
    });

#### eachByBreadthFirst(func, data, scope)

以data为起始广度优先遍历Data对象

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;遍历函数  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;遍历起点元素
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域


#### eachByDepthFirst(func, data, scope)

以data为起始深度优先遍历Data对象

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;遍历函数  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;遍历起点元素
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域

#### firePropertyChange(property, oldValue, newValue)

派发属性变化事件

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp; Description  
`property`&emsp;&emsp;&emsp;String&emsp;&emsp;属性名
`oldValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;旧值
`newValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;新值


See:

*   [fp](hc.DataModel.html#fp)

#### fp(property, oldValue, newValue)

派发属性变化事件

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp; Description  
`property`&emsp;&emsp;&emsp;String&emsp;&emsp;属性名
`oldValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;旧值
`newValue`&emsp;&emsp;&emsp;Object&emsp;&emsp;新值

See:

*   [firePropertyChange](hc.DataModel.html#firePropertyChange)

#### getAttr(name) → {Object}

获取attr属性

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`name`&emsp;&emsp;String&emsp;&emsp;属性名

##### Returns:

Object

#### getAttrObject() → {Object}

获取attr属性对象，该属性默认为空，用于存储用户业务信息

##### Returns:

Object -

attr属性对象

#### getDataById(id) → {[hc.Data](hc.Data.html)}

根据id快速查找Data对象，模型内部维护着一个id->data的映射表，因此查找速度比遍历方式快

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`id`&emsp;&emsp;String | Number&emsp;&emsp;要查找的id

##### Returns:

[hc.Data](hc.Data.html) -

查找到的Data

#### getDataByTag(tag) → {[hc.Data](hc.Data.html)}

根据tag快速查找，模型内部维护着一个tag->data的映射表，因此查找速度比遍历方式快

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`tag`&emsp;&emsp;String | Number&emsp;&emsp;要查找的tag

##### Returns:

[hc.Data](hc.Data.html) -

查找到的Data

#### getDatas() → {[hc.List](hc.List.html)}

获取所有添加到容器的Data数据集合

##### Returns:

[hc.List](hc.List.html)

#### getHistoryManager() → {hc.HistoryManager}

获取历史管理器

##### Returns:

hc.HistoryManager

#### getRoots() → {[hc.List](hc.List.html)}

获取所有parent为空的Data对象

##### Returns:

[hc.List](hc.List.html)

#### getSelectionModel() → {[hc.SelectionModel](hc.SelectionModel.html)}

获取该容器的选择模型

##### Returns:

[hc.SelectionModel](hc.SelectionModel.html)

See:

*   [sm](hc.DataModel.html#sm)

#### getSerializableAttrs() → {Object}

此函数返回一个map，决定序列化时哪些attr属性可被序列化，默认所有attr对象里的属性都会被序列化

##### Returns:

Object -

需要被序列化的attr属性map

##### Example

    function(){
        var name, map = {};
        for (name in this._attrObject) {            
            map[name] = 1;
        }
        return map; 
    }

#### getSiblings(data) → {[hc.List](hc.List.html)}

获取和data同父子层次的兄弟数组，如果data父亲为空，则返回dataModel.getRoots()

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;Description  
`data`&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;目标data

##### Returns:

[hc.List](hc.List.html)

#### isAutoAdjustIndex() → {Boolean}

是否自动调整data在容器中索引顺序

##### Returns:

Boolean

#### isEmpty() → {Boolean}

判断容器是否为空

##### Returns:

Boolean

#### isHierarchicalRendering() → {Boolean}

判断容器是否为树层次渲染

##### Returns:

Boolean

#### md(listener, scope, ahead)

增加模型中Data元素属性变化事件监听器，[addDataPropertyChangeListener](hc.DataModel.html#addDataPropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数 
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [addDataPropertyChangeListener](hc.DataModel.html#addDataPropertyChangeListener)

##### Example

    dataModel.md(function(event) {
         //event格式：
         {
         	property: "name",//发生变化的属性
         	data: data,//属性发生变化的data
         	oldValue: 0,//旧值
         	newValue: 1//新值
         }
    });

#### mh(listener, scope, ahead)

增加监听器，监听Data在DataModel中的层次(用于TreeView、TreeTableView等)变化事件，[addHierarchyChangeListener](hc.DataModel.html#addHierarchyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [addHierarchyChangeListener](hc.DataModel.html#addHierarchyChangeListener)

##### Example

    dataModel.mh(function(event) {
         //event格式：
         {
         	data: data,//事件相关Data
         	oldIndex: 0,//旧层次
         	newIndex: 1//新层次
         }
    });

#### mm(listener, scope, ahead)

增加数据模型增删变化事件监听器，[addDataModelChangeListener](hc.DataModel.html#addDataModelChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [addDataModelChangeListener](hc.DataModel.html#addDataModelChangeListener)

##### Example

    dataModel.mm(function(event) {
         //event格式：
         {
         	kind: "add"|"remove"|"clear",//事件类型
         	data: data//事件相关data
         }
    });

#### moveDown(data)

移动data到同层兄弟数组中的下一个位置

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;要移动的数据元素

#### moveSelectionDown(sm)

移动当前选中的数据元素到同层兄弟数组中的下一个位置

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`sm`&emsp;&emsp;&emsp;[hc.SelectionModel](hc.SelectionModel.html)&emsp;\<optional>&emsp;&emsp;要操作的选中模型，如果为空，使用dataModel自身绑定的选中模型

#### moveSelectionToBottom(sm)

移动当前选中的数据元素到同层兄弟数组的底部

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`sm`&emsp;&emsp;&emsp;[hc.SelectionModel](hc.SelectionModel.html)&emsp;\<optional>&emsp;&emsp;要操作的选中模型，如果为空，使用dataModel自身绑定的选中模型
#### moveSelectionToTop(sm)

移动当前选中的数据元素到同层兄弟数组的顶部

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`sm`&emsp;&emsp;&emsp;[hc.SelectionModel](hc.SelectionModel.html)&emsp;\<optional>&emsp;&emsp;要操作的选中模型，如果为空，使用dataModel自身绑定的选中模型

#### moveSelectionUp(sm)

移动当前选中的数据元素到同层兄弟数组中的上一个位置

##### Parameters:
>Name&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`sm`&emsp;&emsp;&emsp;[hc.SelectionModel](hc.SelectionModel.html)&emsp;\<optional>&emsp;&emsp;要操作的选中模型，如果为空，使用dataModel自身绑定的选中模型

#### moveTo(data, newIndex)

移动数据元素到同层兄弟数组中的指定索引

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;要移动的数据元素  
`newIndex`&emsp;&emsp;&emsp;&emsp;Number&emsp;目标索引  

#### moveToBottom(data)

移动数据元素到同层兄弟数组的底部

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;要移动的数据元素  


#### moveToTop(data)

移动数据元素到同层兄弟数组的顶部

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;要移动的数据元素  

#### moveUp(data)

移动数据元素到同层兄弟数组中的上一个位置

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;要移动的数据元素  

#### onAdded(data)

数据元素添加的回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;新添加的数据元素  

#### onDataPropertyChanged(data, e)

数据元素属性变化回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;发生变化的数据元素  
`e`&emsp;&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;事件信息 


#### onRemoved(data)

数据元素删除时回调函数，可重载做后续处理

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;被删除的数据元素 
#### remove(data)

删除数据元素，该操作有以下副作用：

  
*   其子孙被递归从DataModel中删除
  
*   被断开父子关系data.setParent(null)
  
*   Edge类型通过edge.setSource(null)和data.setTarget(null)断开节点关系
  
*   Node类型会将其关联的连线从DataModel中删除
  
*   Node类型通过data.setHost(null)断开与宿主吸附节点关系
  

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;要删除的数据元素 

#### removeDataById(id)

通过id删除数据元素

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`id`&emsp;&emsp;&emsp;&emsp;Number&emsp;要删除的数据元素id 

See:

*   [remove](hc.DataModel.html#remove)

#### removeDataByTag(tag)

通过tag删除数据元素

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`tag`&emsp;&emsp;String&emsp;&emsp;要删除的数据元素tag 

See:

*   [remove](hc.DataModel.html#remove)

#### removeDataModelChangeListener(listener, scope)

删除数据模型增删变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数 
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [umm](hc.DataModel.html#umm)

#### removeDataPropertyChangeListener(listener, scope)

删除模型中Data元素属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数 
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [umd](hc.DataModel.html#umd)

#### removeHierarchyChangeListener(listener, scope)

删除监听Data在DataModel中的层次(用于TreeView、TreeTableView等)变化事件的监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数 
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [umh](hc.DataModel.html#umh)

#### removeIndexChangeListener(listener, scope)

删除监听Data在DataModel中的索引(用于拓扑组件)变化事件的监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数 
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域


#### sendToBottom(data)

将data在拓扑上置底

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;要置底的数据元素  

#### sendToTop(data)

将data在拓扑上置顶

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;要置顶的数据元素  


#### serialize(space)

将数据模型序列化成JSON格式字符串

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`space`&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;缩进空格数  

#### setAttr(name, value)

设置attr属性

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`name`&emsp;&emsp;&emsp;String&emsp;&emsp;&emsp;属性名  
`value`&emsp;&emsp;&emsp;Object&emsp;&emsp;属性值


#### setAttrObject(attrObject)

设置attr属性对象，该属性默认为空，用于存储用户业务信息

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`attrObject`&emsp;&emsp;Object&emsp;&emsp;attr属性对象


#### setAutoAdjustIndex(autoAdjustIndex)

设置是否自动调整data在容器中索引顺序

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Description  
`autoAdjustIndex`&emsp;&emsp;Boolean&emsp;&emsp;是否自动调整data在容器中索引顺序


是否自动调整data在容器中索引顺序

#### setHierarchicalRendering(hierarchicalRendering)

设置容器是否为树层次渲染，  
GraphView 绘制层次逻辑是这样子的，HT 默认的 GraphView 是根据 DataModel.getDatas() 的顺序绘制图元，而 getDatas() 的图元索引顺序会一直自动调节变化，例如 Node 一般要呈现在其关联的 Edge 之上，孩子一般呈现在 Parent 之上，节点呈现在 Host 的吸附对象之上，包括 Group 的展开合并也会影响关联的 Edge 的显示顺序，所以对于网络拓扑图的应用一般由 HT 自行调节图元层次关系，不需要人工设置干预，操作点击时自定会有 sendToTop 的层次变化效果。

但对于绘制工控 HMI 之类的界面图形，往往和传统的绘图软件类似，先绘制的图元呈现在下面，后绘制的在上面，可通过右键菜单之类的调节上移或下移图元，所以 HT 增加了关闭自动 sendToTop 的开关，dataModel.setHierarchicalRendering(true)，这个参数默认为 false，设置为 true 时 GraphView 就会根据 dataModel.getRoots() 以及所有 Data.getChildren() 的父子关系来绘制

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`hierarchicalRendering`&emsp;&emsp;Boolean

#### size() → {Number}

返回当前容器中Data对象的总数

##### Returns:

Number

#### sm() → {[hc.SelectionModel](hc.SelectionModel.html)}

获取该容器的选择模型

##### Returns:

[hc.SelectionModel](hc.SelectionModel.html)

See:

*   [getSelectionModel](hc.DataModel.html#getSelectionModel)

#### toDatas(matchFunc, scope) → {[hc.List](hc.List.html)}

以matchFunc为过滤函数构建新的元素集合并返回

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`matchFunc`&emsp;&emsp;function&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;过滤函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域

##### Returns:

[hc.List](hc.List.html) -

元素集合

#### toJSON() → {Object}

将数据模型序列化成JSON格式对象

##### Returns:

Object -

JSON对象

#### umd(listener, scope)

删除模型中Data元素属性变化事件监听器，[removeDataPropertyChangeListener](hc.DataModel.html#removeDataPropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [removeDataPropertyChangeListener](hc.DataModel.html#removeDataPropertyChangeListener)

#### umh(listener, scope)

删除监听Data在DataModel中的层次(用于TreeView、TreeTableView等)变化事件的监听器，[removeHierarchyChangeListener](hc.DataModel.html#removeHierarchyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [removeHierarchyChangeListener](hc.DataModel.html#removeHierarchyChangeListener)

#### umm(listener, scope)

删除数据模型增删变化事件监听器，[removeDataModelChangeListener](hc.DataModel.html#removeDataModelChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [removeDataModelChangeListener](hc.DataModel.html#removeDataModelChangeListener)
