# Layer.moveBefore

機能/意味
:   指定レイヤの手前に移動

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   moveBefore(layer)

引数
:   |  |  |
    | --- | --- |
    | layer | ここで指定したレイヤの手前に移動します。  兄弟レイヤ ( 同じ親を持つレイヤ ) のみを指定できます。 |

戻り値
:   なし (void)

説明
:   重ね合わせ順において、指定されたレイヤの手前に移動します。
    このメソッドは Layer.absoluteOrderMode プロパティを false に設定します。