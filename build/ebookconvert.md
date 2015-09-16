### 安裝電子書轉製程式

製作電子書（ePub, mobi 與 PDF）需要 ebook-convert。

#### Mac

下載 [Calibre app](http://calibre-ebook.com/download)，與一般軟體的安裝程序相同，把主程式拖到應用程式目錄。完成之後，你還需要替 `ebook-convert` 建立一個可全域執行的鏈結：

```
$ sudo ln -s ~/Applications/calibre.app/Contents/MacOS/ebook-convert /usr/bin
```

執行目錄 `/usr/bin` 視你的環境調整，只要確保它在你的 `$PATH` 設定裡就可以。