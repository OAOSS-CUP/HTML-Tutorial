<div align="center">

# 表单

</div>

## 简述

表单是用来收集信息的，一般用于网页交互功能，比如登录框，输入框

```html
<form action="https://oct0pu5.cn" method="post" name="MyForm">
```

`action` 定义服务器链接

`name` 是这个表单的名字

`method` 是数据的提交方式，包含以下两种

| 值 | 特点 |
| --- | --- |
| get | 可视，用于少量数据 |
| post | 不可视，用于大量数据 |

**出于安全性考虑，建议选择 `post`**

## 结构

完整的表单包含三部分：标签，控件，按钮

## 控件

### input

`input` 定义输入控件。根据不同的 `type` 值，控件可以是文本字段、复选框、掩码后的文本控件、单选按钮、按钮等等

| 控件 | type值 | 描述 |
| --- | --- | --- |
| 文本框 | `text` | 输入单行文本 |
| 密码框 | `password` | 输入密码，内容会被隐藏 |
| 单选按钮 | `radio` | 单选按钮，可以选择一个选项 |
| 复选框 | `checkbox` | 复选框，可以选择多个选项 |
| 提交按钮 | `submit` | 提交表单 |
| 重置按钮 | `reset` | 重置表单内容 |
| 图片按钮 | `image` | 图像形式的提交按钮 |
| 普通按钮 | `button` | 普通按钮，用于执行自定义操作（与 `JS` 共同启动脚本 |
| 隐藏文本 | `hidden` | 隐藏的输入字段 |
| 文件 | `file` | 文件上传控件 |

```html
 <form action="" method="get">
    <!-- name可以为表单控件起名，其名称在提交表单时会传输给服务器 -->
    <!-- value可以为文本框赋默认值 -->
    <!-- readonly表示只读 -->
    <!-- required表示该信息必填 和表单域结合可以呈现验证内容 -->
    <!-- disabled表示禁用 在页面中呈现灰色 -->
    <!-- placeholder可以指定文本框输入前的信息提示 -->

    <label for="text">*普通文本框： </label><input type="text" name="text" id="text"><br>

    <!-- type="password" 表示密码文本框，其输入的内容以密文的形式出现 -->
    密码： <input type="password" name="password"><br>

    <!-- type="number" 表示数字数据库，只允许用户输入数字，小数或者负数 -->
    数字： <input type="number" name="number"><br>

    日期： <input type="date" name="date"><br>

    <!-- type="tel" 在移动端会调起数字键盘 -->
    <!-- maxlength="11"表示输入最大的字符数 -->
    电话：<input type="tel" name="tel" maxlength="11"><br>

    <!-- type="email" 在移动端会显示@ -->
    邮箱： <input type="email" name="email"><br>

    <!-- type="radio" 使用name属性可以让单选按钮进行分组 name相同时一次只能选择一个 -->
    <!-- checked表示默认选中 -->
    单选框：<label><input type="radio" name="sex" value="男" checked>男</label>
    <label><input type="radio" name="sex" value="女">女</label><br>
    复选框：<input type="checkbox" name="hobby" value="足球">足球
    <input type="checkbox" name="hobby" value="排球">排球
    <input type="checkbox" name="hobby" value="乒乓球">兵乓球<br>

    搜索框：<input type="search" name=""><br>

    <!-- type="button"在value属性中可以显示按钮的内容 -->
    普通按钮：<input type="button" value="普通按钮"><br>

    <!-- type="submit" 结合(form)表单域实现提交效果
	在表单中 submit 点击之后会自从触发提交行为，会向action指定的地址提交，请求方式为method指         定的方式通常表单提交为post
	-->
    提交：<input type="submit" value="提交"><br>

    <!-- 图片会被当作一个按钮 -->
    <input type="image" src="思为哥哥.png" height="50">

    <!-- reset表示重置按钮，会让表单回到默认值-->
    重置：<input type="reset" value="重置"><br>

    <!-- accept属性可以过滤文件 -->
    文件：<input type="file" name="file" accept="img/*"><br>

    <!-- 隐藏域在页面不可见，但是可以随着表单一起提交给服务端-->
    隐藏域：<input type="hidden"><br>
</form>
```

### 其他

`textarea` 定义多行输入文本框，可以容纳无限文本，通过 `cols` `rows` 控制大小

```html
<textarea name="" id="" cols="30" rows="10"></textarea>
```

`label` 定义一段文字，通常用于告知用户输入框的作用

```html
<label><input type="checkbox" name="开源" value="开源">开源</label>
```

`select` 定义下拉选项列表

`option` 定义每个选项

```html
<!-- selected指定默认选中 -->
<!-- optgroup可以进行分组 label="理科"属性命名分组的标题 -->
请选择课程:
<select name="course">
    <optgroup label="理科"></optgroup>
    <option value="高等数学">高等数学</option>
    <option value="离散数学">离散数学</option>
    <option value="线性代数" selected>线性代数</option>
    <option value="概率论">概率论</option>
</select>
```

`button` 定义一个按钮，这个按钮中可以放任何内容

`type` 定义了按钮形式，**一定要规定 `type` 属性！**

```html
    <button type="button">按钮</button> 
    <button type="submit">提交</button>
    <button type="reset">重置</button> 
```

`fieldset` 对表单内控件分组

`legend` 为 `fieldset` 定义标题

```html
<fieldset>
	<legend>测试</legend>
	<p>
		<label for="username">用户名：</label><input type="text" name="username" id="username">
	</p>
	<p>
		密码：<input type="password" name="password" placeholder="请输入密码">
	</p>
</fieldset>
```

表单的内容非常多，也很复杂，想了解更详细的表单教程，请点[这里](https://blog.csdn.net/wshwsh_/article/details/131729849)