# 虛擬類別選擇器

-   pseudo-class 是以 : 為開頭，後面接著 pseudo-class 的名稱
-   有些會在後面加上括號 ()，並在括號之間加上值。例如：:nth-child(2)。

## 語法

```css
selector:pseudo-class {
    property: value;
}
```

## Link

UA (User agent，對 HTML 來說就是瀏覽器) 以不同的方式來顯示連結是否已訪問：

-   :link (未訪問過的連結)
-   :visited (已訪問過的連結)
-   UA 可以將已訪問的連結從 :visited 變回 :link 的狀態
-   網頁過期時間 或 使用者清空歷史記錄

## User-action

用於 response 使用者的操作

-   :hover (當 cursor hover 在元素上時)
-   :active (user mousedown 到 mouseup 之間的時間)
-   :focus (有焦點時，例如：按 Tab 鍵所選到的元素)

### 魔鬼的細節 - “愛恨原則”(LoVe/HAte)

-   LVHA
-   a:link、a:visited、 a:hover、a:active

[Demo](https://codepen.io/zero3william/pen/dyZZRwN)

## Target

帶有 anchor identifier (fragment identifier) 的 URL 會 link 到文件中的某些元素，該元素被稱為 target 元素

```html
<h1><a href="#hello">Hello</a></h1>
<div id="hello">
    <h2>Target</h2>
</div>
```

```css
#hello:target {
    color: red;
}
```
[:target demo](https://codepen.io/zero3william/pen/dyZvJmo)

## States

-   :enabled：處於啟用狀態的 UI 元素
-   :disabled：處於禁用狀態的 UI 元素
-   :checked：選取 radio 或勾選 checkbox 元素時會應用
-   [demo](https://codepen.io/zero3william/pen/mdqperP)

## Child-indexed

-   nth 開頭地()裡，可以使用以下幾種數值
    1. an+b
    2. odd = 2n+1
    3. even = 2n
-   :nth-child(an+b)
-   :nth-last-child(an+b)：
-   :first-child()：
    -   等同於 :nth-child(1)
-   :last-child()：
    -   等同於 :nth-last-child(1)
-   :only-child()：
    -   選擇沒有 sibling 的元素
    -   等同於 :first-child:last-child 或 :nth-child(1):nth-last-child(1)

## Type Child-indexed

-   tag:nth-of-type(an+b) => 第 an+b 個 tag
-   tag:nth-last-of-type(an+b) => 倒數第 an+b 個 tag
-   tag:first-of-type() => 第一個 tag
    -   等同於 :nth-of-type(1)
-   tag:last-of-type() => 最後一個 tag
    -   等同於 :nth-last-of-type(1)
-   tag:only-of-type() => 只有這個 tag
    -   等同於 :first-of-type:last-of-type 或 :nth-of-type(1):nth-last-of-type(1)

## Negation pseudo-class

-   :not(X) 是一個函數符號，可將一個 simple selector (不包括 :not(X) 本身) 作為參數。
-   :not(X) 代表不選擇 match 到 X simple selector 的元素。
-   simple selector：

    1. type selector：例如 div
    2. universal selector：例如 \*
    3. attribute selector：例如 div[foo]
    4. class selector：例如 .myclass
    5. ID selector：例如 #myid
    6. pseudo-class：例如 a:hover

    ```css
    button: not([disable]);

    *:not(#william);
    ```
