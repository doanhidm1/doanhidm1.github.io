# Scripts.execStorage

機能/意味
:   ストレージ上のスクリプトの実行

タイプ
:   [Scriptsクラス](f_Scripts)のメソッド

構文
:   execStorage(storage)

引数
:   |  |  |
    | --- | --- |
    | storage | 実行するストレージを指定します。 |

戻り値
:   スクリプトを実行した結果が戻ります。

説明
:   指定されたストレージを読み込み、その内容を TJS2 スクリプトとして実行します。
    　スクリプトを実行中に発生した例外はこのメソッド内では捕捉されませんので、このメソッドの
    呼び出し側で捕捉することができます。

参照
:   [Scripts.evalStorage](f_Scripts_evalStorage)