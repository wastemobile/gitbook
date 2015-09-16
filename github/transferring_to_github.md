# 移轉內容到 GitHub

一開始你在 GitBook 上建立並編輯過書籍，想改放到 GitHub 上是很容易的。

#### 使用 GitHub 匯入工具

1. 使用 GitHub 提供的 **Import Tool** ：  [import.github.com/new](https://import.github.com/new)
2. 輸入你的 GitBook git 網址，例如： `https://git.gitbook.com/MyName/MyBook.git` （在書籍設定頁可以找到這個網址）。
3. 輸入 GitHub 倉儲要使用的名稱。
4. 跳出提示時，輸入你的 GitBook 認證許可（建議使用 API token，而不要用密碼）。
5. 完成！

當內容移轉到 GitHub 之後，就可以接著設定與 GitBook 的整合，請參照 [整合 GitHub](./README.md) 一章的內容。


#### 使用終端機指令

你必須先到 GitHub 建立一個新的倉儲。

**注意：** 你原先在 GitBook 上的歷史異動紀錄都會重設。

```
# 複製你的 GitBook 倉儲（需要輸入帳號密碼）
$ git clone https://git.gitbook.com/MyName/MyBook.git ./mybook

# 切換到目錄
cd ./mybook

# 推送到 GitHub 的倉儲
$ git push https://github.com/username/repo.git master --force
```