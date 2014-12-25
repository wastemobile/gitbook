# 使用 GIT 更新書籍

在 **gitbook.com** 建立一個書籍專案之後，最重要的就是持續更新內容了，使用網頁版的編輯器，或是使用終端機指令更新皆可。

第二種方法其實就是使用 [GIT](http://git-scm.com) 提交你的內容異動：

### GIT Url

每一本書都對應著一個 Git HTTPS 網址，GitBook 的 git 主機還不接受 ssh 傳輸協定。

網址看起來像這樣：

```
https://git.gitbook.com/{{UserName}}/{{Book}}.git
```

### 授權驗證

主機需要驗證你的 GitBook 帳號，跳出提示時輸入你的 GitBook 帳戶名稱與密碼即可（你也可以使用專屬的 API token）。

### 使用終端機指令建立新的書籍專案

```
touch README.md SUMMARY.md
git init
git add README.md SUMMARY.md
git commit -m "first commit"
git remote add gitbook https://git.gitbook.com/{{UserName}}/{{Book}}.git
git push -u gitbook master
```

### 推送到現有的書籍專案

```
git remote add gitbook https://git.gitbook.com/{{UserName}}/{{Book}}.git
git push -u gitbook master
```
## 使用 GitHub

GitBook 已經支援你將書籍專案（Git 倉儲）擺在 GitHub 服務，對已經很熟悉 GitHub 的程式設計師來說可能更加方便。

請先到自己的設定頁面連接你的 GitHub 帳號，這樣就可以到書籍管理頁去設定對應的倉儲了。

