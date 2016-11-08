# Lava Cafe Stop
  * [Programming](programming/Home.md)
  * [Travel](travel/Home.md)

## Getting started

### OSX (10.12)
```bash
$ brew install icu4c
$ export GEM_HOME=~/.gem
$ export GEM_PATH=~/.gem
$ gem install charlock_holmes -- --with-icu-dir=/usr/local/opt/icu4c
$ gem install gollum
# 裝超過 10分鐘還是卡住？
# Ctrl + c 停掉再試一次吧，一次裝失敗，你有裝兩次嗎？
Successfully installed gollum-4.0.1
$ cd LavaCafeWiki
$ /Users/<user_name>/.gem/gems/gollum-4.0.1/bin/gollum
```
打開browser [http://localhost:4567/](http://localhost:4567/) 就會看到編輯頁了

### 待解問題
  1. 為什麼 local 的線上編輯器 編輯完都直接 commit 到 master branch？  
     有 commit 到 其它branch的方法嗎？
  2. 不知有沒有自動產生目錄，目前感覺都是自己編輯
  3. 內部目錄時，local編輯器使用(例: ```[Travel](travel/Home)```) 可以變連結直接點擊  
     但github上要變連結，還要加上後面的副檔名(例： ```[Travel](travel/Home.md)```)  
     兩邊不互通不方便呀......

### 參考連結
  * [wiki 語法編 (基本上同markdown)](https://github.com/gollum/gollum/wiki)
