# Window.shellExecute

機能/意味
:   バックグラウンドでの外部プログラムの実行

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   shellExecute(target, param)

引数
:   |  |  |
    | --- | --- |
    | target | プログラム |
    | param | 引数 |

戻り値
:   プロセスハンドル（失敗した場合は-1)。terminateProcess に渡すことができます。

説明
:   処理がおわったら onShellExecuted イベントが発生します。