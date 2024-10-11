<div align="center">

# 图片、超链接、路径

</div>

## 图片

`img` 定义图片

```html
<img src="思为哥哥.png" alt="思为哥哥好帅" title="思为哥哥" width="300px" height="300px" >
```

`src` 是图片源文件，可以是本地文件，也可以是网页链接

`alt` 是图片加载不出来时显示的文字

`title` 是鼠标悬停在图片上显示的文字

`width` 是图片宽度

`height` 是图片高度

## 超链接

`a` 定义超链接

超链接可以是文字，图片等，点击超链接后可以跳转到文档的某个位置或其他文档或网页链接

```html
<a href="www.oct0pu5.cn">点我</a>
```

### 颜色变化

> [!IMPORTANT]\
> GitHub 不支持内联HTML样式，因此无法看到下方的颜色和下划线，如果想看请自行下载到本地查看

未点过的超链接是 <span style="color:blue; text-decoration:underline;">蓝色带下划线</span>

点过的超链接是 <span style="color:purple; text-decoration:underline;">紫色带下划线</span>

点超链接的时候是 <span style="color:red; text-decoration:underline;">红色带下划线</span>

### 鼠标变化

鼠标置于超链接上，会变成一只手

![1](https://github.com/user-attachments/assets/307a3ae7-986d-49cf-bf9a-b22244446ba4)

## 路径

路径主要分为三种：绝对路径、相对路径、网络路径

### 绝对路径

绝对路径是从盘符到具体文件的路径

```
D:\Pictures\思为哥哥帅照
```

### 相对路径

相对路径是两个文件的路径关系，不以根目录开始。

如果我们有如下文件结构

```
root/
    CUPDS.html
    docs/
        README.md
        HTML教程.md
    asset/
        思为哥哥.png
```

而我们现在位于README.md中，那么 `CUPDS.html`、`HTML教程.md`、`思为哥哥.png` 的相对路径分别是

```
/CUPDS.html
```

```
HTML教程.md
```

```
/asset/思为哥哥.png
```

### 网络路径

也就是网页链接，比如

```
https://oct0pu5.cn
```