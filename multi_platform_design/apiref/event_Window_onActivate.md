# Window.onActivate

機能/意味
:   ウィンドウがアクティブになったとき

タイプ
:   [Windowクラス](class_Window)のイベント

構文
:   onActivate()

引数

戻り値
:   なし (void)

説明
:   ウィンドウがアクティブになったときに呼び出されるイベント関数を表します。
    このイベントは、ウィンドウが既にアクティブの場合にも発生する可能性があるので注意してください (完全に onActivate → onDeactivate → onActivate → …… の順に発生する保証がない )。

参照
:   [Window.onDeactivate](event_Window_onDeactivate)
    [System.onActivate](prop_System_onActivate)
    [System.onDeactivate](prop_System_onDeactivate)