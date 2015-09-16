# 整合 GitHub

GitBook 完整支援 [GitHub](https://github.com)，你可以把所有撰寫、編輯書籍所需的草稿與素材都擺放在 GitHub。

## 連結帳號 / 授權許可

首先你必須先讓 GitBook 獲得存取你的 GitHub 帳號的權限，才能夠同步資料。

從 GitBook 後台的 [account settings](https://www.gitbook.com/settings)，點擊**連接**你的 GitHub 帳號，取得以下權限：

- **Default permissions**: 登入認證程序
- **Access to webhook**: 替特定專案建立 webhook (參考 [webhooks](#webhooks)).
- **Access to public repositories**: 能夠存取你的開放倉儲。這樣你才能方便的使用線上編輯器修改你的書籍。免費的 GitHub 用戶都只有開放倉儲可用。
- **Access to private repositories**: 存取私密倉儲的權限。（GitHub 付費用戶）

## 從 GitHub 匯入書籍

在 GitBook 新建書籍時，從 `GitHub` 頁籤可以選擇要從哪個 GitHub 倉儲匯入內容。

一旦選定之後，書籍會根據你倉儲內的內容建立，也自動建立了一個 webhook。

## Webhooks

Webhooks 會在你的 GitHub 內容異動後，代為通知 GitBook。

如果你異動了 GitHub 倉儲，GitBook 卻沒有被同步更新，最常見的問題就是 webhook 出錯了。從倉儲設定頁面可以檢查 webhook 的執行紀錄與狀態。


## 設定書籍與 GitHub 倉儲的連接

當你已經設定好 GitHub 帳號與 GitBook 帳號的連接，讓書籍與倉儲連接與同步就很簡單。

**注意：** 當一本書被指定了與 GitHub 倉儲的連接後，優先權高於 GitBook 自己的倉儲。換句話說，此時打開線上編輯器、修改內容，被修改的是 GitHub 倉儲裡面的內容。

**同步是單向的**，只有異動 GitHub 倉儲內容會驅動製書程序。未設定連接 GitHub 的書籍都是使用 GitBook 自己的倉儲，假如你編輯了一些內容，還沒有轉製電子書，又在此時設定了與 GitHub 倉儲的連接，那麼這些異動**不會**被同步到 GitHub。

1. 從書籍後台設定頁面打開 GitHub 設定功能
2. 輸入 GitHub 倉儲 id （例如 `YourGitHubUserName/RepoName`）
3. 儲存設定
4. 點擊 **Add a deployment webhook** 按鍵

如果權限設定無誤，你現在就可以使用線上編輯器，直接修改 GitHub 倉儲中的資料了，當你提交異動到 GitHub，將會驅動在 GitBook 上的製書程序。

## 常見問題：

##### 書籍沒有被同步更新 / 看不到任何製書紀錄

如果你連接了書籍與 GitHub 倉儲，提交異動內容後 GitBook 卻沒有開始進行製書程序，首先要檢查的就是到 GitHub 倉儲頁面看看 webhook 有沒有被正確加入。萬一沒有，回到 GitBook 的設定頁面點擊加入按鈕，再試看看。

##### 書籍的名稱或擁有者變更了

如果你把書移交給另一個擁有者，webhook 就失效了，你必須重新加入一次。
