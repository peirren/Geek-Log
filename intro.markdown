---
layout: page
title: Jekyll
subtitle: "我的Jekyll目錄"
permalink: /intro/
tags: [Jekyll, tutorial]
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

```
    { % post_url 2010-07-21-name-of-post % }
```


<div class="englishcontent">
If you organize your posts in subdirectories, you need to include subdirectory path to the post:
</div>

如果妳posts資料夾中還有 _子資料夾_ ，路徑必須同樣列出，如下：

`{ % post_url /subdir/2010-07-21-name-of-post % }`

<div class="englishcontent">
There is no need to include the file extension when using the post_url tag.
You can also use this tag to create a link to a post in Markdown as follows:
</div>

*創造連結* 的方法:[馬上來一個]({{% post_url 2019-01-01-welcome-to-jekyll %}})


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


讓讀者自己索取PDF檔案的方法
Linking to a PDF for readers to download:

> ` [ 中括號用來顯示連結文字，小括號放置檔案路徑](/ 路徑 ) `
```md
        ... 歡迎在[這裡索取我的PDF教學](/assets/text.pdf) 
```
檔案連結：[Jekyll Termianl 指令 PDF檔案](/Geek-log/assets/pdf/text.pdf)



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


###Ref
- [Hosting on Github Pages](https://www.youtube.com/watch?v=fqFjuX4VZmU)
- [Jekyll Themee 佈景主題](http://jekyllthemes.org/)
- [有點雜亂的中文解說](http://xareelee.github.io/tech_note/2015/07/23/%E4%BD%BF%E7%94%A8-GitHub-Pages-%E5%92%8C-Jekyll-%E4%BE%86%E5%BB%BA%E7%AB%8B-Blog.html#why_github_pages_and_jekyll)


## TBD QUESTION
- Mastering markdown language 熟悉Markdown的用法
[Help GitHub](https://help.github.com/en/github/working-with-github-pages/about-github-pages-and-jekyll
)


