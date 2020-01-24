---
layout: post
title: "Learning Jekyll, Part2, Jekyll 資料夾格式"
date:   2019-01-03 00:55:12 +0800
categories: review
author: "Randy"
---


## Directory Structure - Jekyll 資料夾格式

基本的靜態 Jekyll 網站應該長得像是下面這樣⋯⋯
A basic Jekyll site usually looks something like this:



```
.
├── _config.yml
├── _data
|   └── members.yml
├── _drafts
|   ├── begin-with-the-crazy-ideas.md
|   └── on-simplicity-in-technology.md
├── _includes
|   ├── footer.html
|   └── header.html
├── _layouts
|   ├── default.html
|   └── post.html
├── _posts
|   ├── 2007-10-29-why-every-programmer-should-play-nethack.md
|   └── 2009-04-26-barcamp-boston-4-roundup.md
├── _sass
|   ├── _base.scss
|   └── _layout.scss
├── _site
├── .jekyll-metadata
└── index.html # can also be an 'index.md' with valid front matter
```

## An overview of what each of these does:
#### 每一個檔案的概覽如下：

| config.yml| Stores configuration data. Many of these options can be specified from the command line executable but it’s easier to specify them here so you don’t have to remember them.| `config.yml` 是設定檔案資料，存放於yml檔案的指令在這裡都將會被執行唷！|
| includes| These are the partials that can be mixed and matched by your layouts and posts to facilitate reuse. The liquid tag `{ % include file.ext % }` can be used to include the partial in _includes/file.ext.| 透過語法 { include} 呼叫include資料夾內的檔案！ |


