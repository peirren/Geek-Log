---
layout: page
title: Jekyll
subtitle: "我的Jekyll筆記"
permalink: /intro/
tags: ["Jekyll", "tutorial"]
---



## 之後要放到 `Jekyll語法的部分`
- 為什麼我喜歡Jekyll
- Jekyll的優勢與缺點、前置條件需要什麼


## In this article
- About Jekyll
- Configuring Jekyll in your GitHub Pages site
- Front matter
- Themes
- Plugins
- Syntax highlighting
- Building your site locally


### Read Me 檔案
Jekyll 預設佈景主題是 Minima
![Minima](/assets/img/basic-jekyll.png)
01/28 嘗試啟動，失敗。Q_Q


## 修改Layout
想要修改的原因是，Jekyll雖然是靜態部落格，但是有類似PHP模組化的概念，又不會像PHP這麼複雜，而Server的問題可以交給Github host。
同樣一樣有Template, Page的概念，與WordPress雷同。

用 Wrapper 去包含程式碼，在用posts去製作全部的版型


Folder include, adding a new file: ga_script, pretending some mock-up, nav bar or something functional feature.
資料夾_includes >> 新增 ga_script 預先放程式碼，可以之後放GA的追蹤碼。


#### Layout 

|檔案名稱 | 用途       |說明
|default | 預設       | 預設                                         |
|page    | 獨立頁面    | 如果沒有可以新增，並且呼叫default，基本款互相引用。  |
|psot    | 文章       |   |

##### Layout的說明
所有的頁面或文章都是 **default** ，因此如果要更動 *page* 時候，必須先在MD文章前面呼叫 `layout: default`。 才開始進行修改。




