
#### new List()

集合类，提供比原生数组更便捷的API

### Methods

#### add(item, index)

增加元素

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`item`&emsp;&emsp;&emsp; &emsp; Object&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;新元素  
`index`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;插入索引

#### addAll(array)

将一批元素加入到当前集合中

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp; &emsp;&emsp; Description  
`array`&emsp;&emsp;&emsp;Array | [hc.List](hc.List.html)&emsp;&emsp;元素数组或集合 

#### clear()

清空集合

#### contains(item)

判断当前集合是否包含参数元素

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`item`&emsp;&emsp;&emsp;Object&emsp;&emsp;是否包含此元素 

#### each(func, scope)

提供一个回调函数遍历此集合

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;&emsp; function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;遍历函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域

##### Example

    list.each(function(item) {
      console.log(item);
    });

#### get(index) → {Object}

返回索引位置的的元素

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`index`&emsp;&emsp;&emsp;Number&emsp;&emsp;索引 

##### Returns:

Object - 处于索引位置的元素

#### getClass() → {function}

获取类声明(构造函数)

##### Returns:

function - 类声明(构造函数)

#### getClassName() → {String}

获取类全名

##### Returns:

String - 类全名

#### getSuperClass() → {function}

获取父类声明(构造函数)

##### Returns:

function - 父类声明(构造函数)

#### indexOf(item) → {Number}

获得参数元素的索引

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`item`&emsp;&emsp;&emsp;Object&emsp;&emsp;元素 

##### Returns:

Number - 元素的索引

#### isEmpty() → {Boolean}

判断集合是否为空

##### Returns:

Boolean - 集合是否为空

#### remove(item) → {Number}

将参数元素从集合中删除

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`item`&emsp;&emsp;&emsp;Object&emsp;&emsp;要删除的元素 

##### Returns:

Number - 要删除的元素的索引

#### removeAt(index) → {Ojbect}

删除索引位置的元素

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`index`&emsp;&emsp;&emsp;Number&emsp;&emsp;要删除的索引  

##### Returns:

Ojbect - 删除的元素

#### reverse()

将集合中的元素顺序倒序排序

#### reverseEach(func, scope)

提供一个回调函数倒序遍历此集合

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;&emsp; function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;遍历函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域


##### Example

    list.reverseEach(function(item) {
      console.log(item);
    });

#### set(index, item)

设置索引处的元素

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`index`&emsp;&emsp;&emsp;Number&emsp;&emsp;索引，如果此索引处存在元素则将其替换  
`item`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;新元素 


#### size() → {Number}

获取集合中的元素数

##### Returns:

Number - 集合中的元素数

#### slice(start, end) → {[hc.List](hc.List.html)}

提取集合中的部分元素组成一个新集合并返回

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`start`&emsp;&emsp;&emsp;Number&emsp;&emsp;开始索引(包含)  
`end`&emsp;&emsp;&emsp;&emsp;Number&emsp;&emsp;结束索引(不包含) 

##### Returns:

[hc.List](hc.List.html) - 新集合

#### sort(sortFunc) → {[hc.List](hc.List.html)}

根据参数函数将元素排序

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`sortFunc`&emsp;&emsp;&emsp;function&emsp;&emsp;排序函数 

##### Returns:

[hc.List](hc.List.html) - 自身

##### Example

    list.sort(function(a, b) {
      if (a.age === b.age) return 0;
      if (a.age > b.age) return 1;
      return -1;
    });

#### toArray(matchFunc, scope) → {Array}

以matchFunc为过滤函数构建新的元素数组

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`matchFunc`&emsp;&emsp;function&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;过滤函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域


##### Returns:

Array - 元素数组

##### Example

    var array = list.toArray(function(item) {
       if (item.a('visible')) {
       	return true;
       }
    });

#### toList(matchFunc, scope) → {[hc.List](hc.List.html)}

以matchFunc为过滤函数构建新的元素集合

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`matchFunc`&emsp;&emsp;function&emsp;&emsp;&emsp;\<optional>&emsp;&emsp;过滤函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;&emsp;\<optional> &emsp;&emsp;函数域

##### Returns:

[hc.List](hc.List.html) - 元素集合

##### Example

    var list = list.toList(function(item) {
       if (item.a('visible')) {
       	return true;
       }
    });

#### toString() → {String}

重写js默认的toString

##### Returns:

String
