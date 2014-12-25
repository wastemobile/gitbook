# 編輯歷史紀錄

GitBook 紀錄了各種系統存取、閱讀與編輯的紀錄，可以讓你檢查內部編輯協作時的安全性，或是處理其他的安全性議題。

### 被記錄的行為

你可以搜尋下面各種操作行為的紀錄：

| Name | Description |
| ---- | ----------- |
| `user.login` | Login of an user |
| `user.failed_login` | An user/visitor faield to logged in |
| `user.signup` | Signup of an user |
| `user.remove` | User removed his account |
| `user.email.change` | User changed his email |
| `user.token.change` | User reset his api token |
| `user.password.change` | User changed his password |
| `user.forgot_password` | User reset his password |
| `user.verification.send` | User requested a verification email |
| `user.verification.done` | User verified his email |
| `user.forgot_password` | User reset his password |
| `staff.login.fake` | A site admin signed into an user account |
| `payment.card.change` | Connect a credit card |
| `payment.card.remove` | Remove a credit card |
| `payment.plan.change` | Changed his plan |
| `payment.transfer` | Transfer money to an user's bank account |
| `payment.recipient.change` | Connect a bank/paypal account |
| `payment.recipient.remove` | Remove a bank/paypal account |
| `book.create` | Creation of a book by an user |
| `book.remove` | Remove a book |
| `book.transfer` | Transfer a book |
| `book.publish` | Publish a new version of the book |
