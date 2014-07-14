##これは何？
[Gaucheのオンラインドキュメント](http://practical-scheme.net/gauche/memo-j.html)をオフライン化し、[CHMファイル](http://ja.wikipedia.org/wiki/Microsoft_Compiled_HTML_Help)にしたものです。
主にWindowsユーザの利用を想定していますが、Linux、Macでも適当なブラウザがあれば見れるのかもしれません。

##使い方
リポジトリの中にある[Gaucheリファレンスマニュアル.chm]([https://github.com/aki426/GaucheOfflineHelp/blob/master/Gauche%E3%83%AA%E3%83%95%E3%82%A1%E3%83%AC%E3%83%B3%E3%82%B9%E3%83%9E%E3%83%8B%E3%83%A5%E3%82%A2%E3%83%AB.chm?raw=true)をダウンロードして使ってください。「検索」から全文検索が可能です。

ネットワークの無いところにノートPCを持ち歩いてプログラミングするような時に重宝すると思います。

##どうやって作ったの？
0. FirefoxのScrapbookを使って[日本語ドキュメント](http://practical-scheme.net/gauche/man/gauche-refj.html)以下をすべてダウンロード
1. 文字コードをShift-JISに変換
2. htmlファイル内の文字コード宣言部分をUTF-8からShift-JISに置換
3. titleの「Gauche ユーザリファレンス: 」を削除（CHMファイルにしたときの検索結果表示が煩わしいため）
4. [hhhlp](http://hp.vector.co.jp/authors/VA035931/hhhlp.html)を使ってhhpファイルを生成
5. [Microsoft HTML Help Downloads](http://msdn.microsoft.com/ja-jp/library/windows/desktop/ms669985%28v=vs.85%29.aspx)を使ってCHMファイルにコンパイル

コンパイル前のhtmlファイル、hhpファイルもリポジトリに一緒に入れておきます。

##ライセンス
元のリファレンスマニュアルと同様、修正BSDライセンスです。というかそもそも私に著作権が無いものなので、再配布にあたって明言が必要なのかどうかわかりませんが……。
