# 實際演練與習題

（由於 GitBook 很適合學習程式設計類的書籍，因此開發了獨特的外掛，當然任何類型的書籍也都可以使用，增加一點互動或許能讓你的書籍更吸引人、更有用。）

實際演練（Exercises）與習題（Quizzes）可以使用特殊的 `book.json` 檔案來啟用，參考下面的範例：

```js
{
    "plugins": [ "exercises", "quizzes" ]
}
```

#### 實地演練（Exercises）

一本書可以包含互動的實地演練，目前只支援 JavaScript。一個演練像是讓讀者能實際挑戰一段代碼的寫作，外掛提供了代碼編輯區塊，能夠設計問題與解答的檢查。

一個實地演練由四個簡單步驟組合而成：

* 演練 **訊息**/目標（使用 markdown 或純文字）
* **Initial** 展示給讀者的初始代碼，提供一個起點
* **Solution** 結果代碼，演練的正確解答
* **Validation** 驗證程式：用來檢查讀者輸入代碼是否正確

演練區塊需要以獨立的符號區隔（```---``` 或是 ```***```），應該要包含三段代碼元素（**base**, **solution** 與 **validation**）。特殊的第四種元素是 **context** 代碼（函數、函式庫的引入等等，這些都是提供讓程式能正確運作的情境要素，讀者看不到這些代碼）。

    ---

    Define a variable `x` equal to 10.

    ```js
    var x =
    ```

    ```js
    var x = 10;
    ```

    ```js
    assert(x == 10);
    ```

    ```js
    // This is context code available everywhere
    // The user will be able to call magicFunc in his code
    function magicFunc() {
        return 3;
    }
    ```

    ---


#### 習題

一本書也能包含互動的習題（問題與解答）。

其實習題與實地演練的設定與概念都差不多，只不過習題演練多了輸入與驗證程式碼的功能，比較像是「申論題」；習題則像是簡單的「單選題」或「複選題」，有時猜一下也行。

    ---

    這裏寫一整組習題的描述文字。

    這是第一道習題：
    - [x] This is the proposition 1 (the correct one)
    - [ ] This is the proposition 2

    > This is a help message when the answer to question 1 is wrong

    This is Question 2:
    - [ ] This is the proposition 1
    - [x] This is the proposition 2 (correct)
    - [x] This is the proposition 3 (correct)

    > This is a help message when the answer to question 2 is wrong

    ---

