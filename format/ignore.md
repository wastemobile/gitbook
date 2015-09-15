# 忽略檔案與目錄

GitBook 會讀取 `.gitignore`, `.bookignore` 以及 `.ignore` 這三個檔案，根據裡面的指示，忽略掉特定的檔案或是整個次目錄。（在文件中以一行一個檔案或目錄的方式撰寫即可。）

```
# 可以撰寫註解

# 忽略 test.md 檔案
test.md

# 忽略 "bin" 目錄下的所有檔案
bin/*
```
