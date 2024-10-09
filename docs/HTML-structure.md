<div align="center">

# HTML 结构

</div>

## 框架

```html
<!DOCTYPE html>
<html>
    <head>
        ...
    </head>
    <body>
        ...
    </body>
</html>
```

## 详解

### DOCTYPE

```DOCTYPE```是document type的缩写，**必须写**，要写在**整个文档的最前面**

```html
<!DOCTYPE html>
```

### html, head, body

```html```定义了HTML文档，**必须**从头括到尾
```head```定义了HTML的头部（不可视范围），**必须**写在```html```的最前面
```body```定义了HTML的主体（可视范围），写在```head```的后面

### title

```title```定义了HTML的标题，显示于网页的标题栏，如果写```head```就**必须**写```title```

建议大家一定要写```title```，这有利于搜索引擎的优化（SEO）
```html
<!DOCTYPE html>
<html>
    <head>
        <title>Hello world!</title>
    </head>
    <body>
        Hello world!
    </body>
</html>
```

### meta

```meta```定义了HTML的属性，关键词等。例如，网页常用的编码格式是```UTF-8```（也有的用```gbk```），呈现在meta中就是

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>Hello world!</title>
    </head>
    <body>
        Hello world!
    </body>
</html>
```
