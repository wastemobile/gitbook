# 建立並發布一個外掛

一個 GitBook 外掛，就是一個遵循 NPM 原則所發佈的 node 套件。

### 架構

#### package.json

套件中的 `package.json` 包含外掛的一般資訊（名稱、版本、描述等）：

```
{
    "name": "gitbook-plugin-mytest",
    "version": "0.0.1",
    "description": "This is my first GitBook plugin",
    "engines": {
        "gitbook": ">1.x.x"
    }
}
```

建議參考並遵循 [NPM 說明文件](https://docs.npmjs.com/files/package.json) 中關於 `package.json` 的準則。

注意： **package name（套件名稱）** 必須以 `gitbook-plugin-` 開頭，套件的 **package engines** 也必須包含 `gitbook` 在內。

#### index.js

一般來說，`index.js` 是你的外掛（套件）的程式起點。

### 發佈你的外掛

GitBook 外掛的發佈與安裝方式，都與 [NPM](https://www.npmjs.com) 一樣。

想要發佈新的外掛，你必須先建立 [npmjs.com](https://www.npmjs.com) 的帳號，然後使用一般 NPM 套件的發佈指令：

```
$ npm publish
```

