---
layout: post
title:  "Teachable Machine  (2) - Scratchと連携してみよう"
date:   2020-08-17 08:40:00 +0900
author: kztaka
categories: AI teachablemachine
tags: AI "Teachable Machine" Scratch
---
Teachable Machineで画像などの区別ができるようになったら、そのモデルを使ってScratchでプログラミングしてみよう。

まずはTeachable Machineでトレーニング済みのモデルを保存しよう。Scratchで使うにはクラウド上（インターネット上）に保存する。

「プレビュー」エリアの「モデルをエクスポートする」をクリックしよう

![img001](/blog/images/2020/0817-img001.png)

「モデルをアップロード」をクリック

![img002](/blog/images/2020/0817-img002.png)

「共有可能なリンク」にアップロードされたモデルのURLが表示されるのでコピーして、次のTM2Scratchのブロックにはりつける

![img003](/blog/images/2020/0817-img003.png)

この「モデルをアップロード」ではトレーニング済みのモデルだけがアップロードされる。トレーニング用に追加した写真はアップロードされないので安心しよう。逆に写真を含めてプロジェクトを保存したい場合は「プロジェクトをファイルとしてダウンロード」をする。

![img004](/blog/images/2020/0817-img004.png)

![img005](/blog/images/2020/0817-img005.png)

モデルのアップロードができたらScratchを開く。ここではTeachable Machineのモデルを使える拡張機能「TM2Scratch」を使うために、カスタマイズされたScratchである [Streach3(https://stretch3.github.io/)](https://stretch3.github.io/){:target="_blank"} を使おう。

![img006](/blog/images/2020/0817-img006.png)

「拡張機能を追加（かくちょうきのうをついか）」をクリックすると「拡張機能を選ぶ（かくちょうきのうをえらぶ）」画面が表示されるので「TM2Scratch」をクリックする。

![img007](/blog/images/2020/0817-img007.png)

![img008](/blog/images/2020/0817-img008.png)

TM2Scratchのブロックが表示される

![img009](/blog/images/2020/0817-img009.png)

まずは「画像分類モデルURL（がぞうぶんるいモデル）」ブロックをコードエリアにもってこよう。

![img010](/blog/images/2020/0817-img010.png)

その「画像分類モデルURL（がぞうぶんるいモデル）」ブロックに、上でコピーしたURLを貼り付けよう。

![img011](/blog/images/2020/0817-img011.png)

「画像分類モデルURL（がぞうぶんるいモデル）」ブロックをクリックすると、URLからモデルが読み込まれる（すこし時間がかかる）。
読み込みが完了すると、「画像ラベルのどれかを受け取った時（がぞうラベルのどれかをうけとったとき）」ブロックの「のどれか」の部分が選べるようになる。

![img012](/blog/images/2020/0817-img012.png)

画像ラベルが「きのこの山」のとき「きのこの山！」と言い、「たけのこの里」のとき「たけのこの里！」というプログラムを作ってみよう。

![img013](/blog/images/2020/0817-img013.png)

試してみると、

![img014](/blog/images/2020/0817-img014.png)

![img015](/blog/images/2020/0817-img015.png)

成功だ！
