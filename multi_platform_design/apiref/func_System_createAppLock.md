# System.createAppLock

機能/意味
:   [Windows+]二重起動のチェック

タイプ
:   [Systemクラス](class_System)のメソッド

構文
:   createAppLock(key)

引数
:   |  |  |
    | --- | --- |
    | key | チェックを行うためのキー文字列を指定します。同じキー文字列をほかの実行中の吉里吉里がこのメソッドに指定していた場合、false が戻ります。  キー文字列には基本的には TJS の変数の命名規則と同じ文字のみが使えると考えてください。  キー文字列は十分にユニークな物である必要があります。 |

戻り値
:   すでに同じキー文字列が指定された吉里吉里が実行中の場合は false、そうでなければ true が戻ります。

説明
:   他に同じキー文字列を指定された吉里吉里が実行中ならば false、そうでなければ true が戻ります。
    二重起動の防止に用います。