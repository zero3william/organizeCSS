# Multi Column Layout

## column-count

-   需要準確的 column 數時，可以使用

    ```css
    .container {
        column-count: 3;
    }
    ```

## column-width

-   將 column 保持在特定寬度
-   同時宣告 column-count 與 column-width 時，column-count 是最大 column 數。

    ```css
    .container {
        column-width: 200px;
    }
    ```

## column-rule

-   column 與 column 之間的垂直線
-   不佔用空間

    ```css
    .container {
        /* column-rule: 1px solid black; */
        column-rule-width: 1px;
        column-rule-style: solid;
        column-rule-color: black;
    }
    ```

## column-span

-   設置該元素 column-span: all，使其跨越 column

    ```css
    .container {
        column-span: all;
    }
    ```

## column-gap

-   column 與 column 之間的間隙

    ```css
    .container {
        column-span: 10px;
    }
    ```

## [演示](https://codepen.io/zero3william/pen/QWOMVjw)

## [瀑布流佈局練習](https://codepen.io/zero3william/pen/qBVmeWy)

## [瀑布流 multi-column answer](https://codepen.io/zero3william/pen/yLPXBPZ)
