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

コンパイル前のhtmlファイル、hhpファイルもリポジトリに一緒に入れてあります。必要に応じて使ってください。

##ライセンス
元のリファレンスマニュアルと同様、修正BSDライセンスです。日本語のライセンス文は[SourceForgeの翻訳文など](http://sourceforge.jp/projects/opensource/wiki/licenses%2Fnew_BSD_license)を参考にしてください。
また、本リファレンスマニュアルの著作権は私ではなく、原著作者の川合史郎氏にあります。

  Copyright (c) 2000-2014  Shiro Kawai  <shiro@acm.org>

  Redistribution and use in source and binary forms, with or without
  modification, are permitted provided that the following conditions
  are met:

   1. Redistributions of source code must retain the above copyright
      notice, this list of conditions and the following disclaimer.

   2. Redistributions in binary form must reproduce the above copyright
      notice, this list of conditions and the following disclaimer in the
      documentation and/or other materials provided with the distribution.

   3. Neither the name of the authors nor the names of its contributors
      may be used to endorse or promote products derived from this
      software without specific prior written permission.

  THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
  "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
  LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
  A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
  OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
  SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED
  TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR
  PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF
  LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING
  NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
  SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
