# Scripts.eval

機能/意味
:   式の評価

タイプ
:   [Scriptsクラス](f_Scripts)のメソッド

構文
:   eval(expression)

引数
:   |  |  |
    | --- | --- |
    | expression | 実行する式を文字列で指定します。 |

戻り値
:   式を評価した結果が戻ります。

説明
:   expression で指定された文字列を TJS2 式として実行します。
    　スクリプトを実行中に発生した例外はこのメソッド内では捕捉されませんので、このメソッドの
    呼び出し側で捕捉することができます。

参照
:   [Scripts.execStorage](f_Scripts_execStorage)
    [Scripts.exec](f_Scripts_exec)