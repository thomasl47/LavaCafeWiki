# Lava Cafe Stop
  * [Programming](programming/home)
  * [Travel](travel/home)
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
打開browser [http://localhost:4567/](http://localhost:4567/) 就會看到編輯頁了
