## html

### 1. 书写规范

```
<!DOCTYPE html>   约束，声明              
<html lang="en">  htlm标签，表示html的开始  "en"表示英文，"zh_CN"表示中文； html标签一般分为两部分，head和body
<head>   表示头部信息，一般包含三部分，title标签、css样式、js代码
    <meta charset="UTF-8">  表示当前页面使用UTF-8字符集(最通用的)。中国用的是
    <title>标题</title>  表示标题
</head>  
<body>  body标签是整个html页面显示的主体内容(所有空白界面浏览器打开的界面都是body主体)
    主体内容
</body>
</html>
```

### 2. 标签

####      1. 标签介绍

1. 标签的格式: <标签名>封装的数据 </标签名>

2. 标签名大小写不敏感。 

3. 标签拥有自己的属性。 

   ​    属性是一个名值对(x=y)，属性用来设置标签中的内容如何显示

   ​      i. 基本属性：[^bgcolor ]="red"  可以修改简单的样式效果 

   ​     ii. 事件属性： onclick="alert('你好！');"  可以直接设置事件响应后的代码。

4. 标签又分为，单标签和双标签。 

   ​     i. 单标签格式： <标签名 >   `br 换行`  `hr 水平线`  `input `

   ​    ii. 双标签格式: <标签名> ...封装的数据...</标签名>

#### 2. 标签语法

1. 标签不能交叉嵌套
2. 标签必须正确关闭
3. 属性必须有值，属性值必须加引号
4. 注释不能嵌套

#### 3. 常用标签

##### 1. font字体标签

  `<font color="red" face="宋体" size="3"> 想要写的内容</font>`

##### 2. 特殊字符

一些字符在html中，会被用到格式上，例如`<br>`它只会换行，不会显示`<br>`

