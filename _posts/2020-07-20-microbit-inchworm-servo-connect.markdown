---
layout: post
title:  "micro:bit inchworm しゃくとり虫 - マイクロビットとサーボをつなごう"
date:   2020-07-20 22:15:00 +0900
update: 2020-08-02 10:00:00 +0900
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
※実際の線の色は「赤」がオレンジ、「橙（だいだい）」が黄色に近い

![connector](/blog/images/2020-07-20-img002.png)

![MakeCode servo](/blog/images/2020-07-20-img001.png)