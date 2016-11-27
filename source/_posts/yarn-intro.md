---
title: 取代 npm 的新利器 Yarn
date: 2016-10-12
tags:
- Javascript
- NPM
- Yarn
categories:
- 程式設計
- Javascript
---

日前，Facebook 發布了全新的 JS 套件管理工具 [Yarn](https://yarnpkg.com)，如果你常發生以下幾個問題，我想 Yarn 會是你的解決方案

1. 「同事電腦 npm install OK，我卻 npm install 掛掉」，通常就是因為套件內部相依關係與你之前的檔案衝突，所以只好常常得先 sudo rm -rf node_modules/ 再重新安裝。

1. 沒網路，npm install 直接掛給你看。

1. 不同專案或不同資料夾下，都要更新某個套件。

1. npm install 非常久，久到可以泡杯咖啡聊個天，回來都還沒好。

<!-- more -->

## Yarn 提供一個更快更穩定的套件管理方案

1. 透過 yarn.lock ，鎖住套件版本，因此可以確保安裝之套件在每台機器上都能保持一致。

1. 安裝過的套件，都會加入到 global cache 中，下次有砍掉要重裝，或是不同資料夾要裝，都可以在無網路情況底下安裝。

1. 非常快，平行化處理每個 operation，全新的 resolving 演算法。

## 如何使用
```
    // 以前裝過 npm 再安裝 yarn
    npm install -g yarn

    // 直接安裝 (mac為例，其餘官網有介紹)
    curl -o- -L https://yarnpkg.com/install.sh | bash

    // 一般安裝 (等同 npm install)
    yarn

    // 安裝特定套件 (等同 npm install --save)
    yarn add react         
    yarn add react@15.3.2

    // 更新特定套件 (等同 npm upgrade)
    yarn upgrade react

    // 移除特定套件 (等同 npm uninstall)
    yarn remove react

    // 新增 package.json
    yarn init

    // 新增全域套件
    yarn global add

    // 跑 script
    yarn run

    // 其他常用選項
    --offline   (離線模式，只拉 cache)
    --flat      (將套件扁平化，一個資料夾只會有一個套件)
    --dev       (加入到 devDependencies)
    --peer      (加入到 peerDependencies)
    --optional  (加入到 optionalDependencies)
```
作者實測結果，非常快且沒有遷移問題，可直接捨棄 npm。

雖然說原本的 npm cache-min 設定時間 999999，以及 npm shrinkwrap 鎖版本，都可以達到 Yarn 所說的一些優化，不過 Yarn 本身在平行化處理部分有特別加強，也重寫了解析演算法，是一個完整的套件解決方案。

附註: push 到 repo 時請記得要上 yarn.lock 檔案，才會確保其他機器都能安裝一樣的套件代碼。

Yarn  
[https://yarnpkg.com/](https://yarnpkg.com/)
