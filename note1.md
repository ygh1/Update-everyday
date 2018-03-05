### HTML单标签不用写/ 必须写/的是XHTML规范
### img标签当使用js赋值src属性是
```
  <img src="about:blank" alt="图片加载失败时显示的图片">
  或者
  加载一个一像素的base64透明图片
  <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7">
```
### 自定义标签，加上displat:block就跟div一样，但是不推荐使用
```
<self-div></self-div>
```
###使用https协议的网站，请求的http协议的图片，可能导致浏览器上https小锁没有
