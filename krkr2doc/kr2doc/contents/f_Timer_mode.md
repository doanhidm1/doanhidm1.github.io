# Timer.mode

機能/意味
:   モード

タイプ
:   [Timerクラス](f_Timer)のプロパティ (読み書き可能)

説明
:   動作のモードを表します。値を設定することもできます。
    　以下の値のいずれかを指定します。
    atmNormal :  通常のイベント配信の優先度でイベントが配信されます。
    atmExclusive :  他の非同期イベントよりも優先されて配信されます
    atmAtIdle :  アイドル状態 ( 他に配信するイベントが無くなったとき ) に配信されます。

参照
:   [AsyncTrigger.mode](f_AsyncTrigger_mode)