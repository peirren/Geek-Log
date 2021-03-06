---
layout: page
title: Markdown
permalink: /markdown/
---
# 我是標題1
## 我是標題2
### 我是標題3
#### 我是標題4

[Jekyll](/Geek-Log/intro/) 至多可以到標題6。


### 如何強調行內文字呢？粗體與斜體

Markdown使用星號（ * ）和底線（ _ ）作為 __標記強調字詞的符號__ ，被 * 或 _ 包圍的字詞會自動轉換被 `<em>` 標籤包圍，用兩個 * 或 _ 包起來的話，則會被轉成 `<strong>`

#### Q:如果真的要打 * 或 _ 的時候怎麼辦？
A: 在文本內前後空一格，不要包住任何字元。

Markdown是一種 *輕量級標記式* 語言，創始人為約翰·格魯伯（英語：_John Gruber_）。它允許人們「使用易讀易寫的純文字格式編寫文件，然後轉換成有效的XHTML（或者HTML）文件」。這種語言吸收了很多在電子郵件中已有的純文字標記的特性。

由於Markdown的輕量化、易讀易寫特性，並且對於圖片，圖表、數學式都有支援，目前許多網站都廣泛使用 Markdown 來撰寫說明文件或是用於論壇上發表訊息。例如：GitHub、reddit、Diaspora、Stack Exchange、OpenStreetMap 、SourceForge等。甚至Markdown能被使用來撰寫電子書。


---
## 列表語法
創造清單列表內容有多種方法數字列表、星號、加號，如下：
 ```md 
 1. 2. ⋯⋯ (digits), - (dash), * (star), + (plus) 
 ```

- 標題用法
    - 大標題
    - 小標題
- 其他小用法 
 - 引言
 - CheckBox 核准欄位
 - Highlisht 程式碼

* Star 1
* Star 2
+ Plus 3
+ Plus 4

創造分隔線，有兩種寫法：
`* * *` or `***`
* * *

<br>

### 插入圖片語法
驚嘆號 + 中括號 + 小括號 <br>
`![GITHUB]( 圖片網址 "圖片名稱")`


### 引言 (Quote)

如果想要摘要、標記、回覆、引述一個文章段落，就可以使用『引言』，語法都是在每行文字前面加上` > : `

>:不要努力成為一個成功者，要努力成為一個有價值的人。

分行、跳行也是可以唷

>: 愛因斯坦名言：

>>: 我不知道第三次世界大戰會用哪些武器，但第四次世界大戰中人們肯定用的是木棍和石塊。


### CheckBox 核准欄位
用在確認事情是否完成，語法是兩個中括號 `[]` ；若在加入 _x_ 就代表這個項目是被打勾的，它並不會主動紀錄勾選過的內容，所以使用時要確認勾選過的內容是否有增加 ｘ，避免混亂。

- [x] 安裝GA 追蹤碼
- [ ] 創立自己的模板
- [ ] 些微修改頁腳的設計
- [ ] 調教 Config 檔案



### Highlisht 程式碼
清楚標示程式碼有 **三種方法**， 反

1. 單個 反引號 
2. 三個 反引號
3. 四個空白

#### [特別技巧:跳落語法字元]
讓Markdown語法的符號顯示在前端網頁上，而不會被視為程式語言文本之一。

> 用法： **三個反引號** 加上 **程式語言簡寫**
>> 例如：  ` ` ` md ` ` ` 

```md
    ###標題三

    _斜體字用法，卻又不會變成斜體字_
```

^^ 上面那段的原始代碼截圖 ^^
<img src="https://imgur.com/RxjBcol.png">



{% include reference.html %}
+ [官方參考文件](https://markdown.tw/)
+ [IT邦-六角學院](https://ithelp.ithome.com.tw/articles/10203758)
