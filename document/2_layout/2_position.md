# 定位

覆蓋正常佈局流，產生有趣的效果

## 包含元素(containing block)

-   可理解為左上角(0,0)的位置

## position property

-   static (靜態定位,默認值,正常佈局流)
-   relative (相對定位)
    -   包含元素為父容器
    -   可使用 top, bottom, left, right 屬性
-   position (絕對定位)
    -   可使用 top, bottom, left, right 屬性
    -   脫離正常佈局流
    -   包含元素(containing block)(0,0) 為
        -   最近的”相對定位“祖先
        -   html
-   fixed (固定定位)
    -   可使用 top, bottom, left, right 屬性
    -   脫離正常佈局流
    -   包含元素 為 窗口(viewport)

## z-index property

-   z-index: number
-   當元素開始重疊，哪個元素出現在其他元素的上面？
    -   z-index 數字大的
    -   後定位的元素

---

## 滾動祖先 (scrolling ancestor)

-   可滾動的祖先層元素

## 高手才知道的 position: sticky (CSS3 新屬性)

-   沒有滾動祖先，就是 相對定位
-   有滾動祖先，就是 絕對定位
-   warning
    -   父元素不能 overflow:hidden 或者 overflow:auto 或 overflow:visible
    -   須指定 top、bottom、left、right 之一，否則處於相對定位
    -   父元素的高度不能低於 sticky 元素的高度
    -   sticky 元素僅在其父元素內生效
    -   IE 881

## [Demo](https://codepen.io/zero3william/pen/wvPjjre)