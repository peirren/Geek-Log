---
layout: post
title: "Week9 工作日誌"
date:   2020-02-22 12:30:00 +0800
tags: [Update, Weekly Journal]
---

### [Tooltip](https://codepen.io/randylu/pen/NWqpbbZ)
-[CSS Tooltip Magic@codepen](https://codepen.io/randylu/pen/NWqpbbZ)
- Codepen -> Profile -> Forked

### 選擇器[]
- CSS `[attribute*=value]` Selector

Example:

指定特殊class是test的背景顏色
```
div[class*="test"] {
  background: #ffff00;
}
```

- - -
## Bootstrap Grid System Note
- [40行實作響應式的佈局系統](https://medium.com/@realdennis/40%E8%A1%8C%E5%AF%A6%E4%BD%9C%E9%9F%BF%E6%87%89%E5%BC%8F%E7%9A%84%E4%BD%88%E5%B1%80%E7%B3%BB%E7%B5%B1-%E5%91%8A%E8%A8%B4%E4%BD%A0col-sm-12-col-md-6-%E6%98%AF%E5%A6%82%E4%BD%95%E5%AF%A6%E7%8F%BE-4490a65b1a0)
- [Codepen](https://codepen.io/randylu/pen/oNXZOex)

### 規則
Grid System是經由`Row(列`和`Column(行)`來建立頁面的架構的，然後再將內容裝在這些由Row(列)和Column(行)組成的框框裡面。簡述規則如下：

- class的結構依序為：.container(固定寬度) 或 .container-fluid(滿版，看範例) -> .row -> Column。「.container」或「.container-fluid」讓版面有適當的對齊方式(alignment)和間格(padding)。
- 使用水平方向的「.row」來群組Column。
- 內容放在Column之內，且Column一定緊接在「.row」之下，是為Immediate Children。
- 使用class「.row」或「.col-xs-4」來建立頁面的架構，也可以使用Less mixins and variables來做設定或調整。
- Column為最小單位的方格，且有間格將彼此格開，並由「.row」使用負的margin值校正因Column而多出來的左右padding。
- 指定Column的格數(最多到12)，例如一列希望有3個相等的Column，可指定3個「.col-xs-4」。
- 基本上一個Row放置12個Column，若有一個Row超過12個Column，則會斷行放置多出來的Column。
使用Grid Class會影響到大於/等於設定分段點的Device，例如：使用「.col-md-*」不僅會影響到Desktop，若沒有設定「.col-lg-*」，還會影響到Large Desktop。

#### Media Queries的分段點
- Mobile – xs ( < 768px )
- Tablet – sm ( 768~991px )
- Desktop – md ( 992~1200px )
- Large Desktop - lg ( >= 1200px )



- - -

### 碰到什麼問題...?

- 在試著導入Bootstrap ana template時意外導致Jekyll佈景主題[minima](https://github.com/jekyll/minima)版型遺失。

-- Boostrap 有個不錯用的範例[Examples](https://getbootstrap.com/docs/4.4/examples/)可以套用在Shopline 404頁面中，[Product](https://getbootstrap.com/docs/4.4/examples/product/)


### git的 .ignore ([Ref](https://gitbook.tw/chapters/using-git/ignore.html))
檔案不想要放到git，需要無視時，

```
$ touch .gitignore
```
這裏整理了一份各種程式語言常見的 .gitignore 檔案。 網址： https://github.com/github/gitignore