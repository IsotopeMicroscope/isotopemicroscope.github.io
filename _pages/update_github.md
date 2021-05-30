---
layout: single
classes: wide
title : "Githubを用いたページ更新"
permalink: /update/
comments: true
sidebar: 
    nav: "analysis"
---
### この記事の目的
この記事では，本サイトの更新についての方法を説明します．   
今後，このサイトの情報を拡充する上で，同位体顕微鏡に関わる方々にもコンテンツをご提供いただくかもしれません．   
このサイトは，Github pagesの機能を用いて，作成されていて，「多人数で制作に参加できる」ようになっています．ぜひ，こちらの情報をご参照頂き，今後，記事作成をお願いできますと嬉しいです．

### 作成で役立つリンク
- [本サイトのレポジトリ](https://github.com/IsotopeMicroscope/isotopemicroscope.github.io/tree/gh-pages)
- [更新履歴](https://github.com/IsotopeMicroscope/isotopemicroscope.github.io/commits/gh-pages)
#### 編集に役立つサイト   
- [Minimal Mistakesマークアップシート](https://mmistakes.github.io/minimal-mistakes/markup/markup-html-tags-and-formatting/)   
- [Minimal Mistakes 画像・動画など埋め込み方法](https://mmistakes.github.io/minimal-mistakes/docs/helpers/)
- [Markdownチートシート](https://qiita.com/Qiita/items/c686397e4a0f4f11683d)    
#### 編集で使用するソフトウェア・ツール   
- [Visual Studio code](https://code.visualstudio.com/)   
- [GitHub Desktop](https://desktop.github.com/)
- [LossLessCut](https://github.com/mifi/lossless-cut)
#### VS code内の拡張機能   
- [Japanese Language Pack for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-ja)
- [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
- [Markdown Preview Github Styling](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles)

### 記事ファイルの作成方法
このサイトのファイルには，3種類あります．   
1. 記事への導線やトップページのデザインなど，「機能」を優先して作られたページのファイル．例：[トップページ](/)，[SCAPS像の分析手順](/analysis/)
2. 記事のコンテンツそのもののページのファイル．".md"ファイルで作られています．例：[明るさ・コントラストの調整方法](/analysis/b_c_lut/)
3. ページのバックグラウンドに関係するファイル(写真やcss，ymlなど)．   

追記いただきたいのは，おもに2の記事コンテンツです．   

記事コンテンツは次のような流れで作成出来ます．   
#### 編集権限をお持ちの場合   
【推奨】github desktopとvs codeで作成後，pushしてください．本体のページが直接更新されます．   

#### 編集権限を持っていない場合   
【推奨】[git hub pagesのディレクトリ](https://github.com/IsotopeMicroscope/isotopemicroscope.github.io/tree/gh-pages)をフォークの上，お手持ちの端末で編集，ご自身のGithubディレクトリ上に同期させた後，pullリクエストを送ってください．その際に，gh-pagesへのmerge希望を行ってください．(動画での解説予定)

その他，次の２つの方法がありえます(1より2のほうがありがたいです．)

【初歩1】Wordファイル，または，Google documentでお送りください．   
【初歩2】ファイル本体を記入した.mdファイルをお送りください．写真等の添付がある場合には同じ名前のディレクトリを作成し，その中に写真などを埋め込み，".md"ファイルとフォルダを1つのzipファイルにまとめてお送りください．
{: .notice--info} 

お送り頂いた記事は，レビュー・体裁や内容の修正のなどを行った上で，公開します．

### 記事の雛形   
このページのローデータは[こちら](https://github.com/IsotopeMicroscope/isotopemicroscope.github.io/blob/gh-pages/_pages/update_github.md)です．雛形としてご利用ください．

1. 記事のファイル形式はmarkdown (.md)です． 
2. 改行は文末にスペースを複数(2つ)入れていください (1行空白の行を入れるか，brタグでも改行可能です．)．  
3. ヘッダーは下記から#以下を除いてご利用ください．titleとpermalinkは適宜更新してください．


```
---
layout: single # Don't touch.
classes: wide # Don't touch.
title : "Githubを用いたページ更新" # This is a title of the page.
permalink: /update/ #This is a url where the page will appear.
comments: true  # A comment bar may or may not appear at the bottom.
sidebar: # Don't touch.
    nav: "analysis" # Don't touch.
---
ここから下に，markdown形式で記事を記入ください．
```

### 解説動画  
#### 動画1) VScode・Github desktopの導入まで   
{% include video id="1LCNpWuU1HNorvVph6WvO24_iFiMeVjn3" provider="google-drive" %}
#### 動画2) 上記ソフトウェアを利用したファイルの更新まで   
{% include video id="1x2jczeMgkRVKvujIuMFebOBjDbMZG8tf" provider="google-drive" %}

※pull requestの方法は，後日更新します．   

#### 動画 おまけ) Localでgit hub pagesを確認しよう!
この動画では，githubへpushせずとも，手元でページを確認できる方法を紹介しています．とりあえずは，windowsユーザー向けの紹介です．  
{% include video id="1SEjd1LCqznSz5uVg4lh6nxl7wTYO_h6d" provider="google-drive" %}

参考リンク：   
1. [Jekyll on Windows](https://jekyllrb.com/docs/installation/windows/)   
2. [RubyInstaller for 2.7.2-1](https://rubyinstaller.org/2020/10/06/rubyinstaller-2.7.2-1-2.6.6-2-and-2.5.8-2-released.html)   

コマンドは，ページのおいてあるフォルダへ"cd"したあと，下記を打つだけOKです．
```
bundle update jekyll
bundle install
bundle exec jekyll serve
```

なお，2回目以降は，最後の行 "bundle exec jekyll serve"を打つだけでOKです．   

**Watch Out!**   
Windowsの場合には，jekyll serve中にローカルサイトのコードを変えても，自動的には反映されない場合があります ([Auto Regenerationについて](https://jekyllrb.com/docs/installation/windows/#auto-regeneration))．※私の手元ではVS codeで保存すると，自動で更新されています．
{: .notice--info}  