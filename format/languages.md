# 多語言版本

GitBook 原本就支援以各種語言的內容出版書籍，而這裡指的是一種特殊的模式：在一本書的專案內，同時提供多種語言的版本，讓讀者自行選擇閱讀。

每一種語言版本必須以一個次目錄擺放，裡面的結構與正常的 GitBook 相同（擁有各自的 README.md、SUMMARY.md 以及實際的內容檔案），最外層再擺一個特殊的 `LANGS.md` 檔案，在其中以下面的格式寫明對應：

```
* [中文版](ch/)
* [English](en/)
* [French](fr/)
* [Español](es/)
```

你可以參考一個實際的範例 [Learn Git](http://gitbookio.gitbooks.io/progit/) ，點擊「READ」按鍵後多了一頁，再點選語言版本後就進入了不同的書籍內容。
