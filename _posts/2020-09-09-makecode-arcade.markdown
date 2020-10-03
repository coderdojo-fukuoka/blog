---
layout: post
title:  "MakeCode Arcade - レトロなゲームをモダンなプログラミングで "
date:   2020-09-09 08:30:00 +0900
author: kztaka
categories: Arcade
tags: Arcade
---
[MakeCode Arcade (マイクロソフト メイクコード アーケード)](https://arcade.makecode.com/){:target="_blank"} を知っているかな。

![img001](/blog/images/2020/0909-img001.gif)

[マイクロソフト メイクコード](https://www.microsoft.com/){:target="_blank"}はマイクロソフトが無料で公開しているプログラミングツールだ。[microbit](https://makecode.microbit.org/){:target="_blank"}や[マインクラフト](https://minecraft.makecode.com/){:target="_blank"}のプログラミングで使ったことがある人もいると思う。

マイクロソフト メイクコード

![img002](/blog/images/2020/0909-img002.png)

少し下に Arcade がある

![img003](/blog/images/2020/0909-img003.png)

Arcadeは[メイクコードの公式Blog](https://makecode.com/blog/arcade/01-18-2019){:target="_blank"}では
> Microsoft MakeCode Arcade is a web-based beginner-friendly code editor to create retro arcade games for the web and for dedicated hardware.

と紹介されている。マイクロソフト メイクコード アーケードは、
1. ウェブベースの（ブラウザで使える）初心者にもやさしいプログラミングツール
2. レトロアーケードゲーム（なつかしいゲームセーンターにあるようなゲーム）を作ることができる
3. 作ったゲームはブラウザや、対応するハードウェアで動かすことができる

ということだ。

どんなものか知るためにはさわってみるのが早い。
サンプルプログラムを動かして、ハードウェアにも転送してみよう。

「Arcade でプログラミングを始める」をクリックすると

![img004](/blog/images/2020/0909-img004.png)

Arcadeの画面が開く。これがArcadeの画面だ。

![img005](/blog/images/2020/0909-img005.png)

少し下にスクロールすると「ブロックゲーム」というのがある。ここの「Falling Duck」をクリックしてみよう。

![img006](/blog/images/2020/0909-img006.png)

「サンプルを開く」をクリック

![img007](/blog/images/2020/0909-img007.png)

Falling Duckの画面が開く。

![img008](/blog/images/2020/0909-img008.png)

micro:bitのメイクコードと同じように、画面の右側ににプログラム、左側にハードウェアのエミュレーターが表示される。
まずはエミュレーター上でゲームを遊んでみよう！

右側のプログラムエディターも高機能だ。プログラムをブロックからJavaScriptやPyhonに切り替えることもできる。またデバッグモードで変数の内容を確認しながらプログラムを１ブロックずつ進めることもできる。

JavaScriptに切り替え

![img009](/blog/images/2020/0909-img009.png)

デバッグモードでブロックを1ステップずつ実行

![img010](/blog/images/2020/0909-img010.png)


初心者にもやさしいが、本格的な開発もできそうだね。



次に実物のハードウェアにゲームを転送してみよう。

対応するハードウェアは「ハーウェア」で紹介されている。

![img011](/blog/images/2020/0909-img011.png)

ここにあるハードウェアを買ってもいいし、この中の「Adafruit M4」、「Add Board」を参考に自分で作ることもできる。

![img012](/blog/images/2020/0909-img012.png)

![img013](/blog/images/2020/0909-img013.png)


実際に作ったのがこれだ。これに「Falling Duck」を転送する。

![img015](/blog/images/2020/0909-img015.png)

自分で作ったハードウェアでゲームが動いた！

![img014](/blog/images/2020/0909-img014.gif)


部品のそろえかたや作り方、プログラムの転送のやりかたは別のページで紹介するね。



