# AsyncTrigger.AsyncTrigger

機能/意味
:   AsyncTriger オブジェクトの構築

タイプ
:   [AsyncTriggerクラス](f_AsyncTrigger)のコンストラクタ

構文
:   AsyncTrigger(owner, actionname="action")

引数
:   |  |  |
    | --- | --- |
    | owner | イベントの発生先を指定します。 |
    | actionname | owner で指定したイベントの発生先オブジェクトで、イベントを受け取るメソッド名を 指定します。空文字列を指定すると owner はメソッドとみなされ、イベントの発生ごとに owner が直接呼ばれます。 |

戻り値
:   なし (void)

説明
:   AsyncTrigger クラスのオブジェクトを構築します。