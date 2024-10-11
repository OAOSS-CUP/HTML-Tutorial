<div align="center">

# 表单

</div>

## 简述

表单是用来收集信息的，一般用于网页交互功能，比如登录框，输入框

表单由容器和控件组成，整个框架称为容器，里面的各种框和按钮称为控件

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

完整的表单包含两部分：标签，内容

以下是常用的内容组件

| 类型 | 用途 |
| --- | --- |
| `input type="text"` | 输入单行文本 |
| `input type="password"` | 输入密码，内容会被隐藏 |
| `input type="radio"` | 单选按钮，选择一个选项 |
| `input type="checkbox"` | 复选框，选择多个选项 |
| `input type="submit"` | 提交按钮，提交表单 |
| `input type="reset"` | 重置按钮，重置表单内容 |
| `input type="button"` | 按钮，执行自定义操作 |
| `select` | 下拉列表，选择一个选项 |
| `textarea` | 输入多行文本 |
| `button` | 按钮，用于提交表单或执行其他操作 |

```html
<form>
  <label for="username">用户名:</label>
  <input type="text" id="username" name="username" placeholder="请输入用户名"><br><br>

  <label for="password">密码:</label>
  <input type="password" id="password" name="password" placeholder="请输入密码"><br><br>

  <label>性别:</label>
  <input type="radio" name="gender" value="male"> 男
  <input type="radio" name="gender" value="female"> 女<br><br>

  <label>爱好:</label>
  <input type="checkbox" name="hobby" value="reading"> 阅读
  <input type="checkbox" name="hobby" value="traveling"> 旅行<br><br>

  <label for="country">国家:</label>
  <select id="country" name="country">
    <option value="china">中国</option>
    <option value="usa">美国</option>
    <option value="uk">英国</option>
  </select><br><br>

  <button type="submit">提交</button>
  <input type="button" value="点击我">
</form>
```

表单的内容非常多，也很复杂，想了解更详细的表单教程，请点[这里](https://blog.csdn.net/wshwsh_/article/details/131729849)