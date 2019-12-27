---
title: WebStorm上でjQueryのAPIドキュメントを表示する
author: azu
layout: post
permalink: /2011/0419/res2566/
SBM_count:
  - '00014<>1355366373<>12<>0<>2<>0<>0'
dsq_thread_id:
  - 300970604
categories:
  - javascript
  - software
tags:
  - API
  - jQuery
  - WebStorm
---
[WebStorm & PhpStorm Blog » Blog Archive » jQuery API documentation at your fingertips][1]で紹介されていますが、WebStorm上でjQueryのオンラインヘルプをローカルにダウンロードしたものを表示できるようになっていました。(WebStorm/PHPStrom 2.1 以降が対象)

まずは[JavaScript libraries][2]の設定(Settings> JavaScript Library)で、Addボタンを押してローカルにおいたjQuery.jsをFileに指定します。   
Documentation URLsのSpecifyボタンを押して、[http://api.jquery.com][3] を指定してからダウンロードボタンを押すとローカルにjQueryのドキュメントがダウンロードされます。(実際にダウンロードされるのは[Raw XML API Dump][4]ですが[http://api.jquery.com][3]の方を指定する)

<a class="thickbox" href="https://efcl.info/wp-content/uploads/2011/04/2011-04-19-ss1.png"><img style="background-image: none; border-right-width: 0px; padding-left: 0px; padding-right: 0px; display: inline; border-top-width: 0px; border-bottom-width: 0px; border-left-width: 0px; padding-top: 0px" title="2011-04-19-ss1" border="0" alt="2011-04-19-ss1" src="https://efcl.info/wp-content/uploads/2011/04/2011-04-19-ss1_thumb.png" width="240" height="196" /></a>

これでライブラリの追加は終わったので、次は実際にjQueryを使うプロジェクトを開きます。(プロジェクトを開いていない状態で設定すれば常に適応されるグローバルとして設定できると思う、その辺は[WebStormのコード補完に新しく候補を追加する方法 | Web scratch][5]と同じかな）   
また同じく設定に行き、JavaScript Library>Scopeを見るとそのプロジェクトで適応されているライブラリが分かると思います。jQuery(Addボタン追加したライブラリ名の事）にチェックを入れれば準備は終わりです。(逆をいれば、プロジェクト毎に補完候補に現れるライブラリを指定できるようになっている)

[<img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; display: inline; border-top: 0px; border-right: 0px; padding-top: 0px" title="2011-04-19-ss2" border="0" alt="2011-04-19-ss2" src="https://efcl.info/wp-content/uploads/2011/04/2011-04-19-ss2_thumb.png" width="240" height="122" />][6]

後はjQueryのメソッドにカーソルを合わせて、Quick Documentation Look-up(デフォルトCtrl+Q)をすれば、APIドキュメントがパネルに表示されます。

<a class="thickbox" href="https://efcl.info/wp-content/uploads/2011/04/2011-04-19-ss3.png"><img style="background-image: none; border-right-width: 0px; padding-left: 0px; padding-right: 0px; display: inline; border-top-width: 0px; border-bottom-width: 0px; border-left-width: 0px; padding-top: 0px" title="2011-04-19-ss3" border="0" alt="2011-04-19-ss3" src="https://efcl.info/wp-content/uploads/2011/04/2011-04-19-ss3_thumb.png" width="240" height="158" /></a>

Shift+F1か、ポップアップしたドキュメントの矢印ボタンからドキュメントのWebページのジャンプもできる。

<a class="thickbox" href="https://efcl.info/wp-content/uploads/2011/04/2011-04-19-ss4.png"><img style="background-image: none; border-right-width: 0px; padding-left: 0px; padding-right: 0px; display: inline; border-top-width: 0px; border-bottom-width: 0px; border-left-width: 0px; padding-top: 0px" title="2011-04-19-ss4" border="0" alt="2011-04-19-ss4" src="https://efcl.info/wp-content/uploads/2011/04/2011-04-19-ss4_thumb.png" width="240" height="87" /></a>

今回はjQueryだけみたいですが、ちゃんとオフライン向けのドキュメントを発行してくれるライブラリなら対応されるかも知れません。ドキュメントのヘルプページへのジャンプ機能はjQuery以外にも対応しているライブラリがあります。   
[WebStorm & PhpStorm Blog » Blog Archive » External API Docs Support for Popular JavaScript Frameworks][7]

jQueryの補完もちゃんとできるし、APIドキュメントもすぐに見られるようになったのでjQuery使うのがかなり楽になったと思います。後、自分で追加する[JavaScript libraries][2]を設定できるので、ライブラリバージョン別に分けるといった事もできたりすると思います。

参考

*   [WebStorm & PhpStorm Blog » Blog Archive » External API Docs Support for Popular JavaScript Frameworks][7] 
*   [WebStormのコード補完に新しく候補を追加する方法 | Web scratch][5]

おまけ

[<img title="WS_SpringOffer_2" alt="" src="https://efcl.info/wp-content/uploads/2011/04/WS_SpringOffer_2.jpg" width="210" height="180" />][8]

WebStormが今春のキャンペーンがまだ続いているので半額で購入できるみたいです。   
JetBrains公式の[NodeJS][9]プラグイン(Node.jsもそのうち公式対応されると思う)の公開が始まったりして、まだ進化のスピードは落ちてない印象なので、安いうちに買っておくのもいいかと思います。

**WebStorm & PhpStorm Blog » Blog Archive » 50% OFF personal WebStorm licensesi**
:   <https://blogs.jetbrains.com/webide/2011/04/50-off-on-personal-webstorm-licenses/>

 [1]: https://blogs.jetbrains.com/webide/2011/04/jquery-offline-doc/
 [2]: https://blogs.jetbrains.com/webide/2010/11/working-with-javascript-libraries-in-phpstorm-webstorm/
 [3]: http://api.jquery.com "http://api.jquery.com"
 [4]: http://api.jquery.com/api/
 [5]: https://efcl.info/2010/1203/res2152/
 [6]: https://efcl.info/wp-content/uploads/2011/04/2011-04-19-ss2.png
 [7]: https://blogs.jetbrains.com/webide/2011/01/external-api-docs-support-for-popular-javascript-frameworks/
 [8]: http://www.jetbrains.com/webstorm/buy/
 [9]: http://plugins.jetbrains.com/plugin/?webide&id=6098
