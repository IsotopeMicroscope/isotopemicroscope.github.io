---
layout: single
classes: wide
title : "スタックや3次元像を使いこなす"
permalink: /analysis/stack_3d/
comments: true
sidebar: 
    nav: "analysis"
---
同位体顕微鏡システムで得られたイメージの解析ソフトウェアとして、フリー（パブリック・ドメイン）の画像処理ソフト「[Fiji/ImageJ](https://imagej.net/Fiji)」用プラグインを産業利用拡大支援室が開発しています。

IMSView関連ファイル一式には、SCAPSのデータを簡単に分析するのに必要な、追加plugin、追加lut、StartupMacrosの修正版とオリジナルが入ってます。ImageJやプラグインは、Windows XP以上、Mac 10.5以上、Linuxで動作します。      

**IMSViewアップデート** 2021-04-27rc   
    - パネルタブ(File, Calc, Measure)を廃止し、ImageJ本体のメニューと重複するボタンを削除しました   
    - Save checked images as TIFF（右の下から２番め）を追加しました   
    - 左下のCheck All, Sync ROIのチェックはどちらも起動時オンにしました   
    - LUT menuが動作していなかったのを修正しました   
{: .notice--info}

ダウンロードは下記より (Zipファイルが開きます)   
[Download](/imsview_allinone2021-04-27rc.zip){: .btn .btn--success}  
過去の更新履歴は，[IILホームページ](https://iil.cris.hokudai.ac.jp/software/imsview/index.html)より見れます．

### インストール   
1. [Fiji/ImageJ](https://imagej.net/Fiji)の公式サイトから、ImageJ bundled with 64-bit Java をダウンロードしてデスクトップなどに解凍する。
2. IMSView関連ファイル一式をダウンロードして解凍し、出てきたフォルダ3つ（luts, macros, plugins）を全て、上で解凍したImageJフォルダの中にコピーする。StartupMacros.txtや古いバージョンのImsVIEW_.jarは上書きでok。
3. ImageJフォルダ内のImageJ.exeをダブルクリックして実行。
   
**Watch out!** Macは、フォルダを同じ名前のフォルダへ上書きする際に、以前のフォルダ内にあったファイルを消して，新しいフォルダの内容のみを貼り付けます。そのため、2の手順で、必要なファイルを消してしまう可能性があります。それぞれのフォルダを開き、中にあるファイルを同名のフォルダへ移動することをおすすめします。
{: .notice--warning}

#### ファイルの紹介
- IMSViewは、SCAPSの解析をするためのプラグインです。
- LUTは、SCAPS像を擬似カラーにするための色の設定です。カラーバーと対応させることで、Pixelのカウントを色として表すことができます。
- StartupMacrosは、ImageJを開いてすぐのバーの右側に、「よく使う機能」へのリンクをまとめたものです。

#### 使用条件
- 自由に使用して頂いて構いません。但し、無保証です。
- ソースコード・バイナリコード共に、複製、改変、頒布していただいて構いません。改変する場合は、クレジット表示を残してください。