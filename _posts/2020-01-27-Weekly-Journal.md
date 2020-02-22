---
layout: post
title: "Week4 工作日誌"
date:   2020-01-27 12:30:00 +0800
tags: [Update, Weekly Journal]
---
# 工作日誌 1/28@路易莎

- 建立了 Tag 模板，但是 `/Geek-Log/tags.html' not found.`
- 如果新增或亂改Head.html檔案，原本的設定就會不見！Jekyll預設的佈景主題叫做[minima](https://github.com/jekyll/minima)
- 新學到用[Github issue](https://github.com/peirren/Geek-Log/issues)紀錄開發問題囉，愈來愈覺得自己的思考方式像是個開發者(Programmer)了 :)
- favicon, 不只是把檔案放進去，還要在 `<head>` 中放 `<link rel="shortcut icon" type="image/png" href="favicon.png">` 

```
<link rel="icon" 
    type="image/png" 
    sizes="32x32"
    href="{{ "/assets/favicon-32x32.png" | relative_url }}">
```

Step 3: Edit jekyll plugins.
- Folder includes, then paste that head.html into it.
Open config.yml file in your jekyll folder, under plugins: add in one more line: - jekyll-seo-tag.


[製作Icon參考文件](https://medium.com/@xiang_zhou/how-to-add-a-favicon-to-your-jekyll-site-2ac2179cc2ed)

# Evernote v.s Bear v.s 靜態部落格

|－－－－－|Evernote      |Bear      |靜態部落格(Jekyll or Hexo)      |
|優缺點|能搭建強大的資料庫，適合高度專業使用|支援Markdown語法，      |靜態部落格      |
|技能樹|檔案命名      |Markdown “概念”      |多種語法      |
|費用|我使用免費版本      |付費(每月40元)      |*免費*      |

### 為什麼需要思考這個？
我的筆記已經愈來愈分散，知識太多、思考破碎，就很難內化成一個強大的知識脈絡，希望自己是藉由學習新技能，而獲得新體會，而不只是單純學習、獲得知識。

- 最主要是技術開發的時候，Sublime可以同步開啟，同時當草稿使用。
- 現在最大的問題就是工作思考時的整合
- Evernote 不用程式背景，但有裝置限制。
- Bear 變得有點小雞肋XDD

# 萬用檔案整理術-命名規則 （草稿）


## 關於時間的用法
YYYY-MM-DD = 2020-01-01 OR YYMMDD = 200424 or 190324

## 設計圖片管理
- 原始檔案 (PSD, AI, Original file
- 輸出檔案 (Exported, JPG)


- [ ] Wordpress 相簿，存放像是Flickr那樣的功能。 *需要參考範例* 
- [ ] Wordpress 文章清單，Excel表格。



# 工作日誌 1/27@路易莎
###Jekyll tag問題

```html
<div class="post-tags">
        {% if page.tags.size > 0 %}
          {% for tag in page.tags  %}
            <a href="{{ "/tags.html#" | append: tag | relative_url }}" class="post-tag">{{ tag }}</a>
          {% endfor %}
        {% endif %}
</div>
```

## 問題清單與心得
- 翻譯了很多Jekyll官網很多資料，Configuration, 套件管理
- 從別人的模板主題中複製過來的，但是Ruby判斷式不熟⋯⋯
- 呼叫檔案還在摸索中。