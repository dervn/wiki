---
title: "Mac 命令行"
layout: page
date: 2017-09-06 00:00
---

[TOC]

## 计算目录文件大小

    du -sh *
    du -shc * #可最后显示一个Total大小，即当前目录的总大小

参考：[What command combo at terminal will output a list of directories with human-readable sizes?](http://apple.stackexchange.com/questions/6595/what-command-combo-at-terminal-will-output-a-list-of-directories-with-human-read)

## 显示隐藏文件

    defaults write com.apple.finder AppleShowAllFiles -bool true;KillAll Finder
    defaults write com.apple.finder AppleShowAllFiles -bool false;KillAll Finder # 关闭显示隐藏功能

[GUI](show-hidden-script.html)

## 解压缩.tar.gz文件

    tar czf jpg.tar.gz *.jpg #将目录里所有jpg文件打包成jpg.tar后，并且将其用gzip压缩，生成一个gzip压缩过的包，命名为jpg.tar.gz
    tar zxvf test.tar.gz #解压
    tar xzvf test.py.tar.gz -C test1/ #解压文件到指定文件夹
