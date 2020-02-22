---
layout: default
title: "Week6 工作日誌"
date:   2020-02-08 12:30:00 +0800
tags: [Update, Weekly Journal]
---

# 2/10 SHOPLINE模板大進展
感謝愛禮物的前輩大神，截圖給我看，瞬間全懂了！爽到不行。目前施作的是[測試頁面](https://www.homiya.co/pages/randy-is-testing)。
- - -   
### 簡單原理暸解
Liqiud 的 `{ % if %}` `{ % endif %}` 邏輯判斷式，第一步就是在主機判斷，page.url 是否為特定活動頁面，如果是的話，就要呼叫特定程式代碼，也就是讓消費者看到特定活動內容。 <br>


>> 換句話說，Liquid的基本邏輯if, else很重要呀！！！
>>> 當然前端三劍客也是很重要。

另外，setting.json 必須設定，如下：
```
{
    "root_path": "/",
    "testing_path": "/pages/randy-is-testing"
}
```


#### 測試中的代碼
[3 Column Responsive Layout](https://codepen.io/Cheesetoast/pen/KFAaq) Source.

```
<div class="wrapper">

    <header>
        <h1>消費常見問題</h1>
    </header>
        
<section class="columns">
    
    <div class="column">
        <h2>你的問題一，哇哈哈哈哈</h2>
        <p>智慧圖書館是以自動化設備取代傳統人力資源，提供入館讀者以自助方式借閱或歸還書籍，因無人力查找及整理預約書，故智慧圖書館之館藏不提供讀者預約。</p>
    </div>
    
    <div class="column">
        <h2>你的問題一，哇哈哈哈哈</h2>
        <p>目前僅有「社子島智慧圖書館」提供自助預約取書服務，讀者可於本館館藏查詢系統中預約圖書，並選擇於社子島智慧圖書館領取。
其他智慧圖書館則無提供預約取書服務。</p>
    </div>
  
  <div class="column">
        <h2>你的問題一，哇哈哈哈哈</h2>
        <p>慧圖書館是以自動化設備取代傳統人力資源，提供入館讀者以自助方式借閱或歸還書籍，因無人力查找及整理預約書，故智慧圖書館之館藏不提供讀者預約。</p>
    </div>
    
</section>  

```





2/9 Sat.

安裝 Bootstrap 本機端
加入 Shopify Partner
Shopline 404應用
下一步，


年前熟悉Github, Jekyll模組化，今天又摸了框架、更能修改應用程式了




Bootstrap-4.4.1
 - install `public_suffix`
 - Run `bundle install` to install missing gems.
 - Installing public_suffix 4.0.1
  * 自動安裝需要的套件

-[Liquid file requirements for themes](
  https://help.shopify.com/en/themes/development/theme-store-requirements/theme-file-requirements#recommendations)


Shopify Partner
- Development store
- Managed store

有兩種選項，可以作為開發者或店主。

Shopify 積極打造開發、電商生態圈，Partner 內容持續更新中。




