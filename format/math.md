# Math & TeX

感謝外掛系統，GitBook 支援數學公式與 TeX（學術界十分流行的一種排版語言）了。

兩個官方外掛分別用來處理數學公式：[mathjax](https://github.com/GitbookIO/plugin-mathjax)，以及 [katex](https://github.com/GitbookIO/plugin-katex)。

#### 啟用數學公式外掛

想啟用數學公式支援，就把 `mathjax` 外掛加入 `book.json` 檔案裡：

```js
{
    "plugins": ["mathjax"]
}
```

#### MathJax 與 KaTeX 的不同

這兩個外掛 `mathjax` 與 `katex` 對 TeX 數學公式的導入方式略有不同，分別根基於它們所使用的開源套件：[KaTeX](https://github.com/Khan/KaTeX) 與 [MathJax](https://www.mathjax.org)。

MathJax 支援完整的 TeX 語法，但輸出到電子書格式（PDF, ePub 與 Mobi）時不太完美。
KaTeX 能在各種格式中呈現得很好（包含網站與電子書），但不支援 [所有的語法](https://github.com/Khan/KaTeX/wiki/Function-Support-in-KaTeX)。


#### 在內容中書寫數學公式

```
這是呈現在行內的數學公式： $$a \ne 0$$
```

以單獨段落呈現的數學公式：

```
Here is a block of math:

$$
a \ne 0
$$
```