---
title: Win11右键菜单改回Win10教程
date: 2022-10-11 15:28:50
categories: 前端
tags: 
 - windows 
 - win11
---

恢复Win10右键菜单的方法：
1、Win+R运行CMD

2、输入：
``` java
reg add HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32 /f /ve
```
3、在任务管理器中，重启资源管理器；（或者重启电脑）
![image.png](https://upload-images.jianshu.io/upload_images/3891144-3937a27e415da943.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/400)

恢复Win11右键菜单的方法：
1、Win+R运行CMD

2、输入：
```
reg delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /va /f 
```
3、在任务管理器中，重启资源管理器；