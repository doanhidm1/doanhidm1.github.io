# Window.enableTouch

機能/意味
:   タッチイベント有効/無効

タイプ
:   [Windowクラス](class_Window)のプロパティ

説明
:   タッチイベントが有効かどうかを表します。
    値を設定することもできます。
    真を指定するとWindow.onTouchDown等のイベントが有効になり、タッチ操作ではWindow.onMouseDownなどが発生しなくなります。
    タッチデバイスがありマルチタッチが有効な環境では、デフォルトが true になります。
    Androidでは常にタッチ有効です。