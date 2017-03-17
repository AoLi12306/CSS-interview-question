rel: http://www.programcreek.com/2010/05/inner-div-float-out-of-outer-div-clearing-floats-problem/


目标样式: <br>
![alt text](http://www.programcreek.com/wp-content/uploads/2010/05/clear.png)

如果直接用下面代码
```
<div class="out">
  <div class="inner1"></div>
  <div class="inner2"></div>
</div>
```
inner1和inner2会从上往下,而不会从左往右. <br>
为了从左往右,  inner1和inner2要用float. <br>
float会有个问题， 里层的inner1和inner2会脱离外层outer的文件流导, inner会出现在outer的broder的下面而不是里面(看起来像最外层的div会撑不开)




方法一： clear：both；  <br>
在outer添加之后，outer会向下clear float
