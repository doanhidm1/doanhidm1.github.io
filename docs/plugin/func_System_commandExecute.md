# System.commandExecute

機能/意味
:   コンソール出力取得つきコマンドラインプログラムの実行

タイプ
:   [Systemクラス](class_System)のメソッド

構文
:   commandExecute(target, param, timeout)

引数
:   |  |  |
    | --- | --- |
    | target | プログラム |
    | param | 引数 |
    | timeout | タイムアウト時間(ms) |

戻り値
:   %[\nstatus: ok/error/timeoutのいずれかの文字列, \nstdout: コンソール出力文字列配列(改行で分離)\nexitcode: 終了コード(status=="ok"時のみ),\nmessage: エラーメッセージ(status!="ok"時のみ)\n];

説明
:   バックグラウンド処理はありません。実行対象のプログラムが終了するまで吉里吉里が停止します。