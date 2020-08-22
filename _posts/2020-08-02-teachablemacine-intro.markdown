---
layout: post
title:  "Teachable Machine を使ってみよう"
date:   2020-08-02 11:10:00 +0900
author: kztaka
categories: AI teachablemachine
tags: AI "Teachable Machine"
---
Googleの [Teachable Machine](https://teachablemachine.withgoogle.com/) を使ってコンピューター**を**トレーニングしよう。
自分の画像や音声、ポーズを使ってトレーニングすると、コンピュータが学習してそれらを区別できるようになるよ。
![Teachable Machine page](/blog/images/2020/0802-img001.png)

## 画像の区別
似ているが少し違うものを区別することを考えよう。たとえばおかしの「きのこの山」と「たけのこの里」、このおかしを知ってる人なら見るか手でさわるかすれば簡単にどっちか区別することができるね。  
![Teachable Machine page](/blog/images/2020/0802-img002.png)

でもこの区別をプログラミングでコンピューターに教えようとすると難しそうだと想像できるかな？それぞれの特徴を数値化してコンピューターに教える必要がありそうだね。ただ特徴を数値化するといってもどうやって？そもそも特徴とは？人間はどうやってそれを区別しているの？考えるとちょっと難しそうだ。