### Content 內容
<label class="mylabel">[資料來源官方網站](https://jekyllrb.com/docs/posts/)</label>

<div class="englishcontent">
Blogging is baked into Jekyll. You write blog posts as text files and Jekyll provides everything you need to turn it into a blog.
</div>

可以使用HTML與Markdown兩種語法混用，Jekyll會自動幫忙轉換成Blog形式。

<div class="englishcontent">
    The _posts folder is where your blog posts live. You typically write posts in Markdown, HTML is also supported.
</div>

`_post` 資料夾用來存放所有的文章。

文章格式必須按照 `YEAR-MONTH-DAY-title.MARKUP` 這種格式。

<div class="englishcontent">
All blog post files must begin with front matter which is typically used to set a layout or other meta data. For a simple example this can just be empty:
</div>


---

<br>

> ProTip™: Link to other posts
Use the post_url tag to link to other posts without having to worry about the URLs breaking when the site permalink style changes.

>> 進階技巧：連接到其他文章


#### Linking to posts Permalink
<div class="englishcontent">
If you want to include a link to a post on your site, the post_url tag will generate the correct permalink URL for the post you specify.
</div>

{% highlight ruby %}
    { % post_url 2010-07-21-name-of-post % }
{% endhighlight %}

<div class="englishcontent">
If you organize your posts in subdirectories, you need to include subdirectory path to the post:
</div>

如果妳 posts 資料夾中還有 _子資料夾_ ，路徑必須同樣列出，如下：

{% highlight ruby %}
    { % post_url /subdir/2010-07-21-name-of-post % }
    { % post_url 2019-01-01-welcome-to-jekyll.md % }
{% endhighlight %}

<div class="englishcontent">
There is no need to include the file extension when using the post_url tag.
You can also use this tag to create a link to a post in Markdown as follows:
</div>


```
* 有問題 VVV *

*創造連結* 的方法:[馬上來一個]({{ % post_url posts/2019-01-01-welcome-to-jekyll % }})
```

## 呼叫圖片與其他資源
###### [Including images and resources - Official](https://jekyllrb.com/docs/posts/#the-posts-folder)
<div class="englishcontent">
At some point, you’ll want to include images, downloads, or other digital assets along with your text content. One common solution is to create a folder in the root of the project directory called something like assets, into which any images, files or other resources are placed. Then, from within any post, they can be linked to using the site’s root as the path for the asset to include. The best way to do this depends on the way your site’s (sub)domain and path are configured, but here are some simple examples in Markdown:
</div>

Including an image asset in a post:

```md 
    ... which is shown in the screenshot below:
![My helpful screenshot](/assets/screenshot.jpg)
```
### 哪一種呼叫圖片的方式有效呢？
1. ![My helpful screenshot](/Geek-log/assets/s9OfhzA.jpg)
2. ![My helpful screenshot](/assets/img/s9OfhzA.jpg)
3. ![My helpful screenshot](/assets/s9OfhzA.jpg)
4. ![My helpful screenshot](/Geek-Log/assets/img/s9OfhzA.jpg)
5. ![Ruby 101]((/Geek-Log/assets/img/ruby.png))


讓讀者自己索取PDF檔案的方法
Linking to a PDF for readers to download:

> ` [ 中括號用來顯示連結文字，小括號放置檔案路徑](/ 路徑 ) `
```md
        ... 歡迎在[這裡索取我的PDF教學](/assets/text.pdf) 
```
檔案連結：[Jekyll Termianl 指令 PDF檔案](/Geek-log/assets/pdf/text.pdf)


# [Ruby 101](https://jekyllrb.com/docs/ruby-101/)
## Jekyll is written in Ruby. If you’re new to Ruby, this page is to help you get up to speed with some of the terminology.
Jekyll用Ruby寫成，如果你和我一樣是Ruby新手，這章節可以幫助你更快暸解Ruby的用法。
# Gems
## A gem is code you can include in Ruby projects. It allows you to package up functionality and share it across other projects or with other people. Gems can perform functionality such as:

+ Converting a Ruby object to JSON
+ Pagination
+ Interacting with APIs such as GitHub
+ Jekyll itself is a gem as well as many Jekyll plugins including jekyll-feed, jekyll-seo-tag and jekyll-archives.

Gem寶石的意思，也就是Ruby的函式庫，已經幫使用者把一堆功能打包起來，並且分享給其他使用者，Gem的基本功能包括：

+ 把 Ruby 物件轉換成 JSON **因此Gemfile是JSON格式**
+ Pagination 把文檔分頁，如果少了這個網站就會是所謂的一頁式網站，文章延續下去。
+ Gem 還能幫助使用者處理 API，例如:Github
+ 當然，Jekyll也有許多寫好的Plugin 像是 (jekyll-feed)[https://github.com/jekyll/jekyll-feed], (jekyll-seo-tag)[https://github.com/jekyll/jekyll-feed], (jekyll-archives)[https://github.com/jekyll/jekyll-archives]

<label class="mylabel">
    參考資料：[Ruby官方解釋](https://www.ruby-lang.org/zh_tw/libraries/)
</label>

# Gemfile
## Gemfile 是Ruby的套件，設計者寫好一串Ruby函式打包成一個檔案，讓網站可以使用，長得會像這樣：
A `Gemfile` is a list of gems required for your site. For a simple Jekyll site it might look something like this:
<img src="https://imgur.com/NpsD8Mq" alt="Gemfile">

# Bundler 
管理 Ruby套件的程式。

<label class="mylabel">
    參考資料：[RVM,GEM,Bundler是什麼？](http://sayaku.github.io/blog/2016/05/05/rubyde-rvm-gem-bundler/)
</label>

# Configuration 調教
## Jekyll 給予使用者許多客製化的彈性，更動這兩個檔案 `_config.yml`, `_config.toml` 可以更許多設定，例如：檔案位置、圖檔存放位置、網站編碼、時區，等等⋯⋯

Jekyll gives you a lot of flexibility to customize how it builds your site. These options can either be specified in a `_config.yml` or `_config.toml` file placed in your site’s root directory, or can be specified as flags for the jekyll executable in the terminal.

[官方文件 Configuration-official](https://jekyllrb.com/docs/configuration/)

## 修改 config.yml 檔案
[疑問]baseurl 與 url 的差別，不是很熟練。
<img src="https://imgur.com/j7Qi1HM.jpg">
```
### 階層格式

|Posts||
|     |	Wrapper||
|     | |CSS style|

| 資料夾 | 檔案名稱 |
_layosts | post.html

` Gemfile > url: "___" ` 必填 `

```

```
gemfil "jekyll", "~> 3.6.0" 
gemfil "minima", "~> 2.0"
````

# Front matter
Markdown 檔案最初用三個dash(-)，分隔的區域，用來指定檔案的變數，舉例來說：
```
---
title: This Front matter example
date: 2020/2/20 20:20:20
---
```

[原廠說明](https://jekyllrb.com/docs/configuration/front-matter-defaults/)蠻多資料需要閱讀的T_T


###Ref
- [Hosting on Github Pages](https://www.youtube.com/watch?v=fqFjuX4VZmU)
- [Jekyll Themee 佈景主題](http://jekyllthemes.org/)
- [有點雜亂的中文解說](http://xareelee.github.io/tech_note/2015/07/23/%E4%BD%BF%E7%94%A8-GitHub-Pages-%E5%92%8C-Jekyll-%E4%BE%86%E5%BB%BA%E7%AB%8B-Blog.html#why_github_pages_and_jekyll)


## TBD QUESTION
- Mastering markdown language 熟悉Markdown的用法
[Help GitHub](https://help.github.com/en/github/working-with-github-pages/about-github-pages-and-jekyll
)


