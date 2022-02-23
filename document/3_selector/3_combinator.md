# 組合選擇器

### 後代選擇器

```css
Ancestor Target {
    property: value;
}

.feed .dot1 {
    left: 0px;
}
.feed .dot2 {
    left: 20px;
}
.feed .dot3 {
    left: 40px;
}
```

### 子代選擇器

-   只選擇子元素

```css
Parent > Target {
    property: value;
}
```

### 兄弟選擇器

-   可以選擇兄元素之後所有的弟元素

```css
Sibling ~ Target {
    property: value;
}
```

### 相鄰兄弟選擇器

-   只選擇相鄰的第一個弟元素

```css
AdjacentSibling + Target {
    property: value;
}
```
