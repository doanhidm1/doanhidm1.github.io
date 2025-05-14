# Scripts.exec

機能/意味
:   スクリプトの実行

タイプ
:   [Scriptsクラス](f_Scripts)のメソッド

構文
:   exec(script, name='', linesof=0, context=global)

引数
:   |  |  |
    | --- | --- |
    | script | 実行するスクリプトを文字列で指定します。 |
    | name | エラーメッセージ用ファイル名の指定 |
    | linesof | エラーメッセージ用行番号の指定 |
    | context | 実行コンテキストを指定します。 |

戻り値
:   スクリプトを実行した結果が戻ります。

説明
:   script で指定された文字列を TJS2 スクリプトとして実行します。
    　スクリプトを実行中に発生した例外はこのメソッド内では捕捉されませんので、このメソッドの
    呼び出し側で捕捉することができます。

参照
:   [Scripts.execStorage](f_Scripts_execStorage)
    [Scripts.eval](f_Scripts_eval)