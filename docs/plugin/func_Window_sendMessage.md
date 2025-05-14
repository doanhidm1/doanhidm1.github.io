# Window.sendMessage

機能/意味
:   メッセージの送信を行います。

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   sendMessage(key, message)

引数
:   |  |  |
    | --- | --- |
    | key | 識別キー(文字列:256文字までなので注意) |
    | message | メッセージ(文字列) |

戻り値
:   なし (void)

説明
:   起動している吉里吉里すべてに WM\_COPYDATA メッセージを送信します。
    識別キーとメッセージの意味はそれぞれのアプリで適当に定めてください。