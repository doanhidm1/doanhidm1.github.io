# AsyncTrigger.trigger

機能/意味
:   トリガを引く

タイプ
:   [AsyncTriggerクラス](class_AsyncTrigger)のメソッド

構文
:   trigger()

引数

戻り値
:   なし (void)

説明
:   イベントを発生させます。
    このメソッドを呼んだ後、吉里吉里本体に制御が戻り、吉里吉里本体がたまった非同期イベントを配信する段階になると AsyncTrigger.onFire イベントが発生します。