# 書籍首頁的佈景主題

佈景主題（Themes）是指你在 gitbook.com 上的書籍首頁，並不是指書籍內文的排版樣式。你可以選擇任一種預設主題，或是自訂 HTML 模板。

### 預設主題

GitBook 的預設主題以開源方式提供，你可以從 [GitHub](https://github.com/GitbookIO/themes) 取得檔案。

### 格式

GitBook 使用 [Nunjucks](https://mozilla.github.io/nunjucks/) 與 [Jinga2](http://jinja.pocoo.org/) 的語法。

#### Variables for book homepage

| Variable | Type | Description |
| -------- | ---- | ----------- |
| `book` | `<book>` | Book to display |

#### Book Representation

| Variable | Type | Description |
| -------- | ---- | ----------- |
| `id` | `string` | Complete id of the book (ex: `Username/Test`) |
| `name` | `string` | Name of the book |
| `title` | `string` | Title of the book |
| `description` | `string` | Description of the book |
| `public` | `boolean` | False if the book is private |
| `price` | `number` | Price of the book (0 equals free) |
| `githubId` | `string` | ID of the book on GitHub (ex: `Username/Test`) |
| `categories` | `array[string]` | List of tags associated with this book |
| `author` | `<user>` |User that created the book |
| `collaborators` | `array[<user>]` | Array of collaborators of the book (excluding the author) |
| `cover.small` | `string` | Url of the cover (size small) |
| `cover.large` | `string` | Url of the cover (size large) |
| `urls.access` | `string` | Url to access the book homepage |
| `urls.homepage` | `string` | Url of the homepage (using custom domain) |
| `urls.read` | `string` | Url to read the book |
| `urls.reviews` | `string` | Url to the reviews page |
| `urls.subscribe` | `string` | Url to submit email subscriptions |
| `urls.download.epub` | `string` | Url to download ebook (as EPUB) |
| `urls.download.mobi` | `string` | Url to download ebook (as Mobi) |
| `urls.download.pdf` | `string` | Url to download ebook (as PDF) |

#### User Representation

| Variable | Type | Description |
| -------- | ---- | ----------- |
| `username` | `string` | Username of the user |
| `name` | `string` | Name of the user |
| `urls.profile` | `string` | Url to access the profile homepage |
| `urls.avatar` | `string` | Url of avatar |
| `accounts.twitter` | `string` | Username on Twitter (if linked) |
| `accounts.github` | `string` | Username on GitHub (if linked) |