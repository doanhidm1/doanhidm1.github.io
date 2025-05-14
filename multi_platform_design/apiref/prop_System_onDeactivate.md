# System.onDeactivate

機能/意味
:   アプリケーションが非アクティブになったとき

タイプ
:   [Systemクラス](class_System)のプロパティ

説明
:   アプリケーションが非アクティブになったときに呼び出されるイベント関数を表します。
    null を指定すると関数は呼び出されません。
    通常のイベントハンドラと異なり、このイベントを受け取りたい場合は、呼び出したい関数をこのプロパティに設定してください。
    Window.onDeactivate は、同じアプリケーション内のそれぞれのウィンドウが非アクティブになったときに発生しますが、このイベントは、メインウィンドウが非アクティブになった場合に発生します。
    このイベントは、メインウィンドウが既に非アクティブの場合にも発生する可能性があるので注意してください (完全に onActivate → onDeactivate → onActivate → …… の順に発生する保証がない )。

参照
:   [System.onActivate](prop_System_onActivate)
    [Window.onActivate](event_Window_onActivate)
    [Window.onDeactivate](event_Window_onDeactivate)