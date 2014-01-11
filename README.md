polycal パッケージ
==================

### 主機能
polynom パッケージに微分・積分演算を追加する。

  * \polydiff\cs{var}{poly}

  多項式 poly を変数 var で微分した結果を
  コントロールシーケンス \cs  にセーブする。

  * \polyint\cs{var}{poly}

  多項式 poly を変数 var で0から積分した結果を
  \cs にセーブする。

### その他

  * \polydefine\cs{poly}

  多項式 poly を内部表現に変換し \cs にセーブする。

以下いくつかの代入演算。polynom パッケージの機能で
割り算が出来るのだから、本来なら代入結果は1次式による
剰余で計算できるはずである。 だが多変数多項式の割り算
は変数の優先順位を指定する必要がある。このあたりは
polynomパッケージは未完成のようで、正しく機能しない。
それで代入計算を直接実行するコマンドを作成した。

  * \polysubstnum\cs{var}{num}{poly}

  多項式  poly  の変数  var  に有理数  num  を代入し、
  結果を \cs にセーブする。

  * \polysubst\cs{var}{poly1}{poly2}

  多項式  poly2  の変数  var  に多項式  poly1  を代入し、
  結果を \cs にセーブする。

  * \polysubstsqrt\cs{var}{num}{poly}

  1変数多項式  poly  の変数  var  に有理数  num  の正の
  平方根を代入し、結果を \cs にセーブする。

いずれも計算効率は全く考慮していないので、次数が高くなるととても遅い。

### 更新履歴

  * Version 0.01 2014/01/09
    - 初公開。

  * Version 0.01a 2014/01/11
    - \pld@IfMonomL@ (in polynom.sty) の bug fix.
    - demo の書き換え。

  * Version 0.01b 2014/01/12
    - Minor fix.
    - dtx, ins と manual の作成。


------------
SATO Tatsuya
