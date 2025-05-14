# Window.onDeactivate

機能/意味
:   ウィンドウが非アクティブになったとき

タイプ
:   [Windowクラス](f_Window)のイベント

構文
:   onDeactivate()

引数
:   なし

説明
:   ウィンドウが非アクティブになったときに呼び出されるイベント関数を表します。
    　このイベントは、ウィンドウが既に非アクティブの場合にも発生する可能性があるので注意してください (完全に onActivate → onDeactivate → onActivate → …… の順に発生する保証がない )。

参照
:   [Window.onActivate](f_Window_onActivate)
    [System.onActivate](f_System_onActivate)
    [System.onDeactivate](f_System_onDeactivate)