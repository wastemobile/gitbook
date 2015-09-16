# 自定網域名稱

所有 **Gitbook.io** 的書籍，都可以透過這樣的網址 **http://{{author}}.gitbooks.io/{book}/** 連結到書籍介紹頁，書籍內文則在 **http://{{author}}.gitbooks.io/{book}/content/** 這個網址。

但你可以替自己的書設置**自訂網域名稱**（GitBook 提供的免費功能，當然你必須先在外部付費註冊到自己的網域名稱才行）。網域名稱可以套用到書籍單頁（介紹頁）以及內容頁。

設定網域的程序很簡單：

1. 在書籍管理頁輸入自定網域名稱

你必須先到你的網域購買商、DNS服務商的管理功能中進行設置：

1. 登入網域註冊商頁面後，找到 DNS 管理功能，可能會叫做  'Edit DNS', 'Host Records' 或 'Zone File Control'。

2. 增加一個 CNAME，對應到 ```www.gitbooks.io```。

3. 想設置轉址 (`yourdomain.com`) 到 `www.yourdomain.com`，你必須在 DNS 管理功能中找到 'Forwarding', 'URL Forwarding' 或 'URL Redirect' 的設置選項。

網址的轉換有時需要幾個小時，請耐心等候。
