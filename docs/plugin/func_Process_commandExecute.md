# Process.commandExecute

機能/意味
:   コンソール出力取得つきコマンドラインプログラムの実行

タイプ
:   [Processクラス](class_Process)のメソッド

構文
:   commandExecute(target, param, folder)

引数
:   |  |  |
    | --- | --- |
    | target | プログラム |
    | param | 引数 |
    | folder | 実行時フォルダ(未指定時はカレントフォルダ) |

戻り値
:   起動成功時は true

説明
:   コンソールの行単位出力で onOutput イベントが発生します。
    処理がおわったら onExecuted イベントが発生します。