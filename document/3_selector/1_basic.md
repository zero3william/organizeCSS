# 基礎選擇器

## 語法

```css
/* This is
a multi-line
comment */

selector {
    property: value; /* comment */
}
```

## 基本選擇器

標籤選擇器

```css
a {
    text-decoration: none;
}
```

類別選擇器

```css
.d-flex {
    display: flex !important;
}
```

ID 選擇器

```css
#stats {
    position: fixed;
}
```

萬用選擇器

```css
* {
    box-sizing: border-box;
}
```

## 群組選擇器

多個選擇器可以半形逗號（,）隔開

```css
selector1,
selector2,
selector3 {
    property: value;
}
```

- [選擇器小遊戲](https://flukeout.github.io/)