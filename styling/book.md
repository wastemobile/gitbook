# 擴延網站與電子書樣式

在 `styles` 目錄下，你可以替不同目標對象（網站，或任一種電子書格式）添加要用的視覺樣式（CSS）。

| Type | File |
| ---- | ---- |
| `website` | `styles/website.css` |
| `pdf` | `styles/pdf.css` |
| `epub` | `styles/epub.css` |
| `mobi` | `styles/mobi.css` |
| `pdf`, `epub`, `mobi` | `styles/ebook.css` |


路徑也可以在 `book.json` 中指定，例如想把樣式檔擺在根目錄，就這樣改：

```json
{
    "styles": {
        "website": "website.css",
        "ebook": "ebook.css",
        "pdf": "pdf.css",
        "mobi": "mobi.css",
        "epub": "epub.css"
    }
}
```