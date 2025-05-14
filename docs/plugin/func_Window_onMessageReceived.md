# Window.onMessageReceived

機能/意味
:   イベント：メッセージ受信。

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   onMessageReceived(key, message)

引数
:   |  |  |
    | --- | --- |
    | key | 識別キー(文字列:256文字までなので注意) |
    | message | メッセージ(文字列) |

戻り値
:   なし (void)

説明
:   ほかの吉里吉里、あるいは外部アプリから WM\_COPYDATA メッセージを受信したときに呼び出されます
    呼び出し元はこれの呼び出しが終了するまでロックされてしまうため、
    速やかに処理を終了するようにしてください。