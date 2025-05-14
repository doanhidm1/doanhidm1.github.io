# Window.onActivate

機能/意味
:   ウィンドウがアクティブになったとき

タイプ
:   [Windowクラス](f_Window)のイベント

構文
:   onActivate()

引数
:   なし

説明
:   ウィンドウがアクティブになったときに呼び出されるイベント関数を表します。
    　このイベントは、ウィンドウが既にアクティブの場合にも発生する可能性があるので注意してください (完全に onActivate → onDeactivate → onActivate → …… の順に発生する保証がない )。

参照
:   [Window.onDeactivate](f_Window_onDeactivate)
    [System.onActivate](f_System_onActivate)
    [System.onDeactivate](f_System_onDeactivate)