# 模板

這裏說明了 GitBook 可以使用的模板功能，GitBook 使用的是 [Nunjucks](https://mozilla.github.io/nunjucks/) 與 [Jinga2](http://jinja.pocoo.org/) 的語法（Jinga2 是 Python 程式語言的一種模板引擎，Nunjucks 則是將其功能實現在 JavaScript 語言環境）。

### 跳脫 Escaping

如果想要呈現模板的標籤，可以使用 **raw** 包裹起來，裡面的內容都會原樣輸出成純文字。

```
{% raw %}
  this will {{ not be processed }}
{% endraw %}
```

### 變數 Variables

在一本書的情境範圍內，**變數**會尋找對應的**值**呈現出來。

變數是在 `book.json` 這個檔案中定義的：

```
{
	"variables": {
		"myVariable": "Hello World"
	}
}
```

#### 顯示變數

```
	{{ book.myVariable }}
```

上面這個語法標記，會顯示書籍的變數值（也就是 `Hello World`）。變數可以使用點（`.`）語法尋找下一層的屬性。你也可以使用方括號語法。

```
	{{ book.foo.bar }}
	{{ book["bar"] }}
```

如果找不到對應的變數定義，就什麼都不會呈現。假設你沒有定義 `foo` 變數，那麼後面這些標記都不會呈現： `{{ foo }}`, `{{ foo.bar }}`, `{{ foo.bar.baz }}`。

#### 情境變數

有一些變數可以從**目前的這個檔案**，或是 GitBook 中取得特定的值：

| 名稱 | 描述 |
| -- | -- |
| `file.path` | 目前檔案的相對路徑 |
| `file.mtime` | 目前檔案最後一次修改的時間 |

### 標籤

標籤（Tags），是在模板中執行某些操作的特殊區塊。

#### If

**If** 判斷某些條件，讓你能選擇性的呈現內容。這是程式語言中標準的邏輯判斷。

```
	{% if variable %}
		變數為真
	{% endif %}
```

如果 `variable` 有被定義且被判定為**真**（true），「變數為真」這幾個字就會呈現出來，否則就什麼都不呈現。

你還可以使用 `elif` 與 `else` 指定不同的條件判斷：

```
	{% if hungry %}
		我很餓
	{% elif tired %}
		我很累
	{% else %}
		我很好！
	{% endif %}
```

#### for

**for** 會從陣列（arrays）與字典中迭代取值。（ps.這裡的字典是指在 JSON 檔案中以名稱：值所定義的一些資料。）

假設我們在 `book.json` 中定義了多個作者：

```
	{
		"variables": {
			"authors": [
				{ "name": "Samy" },
				{ "name": "Aaron" }
			]
		}
	}
```

```
# Authors

	{% for author in authors %}
		- {{ author.name }}
	{% endfor %}
```

上面的範例，從作者 `author` 陣列中將每一個名稱 `name` 屬性都以清單呈現出來。

### 嵌入（include）

嵌入功能，會在[內容參照（Content References）](./conrefs.html)中詳細解說。