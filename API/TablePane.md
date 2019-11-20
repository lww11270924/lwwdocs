
[hc](hc.html)[.widget](hc.widget.html).TablePane(tableView)
-----------------------------------------------------------

#### new TablePane(tableView)

表格面板，组合了TableHeader和TableView两个子组件

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`tableView`&emsp;&emsp;[hc.widget.TableView](hc.widget.TableView.html)&emsp;&emsp;绑定的表格组件


### Methods

#### addColumns(columns)

以json的方式配置表格中的列(新增)，内部调用tableView的addColumns方法

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`columns`&emsp;&emsp;Array&emsp;&emsp;json列


##### Example

    //示例：
    tablePane.addColumns([{
    	name: 'id',
    	displayName: '序号'
    },
    {
    	name: 'background',
    	accessType: 'style'
    }
    ]);

#### addToDOM(parentNode)

将组件加入到指定的DOM元素底下，不指定则加入到 document.body 下

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`parentNode`&emsp;&emsp;DOM&emsp;&emsp;DOM元素,默认为 document.body

#### addViewListener(listener, scope, ahead)

监听视图事件，如布局、刷新等

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域  
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

#### getColumnModel() → {[hc.DataModel](hc.DataModel.html)}

获取列模型， 列模型用于存储Column列对象信息，内部调用tableView的getColumnModel方法

##### Returns:

[hc.DataModel](hc.DataModel.html)

#### getDataModel() → {[hc.DataModel](hc.DataModel.html)}

获取绑定的数据模型，内部调用tableView的getDataModel方法

##### Returns:

[hc.DataModel](hc.DataModel.html) - 数据模型

#### getHeighc() → {Number}

获取布局高度

##### Returns:

Number

#### getTableHeader() → {[hc.widget.TableHeader](hc.widget.TableHeader.html)}

获取表头组件

##### Returns:

[hc.widget.TableHeader](hc.widget.TableHeader.html)

#### getTableView() → {[hc.widget.TableView](hc.widget.TableView.html)}

获取表格组件

##### Returns:

[hc.widget.TableView](hc.widget.TableView.html)

#### getView() → {htmlDivElement}

获取组件的根层div

##### Returns:

htmlDivElement

#### getWidth() → {Number}

获取布局宽度

##### Returns:

Number

#### invalidate(delay)

无效组件，并调用延时刷新

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms) 

See:

*   [iv](hc.widget.TablePane.html#iv)

#### isDisabled() → {Boolean}

组件是否处于不可用状态，处于此状态时不能进行任何操作并且会遮挡一层蒙板

##### Returns:

Boolean

#### iv(delay)

无效组件，并调用延时刷新，[invalidate](hc.widget.TablePane.html#invalidate)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`delay`&emsp;&emsp;Number&emsp;&emsp;延迟刷新的间隔事件(单位:ms) 

See:

*   [invalidate](hc.widget.TablePane.html#invalidate)

#### removeViewListener(listener, scope)

删除视图事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;bject&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

#### setColumns(columns)

以json的方式配置表格中的列(设置)，内部调用tableView的setColumns方法

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`column`&emsp;&emsp;Array&emsp;&emsp;&emsp;json列 


##### Example

    //示例：
    tablePane.setColumns([{
    	name: 'id',
    	displayName: '序号'
    },
    {
    	name: 'background',
    	accessType: 'style'
    }
    ]);

#### setDisabled(value, iconUrl)

设置组件是否处于不可用状态，处于不可用状态时不能进行任何操作并且会遮挡一层蒙板

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`value`&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 是否禁用组件  
`iconUrl`&emsp;&emsp;String&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;蒙板上显示的icon的路径


#### setHeighc(v)

设置布局高度

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;高度值


#### setWidth(v)

设置布局宽度

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;宽度值

#### validate()

立刻刷新组件
