# GitBook 終端機指令

> 這章主要針對 `gitbook-cli` 在本地端的使用，一般讀者可以跳過。

不管使用雲端或本地的編輯器，或使用自己喜歡的文字編輯器（例如 Sublime Text）、再推送到遠端倉儲，都是使用 gitbook.com 的雲端「製書程序」。這有一個小問題：當你還在「草稿分支」的時候，就看不到最終成果了，哪一種格式都一樣。如果你想要在本地、在任何分支，都輕鬆的看到最終的網頁書籍呈現，或是製作 ePub, Mobi 與 PDF 預先測試，就得使用 GitBook 提供的終端機指令工具才行。

首先你必須已經安裝好 `Node`、`NPM` 以及 `Calibre`，在 Mac 上測試過的版本為：

- Node v0.10.40 （使用 NVM 安裝）
- NPM 2.14.3
- Calibre 2.38.0

> 製書使用 Calibre 內部的一支 `ebook-convert` 程式，請根據[安裝電子書轉製程式](../build/ebookconvert.md)這章的方式建立鏈結，如果你的 Calibre 不是安裝在個人家目錄下的 `Applications`，要改對應到 `/Applications/calibre.app/Contents/MacOS/ebook-convert` 這個位置。最後使用 `ebook-convert --version` 確認一下，必須跳出正確的版本號，GitBook 終端機指令才能順利執行。

### 安裝

```
$ npm install -g gitbook-cli
```

將終端機指令工具安裝到 npm 的全域位置，目前 GitBook CLI 只支援 `2.0.0` 以上的 GitBook 版本。

- `gitbook versions` 顯示本地目前可用的 GitBook 版本。
- `gitbook versions:available` 顯示有哪些可以安裝的版本。
- `gitbook versions:install latest` 安裝最新版。
- `gitbook versions:install 2.3.3` 安裝特定版本。
- `gitbook versions:uninstall 2.3.3` 移除特定版本。
- `gitbook --version` 顯示 GitBook CLI 的版本號。

本地系統上已經有了最新的 GitBook，Calibre 轉製程式也備妥，接下來就可以製書了。

### 開始一本新書

1. 首先建立一個空目錄，例如 `mybook`，接著切換（`cd mybook`）到該目錄下。
2. 在空目錄中輸入 `gitbook init`，此時目錄下會新增兩個檔案： `README.md` 與 `SUMMARY.md`，這些是除了實際內容檔案之外，GitBook 製書的兩個必要檔案。
3. 你可以開始新增內容檔案，例如 `forword.md`、`ch1.md` 等等，打開你喜歡的純文字編輯器，開始寫書。
4. 添加一些內容之後，記得把要構成實際內容的檔案，加入到 `SUMMARY.md` 檔案中。
5. 此時可以輸入 `gitbook serve`，依照指示在瀏覽器中輸入 `http://localhost:4000`，就會看到與 GitBook 網站一模一樣的網頁版電子書。修改一些文字、儲存，你會看到網頁自動重載、更新了。

現在你已經獲得一個可在本地端離線編輯，還能立即呈現最終樣貌（網頁版閱讀）的編寫環境

### 製作網頁版本

在專案目錄輸入 `gitbook install`，會自動安裝必要與專案指定的外掛。

由於這是一個完全乾淨的空白專案，也就是你還沒有學到編輯 `book.json` 這個指定外掛的控制檔，GitBook 只會預先安裝一個 **highlight** 外掛，用來呈現書中插入程式代碼區段。（使用 `gitbook serve` 還會自動啟用另一個 **livereload** 外掛，用於自動重載更新後的頁面。）

整個書籍靜態網站會擺放在 `_book` 目錄下，若是不需要即時檢視修正，也可以使用 `gitbook build` 建立。可以把整個目錄上傳到自己的網站空間，就連 GitHub Pages 空間都可以用。

### 製作電子書檔

從專案根目錄執行：

- `gitbook epub` 製作 ePub 電子書
- `gitbook mobi` 製作 Kindle 電子書
- `gitbook pdf` 製作 PDF 電子書

最簡指令就這樣，預設都是 `book` 加上副檔名，在專案的根目錄裡。

### 完整指令

你也可以從專案外部執行，完整的指令是：

```
gitbook epub [book] [output]
```

例如 `gitbook mobi ~/books/mynovel ~/Desktop/novel.mobi`。製作電子書指定 output 時需包含完整的路徑與檔案名稱。

想要將靜態網站建置到特定目錄，可以這樣輸入：

```
gitbook build --output=/site/mybook
```

輸入 `gitbook help` 可以看到說明訊息與指示。

### 結論

GitBook 真可說是未來出版的一個雛形建構，而且還在持續進化之中。

一般人可以下載桌面編輯器，或使用雲端進行編輯，只要注意草稿分支的使用技巧，完全不懂技術也能製作各種電子書。不怕終端機指令、略懂 Node 與 NPM 操作的人，搭配 `gitbook-cli` 與 Calibre 則可以完整使用 GitBook 的所有功能，離線自行製書或使用雲端服務，想怎麼用都行。

下一步的進階，就是「書籍呈現格式的調整」，以及「使用模板、外掛」等實驗性功能吧。



