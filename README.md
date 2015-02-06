## GitBook 2.0！

（製書流程始終出現 `ENOSPC, no space left on device` 的怪異錯誤，除蟲中...）

剛剛進入 `2.0.0-alpha` 階段的 GitBook，帶來了讓人興奮的新功能！

#### 模板引擎！

![Template Engine](https://gitbookio.github.io/blog/assets/2015-02-05-process.png)

電子書的擴充（不一定是互動，可能只是特殊呈現）能怎麼做？截至目前為止，只有 iBooks Author 有一些小控件（Widgets）可用，而它們其實都是以精美外觀與介面包裝起來的 JavaScript。

GitBook 2.0 居然向前跨了一大步，直接把 JavaScript 常見的模板、視圖小幫手還有控制器（JavaScript 函數）通通擺了進來，是有一點小誇張，但很讓人驚艷啊！

#### 支援更多的標記語法

增加了 AsciiDoc 和 reStructuredText 解析器。

#### 內容參照（不管是書籍內部或外部）

增加了直接嵌入內容，甚至是外部 Git 倉儲中的文件。

#### 外掛，以及擴充模板語法

GitBook 外掛就是百分百的 Node 套件，熟悉 JavaScript 與 Node 的程式設計師可以大展身手了。

一般的寫作者或是編輯，真正會用的可能是經外掛擴充的**內容區塊**（blocks）。它其實就是一種「視圖小幫手」，作者只需要使用特定語法標籤，送進參數，背後的程序就會做完該做的事，你擺放標籤的位置，會被返回、處理過的 HTML 內容替換掉。

#### 圖片處理能力大幅提升

最重要的，就是支援自動取回遠端圖片的打包功能（之前我只知道 Pandoc 可以做到）。SVG 圖片（包含 inline SVGs）都會被自動轉成 PNGs。

#### 數學公式呈現

原先 [MathJax 外掛](https://github.com/GitbookIO/plugin-mathjax) 只對線上瀏覽的書籍有效，現在也被提升到打包電子書之中了。

> 部分 GitBook 2.x 的功能與說明還不太完整，持續會有更新。

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

GitBook 是一個使用 Git 分散式版本管理與 Markdown 輕量級標記語法製作電子書的服務與工具，你可以一次產生多種不同流通格式，包含了 **PDF**, **ePub**, **mobi**（Amazon 專屬格式）或是一個 **線上閱讀網站**。

GitBook 的工具是開源且完全免費的，完整的原始碼可以在 [GitHub](https://github.com/GitbookIO/gitbook) 上找到。

你可以在這裡找到[中文內容](https://github.com/wastemobile/gitbook)的 GitHub 倉儲。

#### 需要進一步的協助？

對 GitBook 有任何疑問或需要尋求協助，可以在下面兩個 GitHub 專案上提交問題與建議，或直接以電子郵件聯繫： [contact@gitbook.com](mailto:contact@gitbook.com)。

* [GitBook Toolchain](https://github.com/GitbookIO/gitbook/issues?state=open)
* [Platform and Marketplaces](https://github.com/GitbookIO/gitbook.io/issues?state=open)
