---
layout: page
title: Accounting
subtitle: "Personal accounting app. developing record｜個人記帳程式開發心得"
permalink: /accounting/
---


# 記帳科目表

| 主科目   | 次科目  | 說明 |
| 飲食   | 吃飯  | 1 |
| 飲食   | 飲料  | 1 |
| 飲食   | 其他  | 1 |
| 衣著   | 藥妝  | 1 |
| 衣著   | 服飾  | 1 |
| 衣著   | 鞋子  | 1 |
| 交通   | 油錢  | 1 |
| 交通   | 保養  | 1 |
| 交通   | 停車  | 1 |
| 交通   | 過路  | 1 |
| 交通   | 禮物  | 1 |
| 娛樂   | 約會  | 1 |
| 娛樂   | 電影  | 1 |
| 娛樂   | 其它  | 1 |
| 娛樂   | 聚會  | 1 |
| 交通   | 停車  | 1 |
| 交通   | 停車  | 1 |

---

# 記帳系統開發紀錄

### 20-03-06
- NEW FILE: myAccount 4.html
- 合併 `myAccount.html` 與 `index.html` ，後者已帶入Bootstrap框架 -> 新檔案名稱：myApp
- 0.45 Upload 到 Bluehost，建立會計科目表，修改Nav清單。
- CSS, JS程式碼使用相對連結(relative link)


### 19-12-06
- 希望讀取最後三筆資料
- 自動讀取當日日期
- 希望送出資料後，自動刪除表單(Input)內資料
- 送出資料後，提示反應"Success"
- 新增快捷功能：加油150元、悠遊卡加值


### 19-10-23
- Button有多種類型(type)，submit直接送出表格，button 可以另外指定功能。
- 沒有辦法驗證資料後才送出表單。
- 常用消費與金額功能
- 新增 "清除資料"功能 

### 19-10-19
- Server端要發布更新，存擋沒有用，必要時要重新建立一支程式來跑、寫入Sheet的功能。
- 所有錯誤Google 都會報錯為>> Cross domain
