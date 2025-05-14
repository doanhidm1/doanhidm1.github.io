# Timer.Timer

機能/意味
:   Timer オブジェクトの構築

タイプ
:   [Timerクラス](f_Timer)のコンストラクタ

構文
:   Timer(owner, actionname="action")

引数
:   |  |  |
    | --- | --- |
    | owner | イベントの発生先を指定します。 |
    | actionname | owner で指定したイベントの発生先オブジェクトで、イベントを受け取るメソッド名を 指定します。空文字列を指定すると owner はメソッドとみなされ、イベントの周期ごとに owner が直接呼ばれます。 |

戻り値
:   なし (void)

説明
:   Timer クラスのオブジェクトを構築します。
    　初期状態では interval プロパティは 1000、enabled プロパティは偽になっています。