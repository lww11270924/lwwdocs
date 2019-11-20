
[hc](hc.html).SelectionModel()
------------------------------

#### new SelectionModel()

选择模型管理DataModel模型中Data对象的选择状态，  
每个DataModel对象都内置一个SelectionModel选择模型，  
控制这个SelectionModel即可控制所有绑定该DataModel的视图组件的对象选择状态，  
这意味着共享同一DataModel的组件默认就具有选中联动功能。  
  
如果希望某些组件不与其他组件选中联动，  
可通过调用view.setSelectionModelShared(false)，  
这样该view将创建一个专属的SelectionModel实例。

### Methods

#### addPropertyChangeListener(listener, scope, ahead)

增加自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [mp](hc.SelectionModel.html#mp)

#### addSelectionChangeListener(listener, scope, ahead)

增加监听器，监听选中变化事件

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头

See:

*   [ms](hc.SelectionModel.html#ms)

##### Example

    dataModel.addSelectionChangeListener(function(event) {
         //event格式：
         {
         	kind: "set",//事件类型set|remove|append|clear
         	datas: datas,//包含所有选中状态变化的数据元素，之前选中现在取消选中，和之前没选中现在被选中的数据元素
         }
    });

#### appendSelection(datas)

追加选中一个或多个数据元素，参数可为单个数据元素，也可为hc.List或Array数组

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html) | [hc.List](hc.List.html) | Array&emsp;&emsp;数据元素 

See:

*   [as](hc.SelectionModel.html#as)

#### as(datas)

追加选中一个或多个数据元素，参数可为单个数据元素，也可为hc.List或Array数组，[appendSelection](hc.SelectionModel.html#appendSelection)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html) | [hc.List](hc.List.html) | Array&emsp;&emsp;数据元素 

See:

*   [appendSelection](hc.SelectionModel.html#appendSelection)

#### clearSelection()

取消所有选中数据元素

See:

*   [cs](hc.SelectionModel.html#cs)

#### co(data)

判断data对象是否被选中，[contains](hc.SelectionModel.html#contains)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;要判断的data对象 

See:

*   [contains](hc.SelectionModel.html#contains)

#### contains(data)

判断data对象是否被选中

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;要判断的data对象 

See:

*   [co](hc.SelectionModel.html#co)

#### cs()

取消所有选中数据元素，[clearSelection](hc.SelectionModel.html#clearSelection)的缩写

See:

*   [clearSelection](hc.SelectionModel.html#clearSelection)

#### dm() → {[hc.DataModel](hc.DataModel.html)}

获取[DataModel](hc.DataModel.html)，[getDataModel](hc.SelectionModel.html#getDataModel)的缩写

##### Returns:

[hc.DataModel](hc.DataModel.html) - dataModel

See:

*   [getDataModel](hc.SelectionModel.html#getDataModel)

#### each(func, scope)

提供一个回调函数遍历此选中模型

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;遍历函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域

##### Example

    selectionModel.each(function(data) {
      console.log(data);
    });

#### fd() → {[hc.Data](hc.Data.html)}

返回首个被选中的数据元素，如果没有选中数据元素则返回空，此方法是[getFirstData](hc.SelectionModel.html#getFirstData)的缩写

##### Returns:

[hc.Data](hc.Data.html) - 首个被选中的数据元素

See:

*   [getFirstData](hc.SelectionModel.html#getFirstData)

#### getDataModel() → {[hc.DataModel](hc.DataModel.html)}

获取[DataModel](hc.DataModel.html)

##### Returns:

[hc.DataModel](hc.DataModel.html) - dataModel

See:

*   [dm](hc.SelectionModel.html#dm)

#### getFilterFunc() → {function}

返回选中过滤器函数  
  
有些数据元素不希望被用户选中，可以通过设置此过滤器实现

##### Returns:

function - 选中过滤器函数

See:

*   [setFilterFunc](hc.SelectionModel.html#setFilterFunc)

#### getFirstData() → {[hc.Data](hc.Data.html)}

返回首个被选中的数据元素，如果没有选中数据元素则返回空

##### Returns:

[hc.Data](hc.Data.html) - 首个被选中的数据元素

See:

*   [fd](hc.SelectionModel.html#fd)

#### getLastData() → {[hc.Data](hc.Data.html)}

返回最后被选中的数据元素，如果没有选中数据元素则返回空

##### Returns:

[hc.Data](hc.Data.html) - 最后被选中的数据元素

See:

*   [ld](hc.SelectionModel.html#ld)

#### getSelection() → {[hc.List](hc.List.html)}

获取所有被选中数据元素集合，注意不可直接对返回的集合进行增删操作，  
如果需要增删操作，应使用toSelection方法

##### Returns:

[hc.List](hc.List.html) - 被选中的数据元素集合

See:

*   [toSelection](hc.SelectionModel.html#toSelection)

#### getSelectionMode() → {String}

获取选中模式

##### Returns:

String - none|single|multiple

Default Value:

*   multiple

#### isEmpty() → {Boolean}

判断是否有选中的数据元素

##### Returns:

Boolean

#### isSelectable(data) → {Boolean}

判断数据元素是否可被选中

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`data`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html)&emsp;&emsp;要判断的数据元素 


##### Returns:

Boolean

#### ld() → {[hc.Data](hc.Data.html)}

返回最后被选中的数据元素，如果没有选中数据元素则返回空，[getLastData](hc.SelectionModel.html#getLastData)的缩写

##### Returns:

[hc.Data](hc.Data.html) - 最后被选中的数据元素

See:

*   [getLastData](hc.SelectionModel.html#getLastData)

#### mp(listener, scope, ahead)

增加自身属性变化事件监听器，[addPropertyChangeListener](hc.SelectionModel.html#addPropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


See:

*   [addPropertyChangeListener](hc.SelectionModel.html#addPropertyChangeListener)

#### ms(listener, scope, ahead)

增加监听器，监听选中变化事件，[addSelectionChangeListener](hc.SelectionModel.html#addSelectionChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域
`ahead`&emsp;&emsp;&emsp;&emsp;Boolean&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;是否将当前监听器插入到监听器列表开头


See:

*   [addSelectionChangeListener](hc.SelectionModel.html#addSelectionChangeListener)

##### Example

    dataModel.ms(function(event) {
         //event格式：
         {
         	kind: "set",//事件类型set|remove|append|clear
         	datas: datas,//包含所有选中状态变化的数据元素，之前选中现在取消选中，和之前没选中现在被选中的数据元素
         }
    });

#### removePropertyChangeListener(listener, scope)

删除自身属性变化事件监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [ump](hc.SelectionModel.html#ump)

#### removeSelection(datas)

取消选中数据元素，参数可为单个数据元素，也可为hc.List或Array数组

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`datas`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html) | [hc.List](hc.List.html) | Array&emsp;&emsp;数据元素 

See:

*   [rs](hc.SelectionModel.html#rs)

#### removeSelectionChangeListener(listener, scope)

删除监听选中变化事件的监听器

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [ums](hc.SelectionModel.html#ums)

#### rs(datas)

取消选中数据元素，参数可为单个数据元素，也可为hc.List或Array数组，[removeSelection](hc.SelectionModel.html#removeSelection)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`datas`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html) | [hc.List](hc.List.html) | Array&emsp;&emsp;数据元素 

See:

*   [removeSelection](hc.SelectionModel.html#removeSelection)

#### sa()

选中DataModel中的所有数据元素，[selectAll](hc.SelectionModel.html#selectAll)的缩写

See:

*   [selectAll](hc.SelectionModel.html#selectAll)

#### selectAll()

选中DataModel中的所有数据元素

See:

*   [sa](hc.SelectionModel.html#sa)

#### setFilterFunc(func)

设置选中过滤器函数  
  
有些数据元素不希望被用户选中，可以通过设置此过滤器实现

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;function&emsp;&emsp;选中过滤器函数 

##### Example

    //禁止选中name为test的数据元素
    selectionModel.setFilterFunc(function(data) {
     if (data.getName() === 'test') {
     	return false;
     } else {
     	return true;
     }
    });

#### setSelection(datas)

设置选中数据元素，参数可为单个数据元素，也可为hc.List或Array数组，[ss](hc.SelectionModel.html#ss)缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`datas`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html) | [hc.List](hc.List.html) | Array&emsp;&emsp;数据元素 

#### setSelectionMode(mode)

设置选中模式，可选值：

  
*   none:不可选中
  
*   single:只能选中一个数据元素
  
*   multiple:可以选中多个数据元素
  

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`mode`&emsp;&emsp;&emsp;String&emsp;&emsp;选中模式

Default Value:

*   multiple

#### size() → {Number}

获取选中模型中数据元素的个数

##### Returns:

Number

#### ss(datas)

设置选中数据元素，参数可为单个数据元素，也可为hc.List或Array数组，[setSelection](hc.SelectionModel.html#setSelection)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`datas`&emsp;&emsp;&emsp;[hc.Data](hc.Data.html) | [hc.List](hc.List.html) | Array&emsp;&emsp;数据元素 

#### toSelection() → {[hc.List](hc.List.html)}

获取所有被选中数据元素集合(新数组)

##### Returns:

[hc.List](hc.List.html) - 被选中的数据元素集合

See:

*   [toSelection](hc.SelectionModel.html#toSelection)

#### ump(listener, scope)

删除自身属性变化事件监听器，[removePropertyChangeListener](hc.SelectionModel.html#removePropertyChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [removePropertyChangeListener](hc.SelectionModel.html#removePropertyChangeListener)

#### ums(listener, scope)

删除监听选中变化事件的监听器，[removeSelectionChangeListener](hc.SelectionModel.html#removeSelectionChangeListener)的缩写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`listener`&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;监听器函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;监听器函数域

See:

*   [removeSelectionChangeListener](hc.SelectionModel.html#removeSelectionChangeListener)

