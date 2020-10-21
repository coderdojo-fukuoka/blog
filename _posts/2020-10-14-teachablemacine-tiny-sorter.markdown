---
layout: post
title:  "Teachable Machine  (3) - Tiny Sorterを作ってみよう"
date:   2020-10-14 16:30:00 +0900
author: kztaka
categories: AI teachablemachine
tags: AI "Teachable Machine" Scratch microbit
---
Tiny Sorterを作ってみよう。

![img001](/blog/images/2020/1014-img001.png)

Teachable Machineでマシュマロとシリアルを区別し、サーボを使って左右にふり分ける装置だ。

[Tiny Sorter(https://experiments.withgoogle.com/tiny-sorter/view)](https://experiments.withgoogle.com/tiny-sorter/view){:target="_blank"}に作り方がのっている。日本語ページはないのでChromeの翻訳機能で日本語にしてみよう。

![img002](/blog/images/2020/1014-img002.png)

この作り方ではサーボのコントローラーにArduino Leonardoを使っている。Arduino Unoでは動かないので注意しよう（WebUSBに対応したArduinoのみ。対応機種の一覧は[WebUSB/Arduino](https://github.com/webusb/arduino){:target="_blank"}にのっている）。

Arduino Leonardo、持っている人は少ないかもしれない。ここでは手軽に手に入るmicro:bitを使って作ってみよう。

## 材料
材料は[しゃくとり虫](/blog/microbit/inchworm/2020/07/16/microbit-inchworm.html)と同じものが使える。
* micro:bit
* サーボSG90
* ワニ口クリップコード
* ジャンパーワイヤー

福岡市ならば[カホパーツセンター](http://www.kahoparts.co.jp){:target="_blank"}、通販ならば[秋月電子](https://akizukidenshi.com/catalog/top.aspx){:target="_blank"}などで手に入る。
くわしくは[しゃくとり虫の材料](/blog/microbit/inchworm/2020/07/21/microbit-inchworm-materials.html)「部品の購入先」をみてね。

それ以外に必要なものは
* 厚紙（ケント紙など）
* プリンター（厚紙に型紙を印刷する）
* 動眼（ぬいぐるみ用の動く目、紙でつくってもよい）
* ハサミ
* セロテープ
* 定規（厚紙を折り曲げるときに使う）

だ。ケント紙や動眼は100円ショップにもあるよ。

ダイソーのケント紙とユザワヤで買った動眼

![img003](/blog/images/2020/1014-img003.png)

## 組み立て
### ソーターの組み立て
Tiny Sorterの作り方のページに型紙のPDFがある。まずはこれをダウンロードしよう。

![img004](/blog/images/2020/1014-img004.png)

これを厚紙に100%の大きさで印刷する。印刷したあと1インチの線を測って1インチ(2.54cm)であることを確かめよう。

![img0005](/blog/images/2020/1014-img005.png)

組み立ては [Tiny Sorterのページ](https://experiments.withgoogle.com/tiny-sorter/view){:target="_blank"} の「1.Assemble your sorter」の通りで良い。
「C. Put it all together」の3/4のサーボの取り付けは、サーボのコードが上にくるように取り付ける。

![img006](/blog/images/2020/1014-img006.png)

![img007](/blog/images/2020/1014-img007.png)

![img008](/blog/images/2020/1014-img008.png)

また、4/4のつなぎ方だが micro:bitとサーボはこのようにつなぐ（[しゃくとり虫](/blog/microbit/inchworm/2020/07/14/microbit-inchworm-dryrun.html)と同じつなぎ方だ）。

![img009](/blog/images/2020/1014-img009.png)

## サーボを動かす
ここでは [Teachable Machine  (2) - Scratchと連携してみよう](/blog/ai/teachablemachine/2020/08/17/teachablemacine-scratch.html) と同じ「[Stretch3](https://stretch3.github.io/){:target="_blank"}」を使おう。Stretch3はTeachable Machineのモデルだけでなく、micro:bitもプログラムできるのでTiny Sorterにぴったりだ。

まずはサーボを動かすために [サーボをゆらすプログラム(servoshake.sb3)](https://github.com/coderdojo-fukuoka/archives/raw/master/stretch3/tinysorter/servoshake.sb3) をダウンロードしてStretch3で読み込もう。

![img010](/blog/images/2020/1014-img010.png)

プログラムといっしょに拡張機能「micro:bit more」が自動的に読み込まれる。ブロックパレットの「micro:bit more」をクリックし、micro:bit moreのブロックを表示する。
micro:bitと接続されていない場合は「!」アイコンが表示されているのでクリックする。
画面にしたがってmicro:bitを接続しよう（Scratch Linkはあらかじめ起動しておく）。

![img011](/blog/images/2020/1014-img011.png)

![img012](/blog/images/2020/1014-img012.png)

接続が成功すると「!」アイコンが緑のチェックに変わる。

![img013](/blog/images/2020/1014-img013.png)

接続ができたらmicro:bitのAボタンを押してみよう。サーボが左右にゆれ始めるはずだ。
Bボタンを押すと止まる。

## トレーニング
次にTeachable Machineを使って画像データのトレーニングをしよう。区別するもの（マシュマロとシリアルなど）を用意し、
[Tiny Sorterのページ](https://experiments.withgoogle.com/tiny-sorter/view){:target="_blank"} の「3.Train your model」の手順でトレーニングを行う。
ただし 手順8/8はp5の画面ではなくStretch3の「画像分類モデルURL（がぞうぶんるいモデル）」ブロックにはりつける（下の「Tiny Sorterを動かすプログラム）。

トレーニングはサーボをゆらしながら行う。サーボをゆらすには上で試した[サーボをゆらすプログラム(servoshake.sb3)](https://github.com/coderdojo-fukuoka/archives/raw/master/stretch3/tinysorter/servoshake.sb3)を使おう。Stretch3とTeachable Machineはそれぞれ別のChromeウィンドウで起動しよう（1つのChromeの別タブで動作させると動きが遅くなる）。

## Tiny Sorterを動かすプログラム
[Tiny Sorterを動かすプログラム](https://github.com/coderdojo-fukuoka/archives/raw/master/stretch3/tinysorter/tinysorter.sb3)をダウンロードし、Stretch3で読み込む。

画像分類モデルURLはここに貼り付ける。

![img014](/blog/images/2020/1014-img014.png)

## 完成
区別するものをソーターの上にならべてAボタンを押してみよう。

![img001](/blog/images/2020/1014-img001.png)

ここではマシュマロとシリアルの代わりに色の違う星型ビーズを使っている。星型ビーズはサーボでソーターがゆれるとすこしずつ前に進んでくる（モニターのかたむきを調整して進み方を調節しよう）。他にも柿の種とピーナツの区別などいろいろ試してみよう。ソーターに並べるものはすこし表面がざらざらしているもののほうがうまくいくようだ。丸いもの（大豆とあずきなど）は転がり過ぎてうまくいかない。いろいろ試してみよう！