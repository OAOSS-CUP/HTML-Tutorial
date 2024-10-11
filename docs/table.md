<div align="center">

# 表格

</div>

## 标签

 `table` 定义表格。表格由 `tr`（行）、`th`（表头单元格）和 `<td>`（数据单元格）组成

```html
<table border=1 width=100px height=100px>
  <tr>
    <th>姓名</th>
    <th>年龄</th>
    <th>性别</th>
  </tr>
  <tr>
    <td>思为</td>
    <td>18</td>
    <td>男</td>
  </tr>
  <tr>
    <td>子妍</td>
    <td>18</td>
    <td>女</td>
  </tr>
</table>
```

`width` 定义宽度

`height` 定义高度

`border` 定义边框

| 值 | 样式 |
| --- | --- |
| 0 | 无边框 |
| 1 | 单线 |
| 2 | 双线 |
| 3 | 粗线 |

同样的，表格也有 `align` 属性，将在下面与合并单元格一起演示

## 合并单元格

用 `colspan`（列） 和 `rowspan`（行） 来合并单元格

```html
<table border="1">
  <tr>
    <th>姓名</th>
    <th colspan="2">联系方式</th>
  </tr>
  <tr>
    <td rowspan="2">思为</td>
    <th colspan="2">110</th>
  </tr>
  <tr>
    <td colspan="2" align="center">120</td>
  </tr>
</table>
```