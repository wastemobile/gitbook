## GitBook 中文解說 - 2.4

`2015/09/17 更新`

> 增加了一章 [〈GitBook 終端機指令〉](book/gitbook-cli.md)。能夠使用終端機指令與 Node 的讀者，可以在本地製作任一種格式的電子書檔；在本機開啟網頁書籍，即時編輯與校對；建製整個靜態書籍網站，擺放到自己的網站空間，甚或是 GitHub Pages 服務。

`2015/09/16 更新`

> 增加了一章 [〈不懂 GIT 也能用 GitBook〉](book/nogitisok.md)。只要掌握兩個重點，就能善用 GitBook 的長處，希望能對作者或編輯有點幫助。（畢竟 GitBook 愈來愈強大，也有愈來愈難掌握的趨勢...）

`2015/09/15 更新`

> 原搶先預覽中，與開發相關的說明（例如外掛），已移往單獨的 [GitBook 開發者手冊](https://www.gitbook.com/book/wastemobile/gitbook-api-guide/details)，目前官方手冊仍在持續增加內容，儘量會同步測試與更新。

GitBook 是一個終端機指令工具，也是 Node.js 的代碼庫，使用 GitHub/Git 與 Markdown（或 AsciiDoc）就能製作漂亮的書籍。看看這個例子：[《Learn JavaScript》](https://www.gitbook.com/book/gitbookio/javascript/details)。

[GitBook](https://www.gitbook.com/) 同時也是一間書籍發佈平台與電子書店。一度停止開發的桌面版編輯器最近也回籠了，同時支援 Mac、Windows 與 Linux 三種平台，[下載試看看吧！](https://www.gitbook.com/editor)

### 開放格式

GitBook 的工具能製成多種格式：**PDF, ePub, mobi 與線上閱讀版本（網站）**。

它是開源的，你可以在[這裡](https://github.com/GitbookIO/gitbook)看到工具的原始碼，修過進階魔法學的魔法師可以取回自行調配。

你同樣可以在 [GitHub](https://github.com/GitbookIO/gitbook/issues) 上提交你的問題與意見，甚至協助解決問題或改善程序。

### GitBook.com

GitBook.com 是一個建置與擺放書籍的開放**平台**，當然你得遵循 GitBook 對草稿文件的一些規範。

> 好吧，這網站其實複雜得多。它有電子書店的展示、搜尋與購買機制，也能讓出版者自由上架販售，同時底層還是個兼具 Git 版本管理的中央倉儲，以及將草稿轉換為各種電子書與網站的引擎。

### 其他文件

開發者需要參考的 API 與 Plugins 文件已經獨立出來，英文版本在 [developer.gitbook.com](https://developer.gitbook.com/)。

針對企業版本的設定指南與文件則在 [help.enterprise.gitbook.com](http://help.enterprise.gitbook.com/)。

> [GitBook 企業版本](https://enterprise.gitbook.com)是將這整套文件管理與製書機制，提供給企業使用的方案，由於可獨立運作在企業的伺服器中，更能確保安全。20個人以下年費為美金$5,000，21至40人則要$10,000，依次遞增；大學院校、新創公司或非營利事業有特別的優惠。


## 內容概要

現在與未來的電子書，都是一種「微型網站」，結構與內容是 HTML，版面透過 CSS 樣式表設計，互動與進階都仰賴 JavaScript；即使在原生的閱讀軟體中讀書，替你組版的都是與瀏覽器相同（或極其接近）的組版引擎。未來的書籍製作工具，一個極端是全視覺化、模組化的「模擬富文本」生產工具，另一個極端則是寫代碼的編輯工具。

因為還沒有到未來，所以符合的工具還不存在。

GitBook 是一個已經朝正確方向前進了幾步的建構，關心電子書的人都應該嘗試看看，在書中還提到其他幾個你可以使用的服務與工具。

部分內容還會持續更新，畢竟這也是一種「精益出版」。

### GitBook 的基本特色有：

1. 以 Markdown 輕量級標記語法作為編輯「原稿」的基礎。
2. 拿程式設計師已經不能不學的 Git 作為版本管理架構。
3. 透過雲端快速轉製各種格式的流通電子書格式。
4. 提供在瀏覽器中閱讀的介面，增添了特殊的互動元件（JavaSript）。
5. 讀者能夠直接付費購買，支持創作與正版流通。
6. 提供 OPDS 流通，可以在行動裝置上使用支援的閱讀軟體。

這本小書包含 **GitBook** 的完整文件，涵蓋其服務平台與工具。原始的英文文件在 [GitHub](https://github.com/GitbookIO/documentation) ，也可以透過 GitBook 的網頁介面閱讀[原書](http://help.gitbook.io)。

> 你可以在這裡找到[中文內容](https://github.com/wastemobile/gitbook)的 GitHub 倉儲。

#### 需要進一步的協助？

對 GitBook 有任何疑問或需要尋求協助，可以在下面兩個 GitHub 專案上提交問題與建議，或直接以電子郵件聯繫： [contact@gitbook.com](mailto:contact@gitbook.com)。
