---
layout: post
title:  "Google analytics tracking code between two domain"
date:   2020-01-15 00:00:00 +0800
categories: Draft
teg: "Google analytics"
---

#修改追蹤程式碼以設定跨網域追蹤
如要為多個頂層網域設定跨網域追蹤，您必須分別修改每一個網域上的 Analytics (分析) 追蹤程式碼。進行這項程序的人必須具備基本的 HTML 和 JavaScript 知識；如果您不熟悉相關知識，請找開發人員幫忙設定跨網域追蹤。本文中的範例使用通用 Analytics (分析) 追蹤程式碼片段 (analytics.js)。


1. 在GA帳戶中設定資源：建議新建一項資源，在所有要共同追蹤的網域中，安裝同一組`程式碼`與`Tracking ID`，
1.1. 修改主要網域的追蹤程式碼。
在程式碼片段中找出 create 這一行。如果網站是 example-1.com，這一行看起來會像這樣：


對下列程式碼進行調整 (紅色粗體文字是需要變更的部分)： 
```
  ga('create', 'UA-XXXXXXX-Y', 'example-1.com');

```
  ga('create', 'UA-XXXXXXX-Y', `'auto', {'allowLinker': true});`
  `ga('require', 'linker');`
  `ga('linker:autoLink', ['example-2.com'] );`

別忘了將範例追蹤 ID (UA-XXXXXX-Y) 換成您專用的 ID
範例次要網域 `(example-2.com)` 必須換成次要網域名稱

三個以上的網域追蹤，請另外參考[https://support.google.com/analytics/answer/1034342?hl=zh-Hant](Google文件)

# 建立報表資料&添加篩選器
```
/about/contactUs.html
/about/contactUs.html
/products/buy.html
```

以上三個路近，可能存在在兩個網域底下，GA不會顯示唷！

為了讓報表顯示網域名稱，必須建立報表`資料檢視的複本` (其中包含您所有網域的資料)，然後在這個新資料檢視中`添加進階篩選器`。

這樣就會在GA中顯示真實的網域名稱囉！


## 資料檢視篩選器
跨網域追蹤設定完畢後，請按照本例設定資料檢視篩選器，以便在報表中顯示網域名稱。對於部分欄位，您必須選取下拉式選單中的項目。至於其他欄位，您必須輸入下列字元：

篩選器類型：自訂篩選器 > 進階
欄位 A --> 擷取 A：主機名稱 = (.*)
欄位 B --> 擷取 B：要求 URI = (.*)
輸出至 --> 建構函式：要求 URI = $A1$B1

### 參照連結網址排除清單
前述過程只是讓 A 網域到 B 網域，都共用一個GA檢視資源。這樣還不夠唷，必須還要還要製作`排除清單`。


#### 檢查跨網域追蹤
最後再檢查一下資料囉

---

#### 相關資源
[https://support.google.com/analytics/answer/1034342?hl=zh-Hant][Google原廠文件]