![image-20201116213307461](C:\Users\chen'na'a'a\AppData\Roaming\Typora\typora-user-images\image-20201116213307461.png)

*在html中，连续空格只会保留一个。所以像想要多个空格，要用字符实体*

#####  3. 标题标签

`h1  h2  h3  h4  h5  h6 `

> align是对齐属性
>
> left           左对齐(默认) 
>
> center     居中
>
> right        右对齐

`<h1 align="left">标题1</h1>`

##### <font color="red">4. 超链接</font>

> <!-- a 标签是超链接
>      herf 属性设置连接的地址
>      target 属性设置哪个目标进行跳转
>         _self    表示当前页面(默认值)
>         _blank   表示打开新页面进行跳转
> -->

`<a herf= "http://localhost:8080" target="_self">百度</a>`

##### 5. 列表标签

* 无序列表

```
ul 是无序列表
   type 属性可以修改列表前面的符号
li 是列表项
```

* 有序列表

`ol 是有序列表`

##### 6. img标签

> img 是图片标签，用来显示图片
>
> ​	 src 属性设置图片路径
>
> ​	width 属性设置图片宽度
>
> ​	height 属性设置图片高度
>
> ​	border 属性设置图片边框大小
>
> ​	alt 属性设置当前路径找不到图片时，用来代替显示的文本内容

```
在web中路径分为相对路径和绝对路径
	相对路径：
	.	表示当前文件所在的目录
	..	表示当前文件所在的上一级目录
	绝对路径
	http://ip:port/工程名/资源路径
```

##### 7. 表格标签

> table 标签是表格标签
>
> ​	width 属性设置图片宽度
>
> ​	height 属性设置图片高度
>
> ​	border 属性设置图片边框大小
>
> ​	align 设置表格相对于页面的对齐方式
>
> ​	cellspacing 设置单元格间距

`<table align="center" border="1" width="300" height="300" cellspacing="0">`

> tr 是行标签   （表格有若干行）
>
> th 是表头标签   (可以横着，可以竖着)
>
> td 是单元格标签 
>
> ​	align 设置单元格文本对齐方式
>
> ​	b 是加粗标签

```
<tr>
    <th>表头1</th>
    <th>表头2</th>
    <th>表头3</th>
</tr>
<tr>
    <td align="center">1.1</td>
    <td>1.2</td>
    <td>1.3</td>
</tr>
```

*align放到td里面，1.1这一个单元格居中；如果放到tr里面，这一行所有单元格都居中*

> <font color="red">跨行跨列表格</font>
>
> ​	colspan 属性设置跨列
>
> ​	rowspan属性设置跨行

```
<tr>
    <td colspan="2">1.1</td>   (代表第一行第一列的单元格占了两列)
    <td>1.2</td>
    <td>1.3</td>
</tr>
<tr>
    <td rowspan="3">2.1</td>   (代表第二行第一列的单元格占两行)
    <td>2.2</td>
    <td>2.3</d>
</tr>
```

##### 8.iframe框架标签(内嵌窗口)

*可以在一个html页面上，打开一个小窗口，去加载一个单独的页面*

> 如果要加载多个可供选择的页面，iframe和a标签组合使用
>
> 使用步骤：
>
> 1.在iframe标签中使用name属性定义一个名称
>
> 2.在a标签target属性上设置iframe的name属性值
>
> ```
> <iframe name="abc"></iframe><br/>
> <a href="hello.html" target="abc">hello页面</a>
> ```

##### <font color="red">9.表单标签</font>

*表单是html页面中，用来收集用户信息的所有元素集合，然后把这些信息发送给服务器*

```
form 标签就是表单
	input type="text"       文件输入框  value设置默认显示内容
	input type="password"   密码输入框  value设置默认显示内容
	input type="radio"      单选框(单选时要用name对其进行分组，只有同一组的两个元                             素，才能保证只能同时选一个)  checkde="checked"表                             示默认选中
	input type="checkbox"   复选框    checkde="checked"表示默认选中
	input type="reset"      重置按钮    value修改按钮上的文本
	input type="submit"     提交按钮    value修改按钮上的文本
	input type="file"       文件上传域
	input type="submit"     隐藏域 (要发送某些信息，不需要用户参与。提交的时候会                             同时发送给服务器)
	
	select                  下拉列表框  option标签是下拉列表框选项 
	                         select="selected"设置默认选中
	
	textaera                表示多行文本输入框(起始和结束标签中的内容是默认值)
                            rows 设置可以显示几行
                            cols 设置每行显示几个字符
```

***(1)先把要显示的内容写出来***

```
    用户名称：<input type="text" /><br/>
    用户密码：<input type="password"/><br/>
    确认密码：<input type="password"/><br/>
    性别：<input type="radio" name="sex" checked="checked">男<input type="radio" name="sex"/>女<br/>
    兴趣爱好：<input type="checkbox"/>java<input type="checkbox"/>c++<input type="checkbox"/>PHP<br/>
    国籍：<select>
    <option>中国</option>
    <option>美国</option>
    <option>日本</option>
</select><br/>
    自我评价：<textarea rows="10" value="20"></textarea><br/>
    <input type="reset" value="重置"/><br/>
    <input type="submit" value="提交"><br/>
```

***(2)一般表单用表格形式写，调整排版***

```
<table>
        <tr>
            <td>用户名称：</td>
            <td>
                <input type="text" />
            </td>
        </tr>
        <tr>
            <td>用户密码：</td>
            <td><input type="password"/></td>
        </tr>
```

***(3)提交细节***

1. 表单提交没有发送给服务器的情况：

   + 表单项没有name属性值(<font color="red">所以所有项都要加name</font>)
   + 单选、复选、下拉列表中的option标签需要添加value属性

2. form标签属性

+ action属性设置提交的服务器地址

+ method属性设置提交的方式为get(默认)或post

  + get请求

    + 浏览器地址栏中的地址是：属性[+?+请求参数]

      ​	请求参数的格式为：name=value&name=value

    + 不安全

    + 有数据长度的限制

  + post请求

    + 浏览器地址栏中只有action属性值

     + 相对于get请求要安全

     + 理论上没有数据长度的限制

完整

>```
><form action="http://baidu.com" method="post">
><input type="hidden" name="action" value="login"/>
><h1 align="center">用户注册</h1>
><table>
>   <tr>
>       <td>用户名称：</td>
>       <td>
>           <input type="text" name="username" />
>       </td>
>   </tr>
>   <tr>
>       <td>用户密码：</td>
>       <td><input type="password" name="password"/></td>
>   </tr>
>   <tr>
>       <td>确认密码：</td>
>       <td><input type="password" name="qpassword"/></td>
>   </tr>
>   <tr>
>       <td>性别：</td>
>       <td>
>           <input type="radio" name="sex" value="boy"/>男<input type="radio" name="sex" value="girl"/>女
>       </td>
>   </tr>
>   <tr>
>       <td>兴趣爱好：</td>
>       <td>
>           <input type="checkbox" name="hobby" value="java"/>java
>           <input type="checkbox" name="hobby" value="cpp"/>c++
>           <input type="checkbox" name="hobby" value="php"/>PHP
>       </td>
>   </tr>
>   <tr>
>       <td>国籍：</td>
>       <td>
>           <select name="country">
>               <option value="none">--请选择国籍--</option>
>               <option value="cn">中国</option>
>               <option value="usa">美国</option>
>               <option value="jp">日本</option>
>           </select>
>       </td>
>   </tr>
>   <tr>
>       <td>自我评价：</td>
>       <td><textarea name="desc" rows="10" value="20">默认值在这</textarea></td>
>   </tr>
>   <tr>
>       <td>
>           <input type="reset" value="重置"/>
>       </td>
>       <td>
>           <input type="submit" value="提交"/>
>       </td>
>   </tr>
></table>
></form>
>```

##### 10.其他标签

(1)div  默认独占一行

(2)span 它的长度是封装数据的长度

(3)p段落标签  默认会在段落上方或下方各空出一行来(如果已有就不再空)

[^bgcolor ]: 背景颜色





## css

### 1.css和html的结合

+ 第一种：

```
<div style="border:1px solid red;">标签1</div>
<div style="border:1px solid red;">标签2</div>
```

*想给某一个加样式，直接加一个div标签，然后加格式*

+ 第二种

```
<head>
	<style type="text/css">
		div{
			border:1px solid red;
		}
	</style>
</head>
<body>
	<div>标签1</div>
	<div>标签2</div>
</body>
```

*将style标签写着head中，<body>中所有的相关属性都变为设置好的样式

+ 第三种

将css样式写成一个单独的css文件

```
div {
	border:1px solid red;
}
```

html文件

```
<link rel="stylesheet" type="text/css" href="css文件名"/>
```

*link标签可以写在<head>里，也可以写在想使用的某一行里*

### 2.css选择器

**2.1 标签名选择器**

格式：

```
标签名{
	属性:值1  值2；
}
```

**2.2 id选择器**

格式：

```
<head>
#id属性值{
	属性：值；
}
</head>
```

```
<body>
<标签名 id="id属性值">
</body>
```

<font color="red">id选择器在一个html文档中，只能使用一次</font>

**2.3 class选择器**

格式：

```
<head>
.class属性值{
	属性：值；
}
</head>
```

```
<body>
<标签名 class="class属性值">
</body>
```

<font color="red">选择器要写在head中，但是是css样式，所以要正在选择器前加`<style type="text/css">`</font>

### **

一、符号问题：

1、属性和标签名或和其他属性应该使用空格隔开

2、属性值应该用引号引起来，单双引号都可以
