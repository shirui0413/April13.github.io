### css选择器（セレクター）

CSS选择器参考手册

```
https://www.runoob.com/cssref/css-selectors.html
```



#### .classname

Select and style all elements with class=“intro"

```
.intro
{
	background-color:yellow;
}

<div class="intro">                     // yellow
  <p>My name is Donald.</p>
  <p>I live in Duckburg.</p>
</div>
```



#### p.hometown

Style all <p> elements with class="hometown"

```
p.hometown
{
	background-color:yellow;
}

<p>My name is Donald.</p>
<p class="hometown">I live in Ducksburg.</p>     // yellow

```



#### div .hometown     中间有半角空格

Style all elements in div with class="hometown"

```
div .hometown
{ 
	background:red;
}

<div> 
	<p class = "hometown">i am red </p>               // red
	<div class = "hometown">i am red ,too </div>      // red 
	<p>hehehe, i am black</p>
	I also live in Ducksburg.
</div>
```



#### &符号的意思

.bordered.float 是串联选择器，作用在同一标签上
.bordered .top 是后代选择器，作用在不同标签上

```
.bordered {
  &.float {
    float: left; 
  }
  .top {
    margin: 5px; 
  }
}
```

等同于

```
.bordered.float {
  float: left; 
}
.bordered .top {
  margin: 5px;
}
```





