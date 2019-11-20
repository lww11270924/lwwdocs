
#### new EdgeGroup()

连线分组

### Methods

#### each(func, scope)

提供一个回调函数遍历此分组的所有连线

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;遍历函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;\<optional> &emsp;函数域

##### Example

    edgeGroup.each(function(edge) {
      console.log(edge);
    });

#### eachSiblingEdge(func, scope)

提供一个回调函数遍历相同起始和目标图元之间其它分组中的连线

##### Parameters:
>Name&emsp;&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;&emsp;Attributes&emsp;&emsp;Description  
`func`&emsp;&emsp;&emsp;&emsp;function&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;遍历函数  
`scope`&emsp;&emsp;&emsp;&emsp;Object&emsp;&emsp;&emsp;\<optional> &emsp;函数域

##### Example

    edgeGroup.eachSiblingEdge(function(edge) {
      console.log(edge);
    });

#### get(index) → {[hc.Edge](hc.Edge.html)}

根据索引获取分组中的连线

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`index`&emsp;&emsp;&emsp;Number&emsp;&emsp;索引  

##### Returns:

[hc.Edge](hc.Edge.html)

#### getEdges() → {[hc.List](hc.List.html)}

获取分组中所有连线

##### Returns:

[hc.List](hc.List.html)

#### getSiblings() → {[hc.List](hc.List.html)}

获取相同起始和目标图元之间的其它分组

##### Returns:

[hc.List](hc.List.html)

#### indexOf(edge) → {Number}

获取参数连线在分组中的索引

##### Parameters:
>Name&emsp;&emsp;&emsp;Type&emsp;&emsp;&emsp;Description  
`edge`&emsp;&emsp;&emsp;[hc.Edge](hc.Edge.html)&emsp;&emsp;连线 

##### Returns:

Number

#### size() → {Number}

获取分组中的连线数量

##### Returns:

Number
