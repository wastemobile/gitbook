# AsciiDoc

從 Gitbook `2.0.0` 以後，也接受 AsciiDoc 作為輸入格式。

詳細的語法說明請參照 [AsciiDoc Syntax Quick Reference](http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/)。

與使用 Markdown 的情況相同，GitBook 也使用一些特殊的檔案來處理書籍結構： `README.adoc`, `SUMMARY.adoc`, `LANGS.adoc` 以及 `GLOSSARY.adoc`。

### README.adoc

這檔案是書籍的介紹文字，一定要有這檔案才行。

### SUMMARY.adoc

這檔案是章節的清單，與 [使用 Markdown 的情況](./chapters.md) 相同，內容只是簡單的連結列表：連結的名稱會成為章節名稱，對應的則是實際內容檔案（含路徑）。

多層次目錄就是巢狀排列的清單而已。

```
= Summary

. link:chapter-1/README.adoc[Chapter 1]
.. link:chapter-1/ARTICLE1.adoc[Article 1]
.. link:chapter-1/ARTICLE2.adoc[Article 2]
... link:chapter-1/ARTICLE-1-2-1.adoc[Article 1.2.1]
. link:chapter-2/README.adoc[Chapter 2]
. link:chapter-3/README.adoc[Chapter 3]
. link:chapter-4/README.adoc[Chapter 4]
.. Unfinished article
. Unfinished Chapter
```

### LANGS.adoc

對 [多種翻譯版本](./languages.md) 並存的書籍來說，這檔案用來定義支援哪些語言版本與翻譯。

檔案內的語法與 `SUMMARY.adoc` 一樣：

```
= Languages

. link:en/[English]
. link:fr/[French]
```

### GLOSSARY.adoc

這檔案用來定義詞彙，參考 [詞彙表](./glossary.md) 的說明。

```
= Glossary

== Magic
Sufficiently advanced technology, beyond the understanding of the observer producing a sense of wonder.

== PHP
An atrocious language, invented for the sole purpose of inflicting pain and suffering amongst the programming wizards of this world.
```


