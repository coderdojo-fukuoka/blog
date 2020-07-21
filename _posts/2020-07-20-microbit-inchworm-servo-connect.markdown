---
layout: post
title:  "micro:bit inchworm しゃくとり虫 - マイクロビットとサーボをつなごう"
date:   2020-07-20 22:15:00 +0900
categories: microbit inchworm servo
---
マイクロビットとサーボをつなごう。

サーボSG90の配線は、[秋月電子のサイト](http://akizukidenshi.com/catalog/g/gM-08761/)をみると、
> ・配線：茶=GND、赤=電源[+]、橙=制御信号 [JRタイプ]

となっている。
```
マイクロビット      サーボ
------------------------
     GND <------>  茶
     3V  <------>  赤
      0  <------>  橙
```
とつなげばよい。

![servo](/blog/images/2020-07-20-img001.png)