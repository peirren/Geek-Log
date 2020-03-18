---
layout: post
title: "Week10 工作日誌"
date:   2020-03-03 23:30:00 +0800
tags: [Update, Weekly Journal]
---

Boostrap如何創造新頁面，既然是Jekyll host的，但是卻不能創造頁面？
`tooltip` 可以運作，但是太大遭遇到排版問題
解決方法改成 attr : "up"; font-size :18px;
暫存在GTM中
- - - 

Jekyll 測試 GTM中



- - -
### Javascritpt `Argumnet`

```
function method(){
    console.log(arguments);
    for(var i=0; i < arguments; i ++)
    console.log(arguments[i]);
};

method(1,2,3)
```
也可以寫成這樣⋯⋯
```
function method(){
{
     for (var i = 0; i < arguments.length; i++) {
          console.log(arguments[i]);
     };
}
method(9,4,5,3)
console.log("這是分隔線");
method(5,2,0);
```
### callee v.s caller
- callee: 為arguments的屬性(property)之一，可取得被call function本身。
- caller:可用來取得call該function的來源物件。

#### 比較簡單的範例：
```
function method(a, b, c) {
     console.log(arguments.callee);
     console.log(arguments.caller);
     console.log(b);
     console.log(c);
}
function callmethod(a)
{
     method(1,3);
}
callmethod();
```
`arguments.callee` 取得arguments所處的function => method
`arguments.caller` arguments不是function因此輸出為 => undefined

第一個function `method` 執行完畢後，繼續執行第二個 function `callmethod` ，並執行函式中的函式`method(1,3)
` 最後互叫她。



稍微複雜範例：
```
function method(a, b, c) {
     console.log(arguments.callee);
     console.log(arguments.callee.caller);
     console.log('宣告參數長度--'+arguments.callee.length);
     console.log('實際參數長度--'+arguments.length);
     console.log('callmethod的參數長度--' + arguments.callee.caller.length)
     console.log(a);
     console.log(b);
     console.log(c);
}
function callmethod(a)
{
     method(1,3);
}
callmethod();
```
### jQuery 動畫
- show&hide
- Animate, Slow or mms

### Git 託管
Github, Gitbucket, Gitlab
Generate a SSH KEY


### HTML file path
Path    Description
|`<img src="picture.jpg"> ` |picture.jpg is located in the same folder as the current page|
|`<img src="images/picture.jpg"> ` |picture.jpg is located in the images folder in the current folder|
|`<img src="/images/picture.jpg">` | picture.jpg is located in the images folder at the root of the current web|
|`<img src="../picture.jpg">` |  picture.jpg is located in the folder one level up from the current folder|


