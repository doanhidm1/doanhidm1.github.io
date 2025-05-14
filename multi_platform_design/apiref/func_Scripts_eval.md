# Scripts.eval

機能/意味
:   式の評価

タイプ
:   [Scriptsクラス](class_Scripts)のメソッド

構文
:   eval(expression, name=, linesof=0, context)

引数
:   |  |  |
    | --- | --- |
    | expression | 実行する式を文字列で指定します。 |
    | name | エラーメッセージ用ファイル名の指定 |
    | linesof | エラーメッセージ用行番号の指定 |
    | context | 実行コンテキストを指定します。 |

戻り値
:   式を評価した結果が戻ります。

説明
:   expression で指定された文字列を TJS2 式として実行します。
    スクリプトを実行中に発生した例外はこのメソッド内では捕捉されませんので、このメソッドの呼び出し側で捕捉することができます。

参照
:   [Scripts.execStorage](func_Scripts_execStorage)
    [Scripts.exec](func_Scripts_exec)