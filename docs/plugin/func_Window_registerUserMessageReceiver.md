# Window.registerUserMessageReceiver

機能/意味
:   ユーザ定義のメッセージハンドラを登録します。

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   registerUserMessageReceiver(mode, msg, proc, userdata)

引数
:   |  |  |
    | --- | --- |
    | mode | wrmRegister:登録 wrmUnRegister:解除 |
    | msg | 数値:メッセージ番号 文字列:RegisterWindowMessage して値を決定 |
    | proc | 呼び出しファンクション |
    | userdata | ユーザデータパラメータ |

戻り値
:   登録されたメッセージ番号を返す

説明
:   ※TJS2 から関数を登録した場合（typeof proc == Object の場合)
    function receiver(userdata, wparam, lparam)
    の形式のファンクションであるとみなされます。
    この時、userdata は渡した値そのままを、
    wparam, lparam は元メッセージのデータから整数にキャストした値を渡します。

    ※TJS2 から文字列を登録した場合 (typeof proc == String の場合)
    該当オブジェクトの指定された文字列の関数を function name(userdata, wparam, lparam)
    の引数で呼びだします

    ※プラグイン側から関数を登録する場合 (typeof proc == Integer の場合)
    static bool \_\_stdcall receiver(iTJSDispatch2 \*winobj, void \*userdata, tTVPWindowMessage \*Message)
    であるとみなされます。設定時は整数にキャストしてください。
    winobj は該当するウインドウのオブジェクトです
    userdata は整数にキャストした値でひきわたされます。