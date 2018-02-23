# CSS布局篇
### 目录
1. 常用的居中方法
  >- 水平居中
  >- 垂直居中
2. 单列布局
3. 二列&三列布局
  >- float + margin
  >- position + margin
  >- 圣杯布局
  >- 双飞翼布局
  >- flex布局
### 1. 常用的布局方法
居中在布局中很常见，我们假设DOM文档结构如下，子元素要在父元素中居中：
```
  <div class="parent">
    <div class="child"></div>
  </div>
```
#### 水平居中
子元素为行内元素还是块状元素，宽度一定还是宽度未定，采取的布局方案不同。下面进行分析：

- 行内元素：对父元素设置text-align: center;
- 定宽块状元素：设置左右margin值为auto;
- 不定宽块状元素：设置子元素为display:inline&inline-block，然后父元素设置text-align: center;
- 通用方案：flex布局，对父元素设置display: flex;justify-content: center;

#### 垂直居中
垂直居中对于子元素是单行内联文本、多行内联文本以及块状元素采用的方案是不同的。

- 父元素一定，子元素为单行内联文本：设置父元素的height等于行高line-height
- 父元素一定，子元素为多行内联文本：设置父元素的display:table-cell或inline-block，再设置vertical-align:middle;
- 块状元素:设置子元素position:fixed（absolute），然后设置margin:auto;
- 通用方案: flex布局，给父元素设置{display:flex; align-items:center;}。
