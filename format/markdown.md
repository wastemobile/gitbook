# Markdown

GitBook 預設使用 Markdown 標記語法。

本章內容僅快速呈現 Markdown 的基本語法與呈現，若需要更詳細的解說，英文資源可以看看發明人的說明： [John Gruber's original spec](http://daringfireball.net/projects/markdown/) 以及 GitHub 的擴充版 [Github-flavored Markdown info page](http://github.github.com/github-flavored-markdown/)。[Markdown.tw](http://markdown.tw) 有不錯的中文詳解；想看看俗稱 GFM - GitHub 風格的 Markdown 語法，也找得到[中文翻譯](https://github.com/cssmagic/blog/issues/13)。


## 標題

```markdown
# H1
## H2
### H3
#### H4
##### H5
###### H6

最常使用的 H1 與 H2 標題，還有更鮮明的另一種寫法：

Alt-H1
======

Alt-H2
------
```

# H1
## H2
### H3
#### H4
##### H5
###### H6

最常使用的 H1 與 H2 標題，還有更鮮明的另一種寫法：

Alt-H1
======

Alt-H2
------


## 強調語法

```markdown
強調，例如義大利斜體，可以使用 *asterisks* 或 _underscores_。

加重語氣的強調，例如粗體，可以用 **asterisks** 或 __underscores__。

你還可以混用這兩種 **asterisks and _underscores_**。

替文字加上刪除線，像這樣 ~~Scratch this.~~
```

## 清單

（下面的範例為了清楚展示縮排時需要的空格，使用了點號，實際撰寫時只需要相同數量的空格。）

```markdown
1. 第一則列表項目
2. 另一個項目
⋅⋅* 無序的次清單。
1. 數字本身是否排序並不重要，通通使用相同的數字也可以。
⋅⋅1. 排序的次清單。
4. 另一個項目

⋅⋅⋅你可以在一則項目中使用縮進的段落格式。注意上面的**空行**，還有本段前的**空格**（至少一個，我們使用了三個，讓呈現更清楚）。

⋅⋅⋅在一個段落中**強制換行**，在語句後方加入兩個**空格**。⋅⋅
⋅⋅⋅這個被強制設定的獨立行，依舊在同一個段落中。⋅⋅
⋅⋅⋅（有些人覺得使用空格強制換行太麻煩，例如 GFM 就根本不需要）。

* 可以使用星號建立無序清單
- 或是短橫線（負號）
+ 使用半形加號也可以
```

## 連結設定

有兩種方式可以建立文中的連結。

```markdown
[這是一個行內連結](https://www.google.com)

[這是一個帶有標題的行內連結](https://www.google.com "Google's Homepage")

[這是一個參考連結][Arbitrary case-insensitive reference text]

[這是一個對應到 Git 倉儲檔案的相對參考連結](../blob/master/LICENSE)

[參考標的物也可以使用數字][1]

直接使用文字對應也可以 [這段文字連到參考項目]

參考項目可以寫在文檔的最後，有點像書內的註解（註腳）。

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[這段文字連到參考項目]: http://www.reddit.com
```

## 註腳 Footnotes

The default footnote-style links that Markdown uses do not display on the page. Sometimes it is useful to include a non-hyperlink footnote that will be visible to the reader. GitBook supports a simple syntax for such footnotes.

```markdown
Text prior to footnote reference.[^2]
[^2] Comment to include in footnote.
```

> Markdown 的註腳實際上轉換成 HTML 時，是將所有註解文字移往「文件」最後成一個「清單列表」，文內則轉成對應的「跳轉連結」（俗稱的 **hash**），某些閱讀軟體採用跳轉模式，有些會以「跳出視窗」處理。新版 ePub 3 還有不同的標記法（noteref），GitBook 的處理方式還有待驗證。

## 圖片

```markdown
這是我們的 logo （將滑鼠移到圖片上會顯示圖片標題）：

行內格式：
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo 標題文字範例一")

參考連結格式：
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo 標題文字範例二"
```


## 程式代碼與語法高亮標示

程式代碼的呈現是 Markdown 規格的一部分，但語法高亮標示不是。已經有許多新的組版與轉換引擎支援了這個顯示慣例，例如 Github 與 *Markdown Here*，當然這項功能的實作還有很多歧異。*Markdown Here* 支援了非常多不同語言的特殊呈現（甚至包含了 diffs 與 HTTP headers）。想一覽完整的支援清單，以及如何正確標示語言名稱，可以參考 [highlight.js demo page](http://softwaremaniacs.org/media/soft/highlight/test.html)。

```markdown
行內 `code` 必須使用 `back-ticks` 將文字包起來（一般鍵盤左上方的第一個鍵）。
```

整段獨立呈現的代碼必須使用成對的三個 back-ticks <code>```</code> 包裹起來，或是使用四個空格縮排。建議使用第一種方法，因為那能讓代碼顯著標示。

<pre lang="no-highlight"><code>```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```

```python
s = "Python syntax highlighting"
print s
```

```
No language indicated, so no syntax highlighting.
But let's throw in a &lt;b&gt;tag&lt;/b&gt;.
```
</code></pre>


## 表格

最初的 Markdown 規格並沒有包含表格，但 GFM 與 *Markdown Here* 都有支援。這個撰寫語法也常出現在電子郵件中。

```markdown
冒號（Colons）是用來對齊的（擺左齊左、擺右齊右，都擺就置中）。

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

最外圍的豎線（|）不是絕對需要，在原始文檔中你可以不要太在意美觀，實際轉成網頁或電子書時會呈現得很好。你也可以在表格內使用行內格式。

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
```

## 引言

```markdown
> 引言（Blockquotes）常常出現在電子郵件中，表示摘錄來信原句並回覆。
> 這一行是引言的一部分。

Quote break.

> 這是一段非常長的引言區塊，只要在句首使用了正確的符號與空格，你可以持續不間斷的撰寫，整段文字都還是會被包含在引言區塊中。當然你依舊可以在引言區塊中 *使用* **Markdown** 的行內格式標記語法。
```

## 行內 HTML

因為 Markdown 本來就預設要轉換成 HTML 網頁格式，所以你當然可以直接寫入正確的 HTML 代碼，看起來都蠻正常的。（是的，電子書就是一種經過打包的 HTML 網頁組合，很像一個獨立的微型網站。）

```markdown
<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>
```


## 水平分隔線

```
三個或三個以上的符號，必須在獨立的一行，前後不能有其他文字。

---

短橫線（Hyphens）

***

半形星號（Asterisks）

___

下底線（Underscores）
```


## 空行分隔段落

習慣或熟悉 Markdown 如何進行分段是很重要的，基本上**空行**代表前後的文字都會是段落（在 HTML 中以 `<p>` 與 `</p>` 包裹起來）。如果你使用新一代的桌面編輯軟體，有些讓你可以微調空行的呈現，讓編輯區看起來不那麼鬆散；甚至還有軟體直接取消分行的設定，按下 **return** 就代表分段了，例如 [Ulysses]
(http://www.ulyssesapp.com)。

總之最好的方法是有一點實驗精神，打開你的編輯環境（不管是桌面軟體或 GitBook Web Editor），啟用即時檢視（預覽結果），試著輸入幾次、看看有什麼結果，很快就熟悉了。

試著嘗試看看下面的輸入與結果：

```markdown
Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This line is also a separate paragraph, but...
This line is only separated by a single newline, so it's a separate line in the *same paragraph*.
```

（注意： *Markdown Here* 套用了 GFM 的分行模式，因此強制斷行並不需要在字句後方加入兩個空格。）


## Youtube 影片

雖然你無法直接置入 Youtube 影片，但可以採用圖片連結的模式：

```markdown
<a href="http://www.youtube.com/watch?feature=player_embedded&v=YOUTUBE_VIDEO_ID_HERE
" target="_blank"><img src="http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg"
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>
```

你也可以直接在 Markdown 這樣寫，但會失去尺寸與邊線的設定：

```markdown
[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](http://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)
```
