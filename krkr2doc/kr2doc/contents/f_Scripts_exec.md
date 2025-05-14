# Scripts.exec

機能/意味
:   スクリプトの実行

タイプ
:   [Scriptsクラス](f_Scripts)のメソッド

構文
:   exec(script)

引数
:   |  |  |
    | --- | --- |
    | script | 実行するスクリプトを文字列で指定します。 |

戻り値
:   スクリプトを実行した結果が戻ります。

説明
:   script で指定された文字列を TJS2 スクリプトとして実行します。
    　スクリプトを実行中に発生した例外はこのメソッド内では捕捉されませんので、このメソッドの
    呼び出し側で捕捉することができます。

参照
:   [Scripts.execStorage](f_Scripts_execStorage)
    [Scripts.eval](f_Scripts_eval)