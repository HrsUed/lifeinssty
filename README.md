![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/HrsUed/lifeinssty)

# 概要
このパッケージは生命保険数学に必要なアクチュアリー記号を出力するためのコマンドを提供しています。
基本的にはLaTeX 2e標準のパッケージやamsmath等のパッケージですべて補える記号ですが、入力の省略と同時に、記号の意味を著者が一目で判断できるようにしておく必要があります。
したがって、ここでアクチュアリー記号を与えるコマンドを定義する意義は大いにあると考えています。

なお、このパッケージで与えるコマンドはすべて数式モード内で入力してください。
また、出力例ではわざとおかしな出力を与えている箇所がありますが、それは注意のためのものであって、ミスではありません。

さらに、このパッケージが与えるコマンドの定義は、マクロ初心者の著者がスパイラル方式で作成したものばかりです。
したがって、その定義はスマートでもエレガントでもない、泥臭い定義ばかりです。
その点が気になる方は、適宜プルリクエストやフォークして変更して頂いても構いません。

# 使い方
lifeins.dtx, lifeins.insファイルからlifeins.styファイルとドキュメントを作成する手順です。

1. リポジトリをzipファイルダウンロードします。
2. ダウンロードしたzipファイルを解凍し、適当な場所にファイルlifeins.ins、lifeins.dtxを保存する。
3. コマンドプロンプト/ターミナルでこれらのファイルがある場所まで移動。
4. `platex lifeins.ins`を実行。スタイルファイルlifeins.styが生成される。
5. `platex lifeins.dtx`を実行。ドキュメントlifeins.dviが生成される。その際、処理が途中で止まっても、構わずにEnterを押してください。
6. `"Transcript written on lifeins.log."`と表示されれば、正常に終了です。
7. 正常に終了すれば、スタイルファイルlifeins.sty、ドキュメントlifeins.dviが生成されます。
8. パッケージを使用したいtexファイルのブリアンブルでlifeins.styを読み込みます。
9. コマンドの詳細はドキュメントをご覧ください。

# 変更履歴
- 2012/01/15 v3.1
  - `\balign`の位置を調整
- 2011/02/08 v3.0
  - `\overtortoise`を追加。
  - `\alignsep`にて保険者と順序の間のスペースを調整できるようにした。
  - `\order`とそれに関連するコマンドを追加。それに伴い、`\aa`, `\ba`を廃止。
