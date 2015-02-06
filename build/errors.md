# 常見錯誤

這裏有一些常見的錯誤，以及如何修正的建議。

---------

```
Error loading plugins: plugin1, ...
```

出現這錯誤的原因是 GitBook 找不到指定的外掛（或是外掛出錯）。

第三方的外掛需要使用 `gitbook install` 指令安裝後才能使用。

---------

```
Need to install ebook-convert from Calibre
```

這是轉製 PDF 常見的錯誤： [Convert of PDF - Need to install ebook-convert from Calibre #333 on GitHub](https://github.com/GitbookIO/gitbook/issues/333).

如果你希望在桌面（本地電腦）上完成書籍轉製，你就需要安裝 [Calibre](http://calibre-ebook.com) 與它提供的終端機工具。

已經安裝好 Mac 版本的 Calibre 之後，循著上面的選單依序點擊： **calibre - Preferences - Miscellaneous - Install command line tools**，就可以安裝好終端機指令工具。

上面程序完成之後，本地的轉製工作應該就會正常。

ps. 使用網頁編輯器，或是用 Git 提交更新，轉製程序是在 GitBook 主機上運作，並不需要安裝 Calibre，這應該是大多數人的使用情境。

***
