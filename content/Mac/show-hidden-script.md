---
title: "AppleScript 切换显示/隐藏GUI"
layout: page
date: 2017-09-08 00:00
---

## AppleScript 切换显示/隐藏GUI

作者：Linkzero Tsang
链接： https://www.zhihu.com/question/24635640/answer/28455134

鼓捣过一个 AppleScript, 做了个有 GUI 的小程序。可以打开 AppleScript 编辑器 这个自带 App, 新建一个文档，将下面的代码粘贴进去，编译，然后导出 .app 应用程序，方便切换显示/隐藏两个状态。

```
display dialog "隐藏/显示隐藏文件" buttons {"可见", "隐藏"} with icon 2 with title "Switch to presentation mode" default button 1

set switch to button returned of result

if switch is "隐藏" then
	do shell script "defaults write com.apple.finder AppleShowAllFiles -bool false;
KillAll Finder"

else
	do shell script "defaults write com.apple.finder AppleShowAllFiles -bool true;
KillAll Finder"

end if

```
