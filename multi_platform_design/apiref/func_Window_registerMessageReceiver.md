# Window.registerMessageReceiver

機能/意味
:   [Windows+]メッセージ受信関数の登録/登録削除

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   registerMessageReceiver(mode, func, userdata)

引数
:   |  |  |
    | --- | --- |
    | mode | 登録するか、登録削除するかどうかを指定します。  wrmRegister を指定すると登録になります。  wrmUnregister を指定すると登録削除になります。  wrm で始まる定数は tp\_stub.h に定義されています。 |
    | func | メッセージ受信関数を指定します。  メッセージ受信関数は bool *\_stdcall func(void \*userdata, tTVPWindowMessage \*Message) の形式である必要があり、このメソッドに渡す際にその関数ポインタを整数型にキャストして渡す必要があります。  構造体 tTVPWindowMessage は tp*stub.h に定義されています。  この関数が true を返すと吉里吉里本体側はそのウィンドウメッセージに関知しなくなります。 |
    | userdata | func 引数で指定された受信関数の userdata 引数に渡すためのデータポインタを指定します。  このメソッドに渡す際にはそのポインタを整数型にキャストして渡す必要があります。  この引数は mode 引数が wrmRegister でないときは無視されます。 |

戻り値
:   なし (void)

説明
:   このメソッドは C++ 等で記述されたプラグインから利用されることを想定しているメソッドです。
    TJS2からは正常に利用できません。
    このメソッドでは、このウィンドウを通過するメッセージをトラップするためのメッセージ受信関数を登録することができます。
    メッセージ受信関数では通常のウィンドウメッセージの他、TVP*WM*DETACH と TVP*WM*ATTACH という２つの重要なメッセージもトラップすることができ、ウィンドウが再構築や破棄されるタイミングにおいて、子ウィンドウを取り外すというような用途に使用できます。
    吉里吉里ソース配布パッケージ中の src/plugins/win32/wmrdump に簡単な使用法の説明があります。

参照
:   [Window.HWND](prop_Window_HWND)