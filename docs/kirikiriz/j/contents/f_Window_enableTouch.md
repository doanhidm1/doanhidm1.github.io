# Window.enableTouch

機能/意味
:   タッチイベント有効/無効

タイプ
:   [Windowクラス](f_Window)のプロパティ (読み書き可能)

説明
:   タッチイベントが有効かどうかを表します。値を設定することもできます。
    　真を指定すると[Window.onTouchDown](f_Window_onTouchDown)等のイベントが有効になり、タッチ操作では[Window.onMouseDown](f_Window_onMouseDown)などが発生しなくなります。
    　タッチデバイスがありマルチタッチが有効な環境では、デフォルトが true になります。