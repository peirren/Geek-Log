---
layout: post
title: "Learning Jekyll, Part1"
date:   2019-01-02 00:55:12 +0800
categories: review
---

### 安裝前準備確認
- ruby -v (至少高於2.4)
- gem -v (至少高於2.6.13)
- gem install jekyll bundler (啟用Gem安裝Jekyll)
- jekyll -v (我的是 4.0)

## 終端機需要指令
- cd/ folder
- jekyll new document name (創建jekyll資料夾)
- bundle exec jekyll serve (啟動jekyll)

```
Randys-MacBook-Pro:~ Randy$ jekyll new jekyll_folder
Running bundle install in /Users/Randy/jekyll_folder…  
```
~畫面預覽~

[image:AB0A1B73-4288-4748-9161-8B0045E870D4-286-0000061D86AE4D70/螢幕快照 2020-01-04 上午12.57.20.png]



重要文件有：
- _posts 存放文章的地方，文件用markdown語法寫成
    - layout: post/title/date/categories
- site
    - about
    - assets
    - jekyll


<hr>

### Tutorial 7 Draft
- draft，可以創建一個資料夾，用於存放文章草稿。

### Tutorial 8 Creating Pages
- Jekyll的世界只有兩種，POST/PAGE
- 創建一個文件，以.md為結尾，例如：example.md
- layout: "page" ，一樣是以json格式起頭


### Tutorial 9:Permalinks
一定要三槓(Dash)
---
layout: post
title: "Learning Jekyll Part1.markdown"
date:   2020-01-03 00:47:12 +0800
categories: update
permalink: /:catagories/:year/:day/:title.html
---
 永久連結，可以改變格式


### Tutorial 11: Front Matter Defaults
把文章預設成某種格式 (layout:post)

config.yml
default:
scope:
path:
values:

### Tutorial 12: Layouts
Creat a layout folder


Locoal host path is `http://127.0.0.1:4000/Geek-Log/`

ctr + c => Close the Jekyll server.


# Reference
- [Command Line Usage](https://jekyllrb.com/docs/usage/) 指令用法
- [Configuration](https://jekyllrb.com/docs/configuration/)  調教