
[hc](hc.html)[.widget](hc.widget.html).PropertyPane(dataModel)
--------------------------------------------------------------

#### new PropertyPane(dataModel)

性面板组件，该组件增强了hc.widget.PropertyView组件的展示及操作功能，提供了可视化的切换排序、过滤和分组的界面功能。使用需引入 hc-propertypane.js

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Description  
`dataModel`&emsp;&emsp;&emsp;[hc.DataModel](hc.DataModel.html)&emsp;&emsp;绑定的数据模型 

### Methods

#### addProperties(painter)

可批量增加属性信息，该函数是对[PropertyView.addProperties](hc.widget.PropertyView.html#addProperties)的包装

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`painter`&emsp;&emsp;&emsp;function&emsp;&emsp;Painter类 

##### Example

    //Painter示例：
    graphView.addBottomPainter(function(g){
        g.fillStyle = '#000000';
        g.fillRect(0, 0, 100, 100);
    });

#### getCategoryIcon() → {color}

获取工具条分组按钮图标

##### Returns:

color

#### getHeaderHeighc() → {Number}

获取表头高度

##### Returns:

Number

#### getHeaderLabelAlign() → {String}

获取表头文字水平对齐方式，默认为 center

##### Returns:

String

#### getHeaderLabelColor() → {color}

获取表头文字颜色

##### Returns:

color

#### getHeaderLabelFont() → {String}

获取表头文字字体

##### Returns:

String

#### getHeaderLabels() → {Array}

获取表头文字内容

##### Returns:

Array

#### getIndent() → {Number}

获取工具条图片缩进

##### Returns:

Number

#### getPropertyView() → {[hc.widget.PropertyView](hc.widget.PropertyView.html)}

获取hc.widget.PropertyView对象

##### Returns:

[hc.widget.PropertyView](hc.widget.PropertyView.html)

#### getSelectBackground() → {color}

获取选中背景

##### Returns:

color

#### getSortFunc() → {function}

获取工具条排序逻辑函数

##### Returns:

function

#### getSortIcon() → {Sting}

获取工具条排序按钮图标

##### Returns:

Sting

#### getToolbarHeighc() → {Number}

获取工具条高度

##### Returns:

Number

#### isCaseSensitive() → {Boolean}

获取过滤是否考虑大小写

##### Returns:

Boolean

#### setCaseSensitive(v)

设置过滤是否考虑大小写

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Boolean

#### setCategoryIcon(v)

设置工具条分组按钮图标

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;String

#### setHeaderHeighc(v)

设置表头高度

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number

#### setHeaderLabelAlign(v)

设置表头文字对齐方式

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;String&emsp;&emsp;left|center|righc

#### setHeaderLabelColor(v)

设置表头文字颜色

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;color

#### setHeaderLabelFont(v)

设置表头文字字体

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;String

#### setHeaderLabels(v)

设置表头文字内容，例如setHeaderLabels(\['属性', '值'\])

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Array

#### setIndent(v)

设置工具条图片缩进

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number

#### setSelectBackground(v)

设置选中背景

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;color

#### setSortFunc(v)

设置工具条排序逻辑函数

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;function

#### setSortIcon(v)

设置工具条排序按钮图标

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;String

#### setToolbarHeighc(v)

设置工具条高度

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;Description  
`v`&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Number

