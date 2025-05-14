# Scripts.getTraceString

機能/意味
:   呼び出し履歴の取得

タイプ
:   [Scriptsクラス](f_Scripts)のメソッド

構文
:   getTraceString(limit=0)

引数
:   |  |  |
    | --- | --- |
    | limit | 履歴を取得する最大呼び出し深さを指定します。この引数を省略するか 0 を指定すると、取得できる限りの履歴を取得します。 |

戻り値
:   呼び出し履歴を文字列化した物

説明
:   メソッドの呼び出し履歴を文字列として取得します。このメソッドが呼ばれた時点での履歴を取得することができます。
    　このメソッドを使用するには、コマンドラインオプションで -debug (デバッグモード) が有効になっていなければなりません。デバッグモードが無効の場合はこのメソッドは空文字列を返します。
    　返される文字列はたとえば 'messagelayer.tjs(1561)[(function) addButton] <-- mainwindow.tjs(4463)[(function expression) (anonymous)] <-- conductor.tjs(427)[(function) onTag] <-- conductor.tjs(95)[(function) timerCallback]' のような物です。