# Window.onDeactivate

機能/意味
:   ウィンドウが非アクティブになったとき

タイプ
:   [Windowクラス](class_Window)のイベント

構文
:   onDeactivate()

引数

戻り値
:   なし (void)

説明
:   ウィンドウが非アクティブになったときに呼び出されるイベント関数を表します。
    このイベントは、ウィンドウが既に非アクティブの場合にも発生する可能性があるので注意してください (完全に onActivate → onDeactivate → onActivate → …… の順に発生する保証がない )。
    Androidでは、非アクティブになった後、復帰せずプロセスが終了させられる場合もあるので注意してください。

参照
:   [Window.onActivate](event_Window_onActivate)
    [System.onActivate](prop_System_onActivate)
    [System.onDeactivate](prop_System_onDeactivate)