# AsyncTrigger.cached

機能/意味
:   イベントをキャッシュするかどうか

タイプ
:   [AsyncTriggerクラス](class_AsyncTrigger)のプロパティ

説明
:   イベントをキャッシュするかどうかを表します。
    値を設定することもできます。
    真を指定すると、発砲までに何度 AsyncTrigger.trigger メソッドを呼んでも発砲は１回だけとなります。
    偽を指定すると、発砲までに呼んだ回数分、発砲されます。