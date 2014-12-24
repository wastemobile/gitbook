# 格式

編輯格式的設計，將焦點放在「簡潔易用」與「可讀性」。

GitBook 使用 Markdown 這種輕量級標記語法作為編輯格式的設計基礎。

根據我們的最簡定義：一本書就是至少包含了 README.md 與 SUMMARY.md 這兩個檔案的 Git 倉儲。

#### README.md

這個檔案是書籍的介紹文字，會自動被加入到完成後的目錄。

#### SUMMARY.md

SUMMARY.md 檔案定義了你的書籍結構，也就是指向實際檔案的一份目錄，列出所有章節（可以有多層次的章節架構）。

範例：

```
# Summary

這裏可以撰寫關於本書的詳細介紹文字。

* [section 1](section1/README.md)
    * [example 1](section1/example1.md)
    * [example 2](section1/example2.md)
* [section 2](section2/README.md)
    * [example 1](section2/example1.md)
```

沒有在 SUMMARY.md 文件裏指定的檔案，GitBook 在轉製書籍時都不會使用。

## 譯者補充說明

### 關於 Git 與 GitHub

這是一種目前程式開發者很習慣的「版本管理系統」，簡單的說就是會儲存你的內容修改與編輯歷程，讓你有機會比較甚至回復到之前修改過的某個時間點，但原則上你必須在修改到一定程度後明確的「儲存」並讓系統知道這是一個需要紀錄的過程版本。[GitHub](https://github.com) 則是目前全世界最大、被程式設計師廣泛使用的 Git 線上服務。

GitBook 支援兩種模式：使用 GitBook 自己的倉儲系統，或是導入你擺在 GitHub 上面的專案。對一般不熟悉 Git 系統的用戶來說，直接在 GitBook 上開啟一個書籍專案，持續使用它提供的編輯器書寫與編輯，就不用太在意這個在背後持續保護你的內容的底層機制，只要記得儲存就好。

### 關於目錄與檔案

GitBook 可以作為一種「持續出版」的工具，因為你可以在專案目錄下，擺放各種狀態的文件：研究資料、參考書摘，以及章節還在進行中的草稿，只要不將這些檔案對應寫進 SUMMARY.md 文件中，GitBook 就不會在轉製時包含進去。

你可以在寫完前言、第一章時，就先修改 SUMMARY.md 檔案讓它只包含這些完成的部分，製作出來的書籍就很像是「試讀本」。你也可以用上面的格式預先展示目錄（書籍的架構與未來會撰寫的章節計畫），但不要賦予實際的檔案連結（畢竟你還沒有寫完對嗎？）。


#### 支援多語言版本

GitBook 原本就支援以各種語言的內容出版書籍，而這裡指的是一種特殊的模式：在一本書的專案內，同時提供多種語言的版本，讓讀者自行選擇閱讀。

每一種語言版本必須以一個次目錄擺放，裡面的結構與正常的 GitBook 相同（擁有各自的 README.md、SUMMARY.md 以及實際的內容檔案），最外層再擺一個特殊的 `LANGS.md` 檔案，在其中以下面的格式寫明對應：

```
* [中文版](ch/)
* [English](en/)
* [French](fr/)
* [Español](es/)
```

你可以參考一個實際的範例 [Learn Git](http://gitbookio.gitbooks.io/progit/) ，點擊「READ」按鍵後多了一頁，再點選語言版本後就進入了不同的書籍內容。

#### Glossary

GitBook 提供了一種簡單的「詞彙表」、「名詞解釋」製作方法。

Allows you to specify terms and their respective definitions to be displayed in the glossary. Based on those terms, gitbook will automatically build an index and highlight those terms in pages.

測試文字：Meteor，精益出版。

The GLOSSARY.md format is very simple :

````
# term
Definition for this term

# Another term
With it's definition, this can contain bold text and all other kinds of inline markup ...
```

#### Ignoring files & folders

GitBook will read the `.gitignore`, `.bookignore` and `.ignore` files to get a list of files and folders to skip. (The format inside those files, follows the same convention as `.gitignore`)
