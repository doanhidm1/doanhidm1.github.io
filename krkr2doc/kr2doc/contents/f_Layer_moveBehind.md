# Layer.moveBehind

機能/意味
:   指定レイヤの奥に移動

タイプ
:   [Layerクラス](f_Layer)のメソッド

構文
:   moveBehind(layer)

引数
:   |  |  |
    | --- | --- |
    | layer | ここで指定したレイヤの奥に移動します。  　兄弟レイヤ ( 同じ親を持つレイヤ ) のみを指定できます。 |

戻り値
:   なし (void)

説明
:   重ね合わせ順において、指定されたレイヤの奥に移動します。
    　このメソッドは [Layer.absoluteOrderMode](f_Layer_absoluteOrderMode) プロパティを false に設定します。