### 块格式上下文（Block Formatting Context, BFC）是web页面的可视化CSS渲染的部分，是块级盒分布发生的区域，也是浮动元素与其他元素交互的区域
#### 创建块格式化上下文的方式如下：

+ 根元素或其它包含它的元素
+ 浮动元素 (元素的 float 不是 none)
+ 绝对定位元素 (元素的 position 为 absolute 或 fixed)
+ 内联块元素 (元素具有 display: inline-block)
+ 表格单元格 (元素具有 display: table-cell，HTML表格单元格默认属性)
+ 表格标题 (元素具有 display: table-caption, HTML表格标题默认属性)
+ 匿名表格元素 (元素具有 display: table, table-row, table-row-group, table-header-group, table-footer-group [分别是HTML tables, table rows, table bodies, table headers and table footers的默认属性]，或 inline-table )
+ overflow 值不为 visible 的块元素，
+ display 值为 flow-root 的元素
+ contain 值为 layout, content, 或 strict 的元素
+ 弹性元素 (display: flex 或 inline-flex元素的子元素)
+ 网格元素 (display: grid 或 inline-grid 元素的子元素)
+ 多列容器 (元素的 column-count 或 column-width 不为 auto 即视为多列，column-count: 1的元素也属于多列)
+ 即便具有 column-span: all 的元素没有被包裹在一个多列容器中，column-span: all 也始终会创建一个新的格式化上下文


#### BFC特性
1. 内部的Box会在垂直方向，从顶部开始一个接一个地放置。
2. Box垂直方向的距离由margin决定。属于同一个BFC的两个相邻Box的margin会发生叠加
3. 每个元素的margin box的左边， 与包含块border box的左边相接触(对于从左往右的格式化，否则相反)。即使存在浮动也是如此。
4 .BFC的区域不会与float box叠加。
5. BFC就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素，反之亦然。
6. 计算BFC的高度时，浮动元素也参与计算。
