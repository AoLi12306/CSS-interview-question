### 题目

Given the HTML below:

```
<ul class="shopping-list" id="awesome">
    <li><span>Milk</span></li>
    <li class="favorite" id="must-buy"><span class="highlight">Sausage</span></li>
</ul>
```
What is the color of the text Sausage ?
```
#awesome .favorite:not(#awesome) .highlight {
    color: red;
}
#awesome .highlight:nth-of-type(1):nth-last-of-type(1) {
    color: blue;
}
```


## 解释

两个都能定位到Sausage

先说定位
1. 有没有空格的区别
.a .b是
```
<div class="a">
   <div class="b"></div>
</div>
```

.a.b是
```
<div class="a b"></div>
```


选择器的优先权
1.  内联样式表的权值最高 1000；

2.  ID 选择器的权值为 100

3.  Class 类选择器的权值为 10

4.  HTML 标签选择器的权值为 1
