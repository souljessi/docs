
## 项目背景

### 数字化城市管理新模式的概念
数字化城市管理新模式就是采用万米单元网格管理法和城市部件、事件管理法相结合的方式；应用、整合多项数字城市技术；研发信息采集器“城管通”，创新信息实时采集传输的手段；创建城市管理监督中心和指挥中心两个轴心的管理体制；再造城市管理流程；从而实现精确、敏捷、高效、全时段、全方位覆盖的城市管理模式。





'********华丽的风格线，下面是内容展示出了我牛逼的文采和文档词法高亮技巧，支持超链接，关键词变色，标签插入，这篇文档纯README.md编写，可以解析出html代码，也可以像文员一样手搓文字*********'


## 写在前面
此组件仅提供一个创建TreeTable的解决方案

## prop说明
### data
  **必填**


### columns
  列属性,要求是一个数组

  1. text: 显示在表头
  2. value: 对应data的key，treeTable将显示相应的value
  3. width: 每列的宽度，为一个数字
  如果你想要每个字段都有自定义的样式或者嵌套其他组件，columns可不提供，直接像在el-table一样写即可，如果没有自定义内容，提供columns将更加的便捷方便
  ```javascript
  [{
    value:string,
    text:string,
    width:number
  },{
    value:string,
    text:string,
    width:number
  }]
  ```

### expandAll
  是否默认全部展开，boolean值，默认为false

### evalFunc
  解析函数，function，非必须

  如果不提供，将使用默认的evalFunc

  如果提供了evalFunc,那么会用提供的evalFunc去解析data，并返回treeTable渲染所需要的值。如何编写一个evalFunc，请参考此目录下的*eval.js*

### evalArgs
  解析函数的参数，是一个数组

  **请注意，自定义的解析函数参数第一个为this.data，你不需要在evalArgs填写。**

  如你的解析函数需要的参数为`(this.data,1,2,3,4)`，那么你只需要将`[1,2,3,4]`赋值给`evalArgs`就可以了

 ## slot
 请参考`customTreeTable`

