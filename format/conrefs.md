# 內容參照（Content References）

內容參照（Content referencing - conref），是從其他檔案或書籍中，重複取用內容的一種便利機制。

### 嵌入本地檔案

使用 `include` 標籤就能非常方便的載入其他檔案的內容：

```
	{% include "./test.md" %}
```

### 從其他書籍嵌入內容

GitBook 也能理解你嵌入的 git 路徑：

```
	{% include "git+https://github.com/GitbookIO/documentation.git/README.md#0.0.1" %}
```

Git 網址的格式是這樣：

```
git+https://user@hostname/project/blah.git/file#commit-ish
```

Git 倉儲的結尾應該是 `.git`，接著則是要載入的檔案名稱。

最後以 `#` 附加的可以是任何標籤、sha 或是倉儲分支，有點像是使用 `git checkout` 命令指定要從哪裡取出資料。預設值是 `master`。

### 繼承

模板繼承，是讓你能重複使用模板的一種方式。撰寫模板時，你可以定義一些區塊（blocks），而這些區塊是使用子模板載入內容的。這樣的繼承鏈結並沒有層級數量的限制。

> 簡單的說，就是你可以「在模板中使用不限數量、層級的子模板」。舉例來說，你有一個小模板用來呈現特殊的「名詞解釋」或「引用來源」，在不同章節中你都可以叫用這個小模板，但呈現不同的名詞、網站資料或是維基百科詞條。當你修改了這個小模板，所有使用到它的章節，都會自動套用新的呈現。

區塊（`block`）定義了模板中的一個區段，賦予它一個特定的名稱。你在基礎模板中定義這些區塊，子模板則負責取得不同的內容，最後覆蓋、填充進這些區塊的位置。

```
	{% extends "./mypage.md" %}

	{% block pageContent %}
		# This is my page content
	{% endblock %}
```

在 `mypage.md` 檔案裏，你就可以指定區塊該如何被替代：

```
	{% block pageContent %}
	這裏擺放預設內容
	{% endblock %}

	# License

	{% import "./LICENSE" %}
```
