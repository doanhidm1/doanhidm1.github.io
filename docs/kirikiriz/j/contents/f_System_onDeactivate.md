# System.onDeactivate

機能/意味
:   アプリケーションが非アクティブになったとき

タイプ
:   [Systemクラス](f_System)のプロパティ (読み書き可能)

説明
:   アプリケーションが非アクティブになったときに呼び出されるイベント関数を表します。
    　null を指定すると関数は呼び出されません。
    　通常のイベントハンドラと異なり、このイベントを受け取りたい場合は、呼び出したい関数をこのプロパティに設定してください。
    　[Window.onDeactivate](f_Window_onDeactivate) は、同じアプリケーション内のそれぞれのウィンドウが非アクティブになったときに発生しますが、このイベントは、メインウィンドウが非アクティブになった場合に発生します。
    　このイベントは、メインウィンドウが既に非アクティブの場合にも発生する可能性があるので注意してください (完全に onActivate → onDeactivate → onActivate → …… の順に発生する保証がない )。

参照
:   [System.onActivate](f_System_onActivate)
    [Window.onActivate](f_Window_onActivate)
    [Window.onDeactivate](f_Window_onDeactivate)