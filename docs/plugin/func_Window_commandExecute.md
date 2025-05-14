# Window.commandExecute

機能/意味
:   コンソール出力取得つきコマンドラインプログラムの実行

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   commandExecute(target, param)

引数
:   |  |  |
    | --- | --- |
    | target | プログラム |
    | param | 引数 |

戻り値
:   プロセスハンドル（失敗した場合は-1)。terminateProcess に渡すことができます。

説明
:   コンソールの行単位出力で onCommandLineOutput イベントが発生します。
    処理がおわったら onShellExecuted イベントが発生します。