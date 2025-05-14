# AsyncTrigger.mode

機能/意味
:   モード

タイプ
:   [AsyncTriggerクラス](class_AsyncTrigger)のプロパティ

説明
:   動作のモードを表します。
    値を設定することもできます。
    以下の値のいずれかを指定します。
    atmNormal : 通常のイベント配信の段階で発砲されます。
    atmExclusive : 他の非同期イベントよりも優先されて発砲されます
    atmAtIdle : アイドル状態 ( 他に配信するイベントが無くなったとき ) に発砲されます。
    同時にトリガを引いたときに発砲される順序は atmExclusive, atmNormal, atmIdle の順になります。
    同じモードのトリガが複数引かれている場合は、トリガが引かれた順に発砲します。

参照
:   [Timer.mode](prop_Timer_mode)