## 來源優先順序

1. 行內樣式
2. 外部與內部樣式表
3. 瀏覽器預設

## 同源規則優先順序

1. 行內樣式
2. ID 選擇器
3. 類別選擇器
4. 標籤選擇器
5. 通用選擇器

```css
.type1 #id3 {
    color: green;
}

div p #id3 {
    color: blue;
}
```

## 不講武德

-   直接指定為最優先，就是在屬性後面加上「!important」
-   盡量避免

## 不分軒輊

-   後者優先

## [Test](https://codepen.io/zero3william/pen/NWwpYgq)