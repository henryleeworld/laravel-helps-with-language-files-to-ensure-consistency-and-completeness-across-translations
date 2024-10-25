# Laravel 11 幫助處理語系檔以確保翻譯的一致性和完整性

引入 bottelet 的 translation-checker 套件來擴增幫助處理語系檔以確保翻譯的一致性和完整性，協助尋找忘記新增至語系檔的翻譯、檢查和維護專案翻譯的工具。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 執行 __Artisan__ 指令的 __translations:check__ 來檢查、管理和更新翻譯。
```sh
$ php artisan translations:check {語系，例如：zh_TW}
```

----

## 畫面截圖
![](https://i.imgur.com/JKQ4shg.png)
> 確保翻譯的一致性和完整性
