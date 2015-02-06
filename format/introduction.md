# Readme 檔案與書籍介紹

書籍的第一頁內容是從 `README.md` 這個檔案生成的，即使你沒有將 `README.md` 擺進製書指引檔（`SUMMARY.md`），它還是會被自動加入。

### 使用其他檔案

使用 `README.md` 的慣例，是從 GitHub 網站對專案的基準要求而來，大多數程式開發專案倉儲都會擺一個 README，記載專案最簡要的介紹與說明。當然，對大多數作者或編輯而言，可能不太習慣。

從 GitBook `>2.0.0` 之後，你可以在 `book.json` 檔案中指定要用哪一個檔案來扮演 README 的角色：

```
{
	"structure": {
		"readme": "myIntro.md"
	}
}
```

