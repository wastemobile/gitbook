# 使用 GIT 更新書籍

在 **gitbook.com** 建立一個書籍專案之後，你需要把內容推送上去，使用網頁版的編輯器，或是使用終端機指令更新皆可。

第二種方法其實就是使用 [GIT](http://git-scm.com) 提交你的內容異動：

### GIT Url

每一本書都對應著一個 Git HTTPS 網址，GitBook 的 git 主機還不接受 ssh 傳輸協定。

網址看起來像這樣：

```
https://git.gitbook.com/{{UserName}}/{{Book}}.git
```

### 授權認證

主機需要認證你的 GitBook 帳號，跳出提示時輸入你的 GitBook 帳戶名稱與密碼即可（你也可以使用專屬的 API token）。

### 儲存你的認證許可（credentials）

為了省去每次推送內容時都得輸入帳號密碼的麻煩，你可以把 GitBook 的認證許可寫到 `~/.netrc` 檔案裡。新建或是添加下面的內容到 `~/.netrc` 檔案：

```
machine git.gitbook.com
  login USERNAME-or-EMAIL
  password API-TOKEN-or-PASSWORD
```

建議使用 **API TOKEN**，因為安全性更高些；你可以從[網站後台](https://www.gitbook.com/settings#api)的「API」選項中找到專屬於你的相關資訊。


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
