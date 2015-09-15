# 設定檔

對一本書的所有設定，都以 JSON 格式寫在 `book.json` 檔案中。

你可以把 `book.json` 檔案內容複製貼到 [jsonlint.com](http://jsonlint.com) 檢查 JSON 語法是否正確。

所有欄位都有多種選項，以及特定的預設值。


## 欄位

#### gitbook

```js
{ "gitbook": ">=2.0.0" }
```

這個選項用來偵測使用 GitBook 哪個版本來製作書籍，版本號的格式遵循 SEMVER](http://semver.org) 的規範。

#### title

```js
{ "title": "My Awesome Book" }
```

這用來定義你的書名，預設值是 **README** 檔案內的第一個標題。

在 **gitbook.com** 網站上，這個標題的值則是根據你輸入平台的資料。

#### description

```js
{ "description": "This is such a great book!" }
```

用來撰寫書籍的簡介，預設值是 **README** 檔案中的第一個段落內容。

同樣的在 **gitbook.com** 網站，書籍簡介是根據你後台輸入的內容。

#### isbn

```js
{ "isbn": "978-3-16-148410-0" }
```

如果書籍具備 ISBN，記得要輸入進去。 

#### language

```js
{ "language": "fr" }
```

定義書籍使用的主要語言文字，預設值是 `en` （英文）。

也會用來設定國際與本地化，例如網站介面使用的文字會連帶變換語系。

This option defines the language of your book, by default value is `en`.

This option is used for internationalization and localization, it changes the text from the website.

在 **gitbook.com** 網站上，這個值可以在設定介面中指定，否則就會根據內容自動偵測。

#### direction

```js
{ "direction": "rtl" }
```

這個選項用來覆蓋掉語言預設的閱讀走向，由左到右（ltr）或由右到左（rtl），建議依據語言特性設定正確，例如阿拉伯語系文字都是由右到左；而中文設定 `rtl` 則是直排專用，目前 GitBook 並不支援。

#### styles

這個選項可以設定對應的 CSS 樣式表。

例如：

```js
{
    "styles": {
        "website": "styles/website.css",
        "ebook": "styles/ebook.css",
        "pdf": "styles/pdf.css",
        "mobi": "styles/mobi.css",
        "epub": "styles/epub.css"
    }
}
```

#### plugins

```js
{ "plugins": ["mathjax"] }
```

設定這本書使用到的外掛。

#### pluginsConfig

```js
{
    "plugins": ["myplugin"],
    "pluginsConfig": {
        "myPlugin": {
            "message": "Hello World"
        }
    }
}
```

外掛有時需要額外的設定，就依照上面的格式撰寫。

#### structure

這選項用來覆蓋到 GitBook 預設使用的檔案與路徑。

例如你想用 `INTRO.md` 而不是 `README.md` 撰寫書籍介紹：

```js
{
    "structure": {
        "readme": "INTRO.md"
    }
}
```

可以改變的架構設定有： `readme`, `langs`, `summary` 與 `glossary`。

> 建議沒事不要變更這些設定比較好，程式有時不那麼聰明，正常運作最重要。

#### variables

```js
{
    "variables": {
        "myTest": "Hello World"
    }
}
```

這選項用來定義[模板]((./templating.md)中要使用到的變數與值。

