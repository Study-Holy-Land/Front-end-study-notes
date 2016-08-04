### 表格

0. 表格不换行显示，列宽自适应，内容过长显示省略号

给表格添加如下 CSS / LESS 样式即可
``` less
table {
  table-layout:fixed;

  th, td {
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
  }
}
```

