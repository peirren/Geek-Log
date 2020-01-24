---
layout: page
title: 認識Jekyll
permalink: /intro/
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


## 修改 config.yml 檔案
baseurl 與 url 的差別


## 圖片顯示不出來 VVV
[Imgur](https://imgur.com/j7Qi1HM.jpg)



### 階層格式

|Posts||
|     |	Wrapper||
|     | |CSS style|


| 資料夾 | 檔案名稱 |
_layosts | post.html


` Gemfile > url: "___" ` 必填

```
gemfil "jekyll", "~> 3.6.0" 
gemfil "minima", "~> 2.0"

````

###Ref

-[Hosting on Github Pages](https://www.youtube.com/watch?v=fqFjuX4VZmU)
-[Jekyll Themee 佈景主題](http://jekyllthemes.org/)
-[有點雜亂的中文解說](http://xareelee.github.io/tech_note/2015/07/23/%E4%BD%BF%E7%94%A8-GitHub-Pages-%E5%92%8C-Jekyll-%E4%BE%86%E5%BB%BA%E7%AB%8B-Blog.html#why_github_pages_and_jekyll)


## TBD QUESTION
- Mastering markdown language 熟悉Markdown的用法




![Help GitHub](https://help.github.com/en/github/working-with-github-pages/about-github-pages-and-jekyll
)

![123](https://imgur.com/a/VLJbEbO)(Titlte)


