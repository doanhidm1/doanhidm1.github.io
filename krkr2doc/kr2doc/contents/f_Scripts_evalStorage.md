# Scripts.evalStorage

機能/意味
:   ストレージ上の式の評価

タイプ
:   [Scriptsクラス](f_Scripts)のメソッド

構文
:   evalStorage(storage)

引数
:   |  |  |
    | --- | --- |
    | storage | 評価するストレージを指定します。 |

戻り値
:   式を評価した結果が戻ります。

説明
:   指定されたストレージを読み込み、その内容を TJS2 式として評価します。
    　スクリプトを実行中に発生した例外はこのメソッド内では捕捉されませんので、このメソッドの
    呼び出し側で捕捉することができます。

参照
:   [Scripts.execStorage](f_Scripts_execStorage)