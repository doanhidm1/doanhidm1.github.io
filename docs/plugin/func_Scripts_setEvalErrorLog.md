# Scripts.setEvalErrorLog

機能/意味
:   Scripts.evalのエラーログ出力抑制

タイプ
:   [Scriptsクラス](class_Scripts)のメソッド

構文
:   setEvalErrorLog(enabled)

引数
:   |  |  |
    | --- | --- |
    | enabled | 出力許可 |

戻り値
:   元の値

説明
:   enabled に false を設定すると Scripts.eval の評価処理を
    TVPExecuteExpression 経由で行うようになり，例外発生時にログが出力されない
    吉里吉里のバージョンアップに伴い仕様が変わる可能性があるので注意のこと