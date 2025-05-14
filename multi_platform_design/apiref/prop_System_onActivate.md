# System.onActivate

機能/意味
:   アプリケーションがアクティブになったとき

タイプ
:   [Systemクラス](class_System)のプロパティ

説明
:   アプリケーションがアクティブになったときに呼び出されるイベント関数を表します。
    null を指定すると関数は呼び出されません。
    通常のイベントハンドラと異なり、このイベントを受け取りたい場合は、呼び出したい関数をこのプロパティに設定してください。
    Window.onActivate は、同じアプリケーション内のそれぞれのウィンドウがアクティブになったときに発生しますが、このイベントは、メインウィンドウがアクティブになった場合に発生します。
    このイベントは、メインウィンドウが既にアクティブの場合にも発生する可能性があるので注意してください (完全に onActivate → onDeactivate → onActivate → …… の順に発生する保証がない )。

参照
:   [System.onDeactivate](prop_System_onDeactivate)
    [Window.onActivate](event_Window_onActivate)
    [Window.onDeactivate](event_Window_onDeactivate)