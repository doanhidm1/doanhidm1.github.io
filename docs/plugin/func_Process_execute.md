# Process.execute

機能/意味
:   バックグラウンドでの外部プログラムの実行

タイプ
:   [Processクラス](class_Process)のメソッド

構文
:   execute(target, param, folder)

引数
:   |  |  |
    | --- | --- |
    | target | プログラム |
    | param | 引数 |
    | folder | 実行時フォルダ(未指定時はカレントフォルダ) |

戻り値
:   起動成功時は true

説明
:   処理がおわったら onExecuted イベントが発生します。