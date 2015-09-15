# 外掛 Plugins

外掛是擴充 GitBook 功能的最佳方式（針對電子書或書籍網站）。目前已經有不少好用的外掛，例如數學公式的呈現、使用 Google Analytic 服務追蹤造訪者等等。

### 哪裏找外掛？

直接連線到 [plugins.gitbook.com](http://plugins.gitbook.com)。

> 目前已經有一百多種外掛可用。

### 如何安裝外掛？

安裝外掛的方式，是編輯 `book.json` 檔案：

```
{
  "plugins": ["myPlugin", "anotherPlugin"]
}
```

也可以直接指定外掛的版本： `"myPlugin@0.3.1"` ，在使用舊版本 GitBook，必須指定舊版相容的外掛時很有用。

如果你是下載 GitBook 程式並在自己的電腦上轉製書籍時，修改完 `book.json` 檔案後，需要執行 `gitbook install` 終端機指令，就會自動連線下載並安裝外掛。


