# Layer.bringToBack

機能/意味
:   一番奥に移動

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   bringToBack()

引数

戻り値
:   なし (void)

説明
:   重ね合わせ順において、兄弟レイヤ ( 同じ親を持つレイヤ ) の中でもっとも奥に移動します。
    このメソッドを実行すると親レイヤの Layer.absoluteOrderMode プロパティが偽に設定されます。

参照
:   [Layer.order](prop_Layer_order)
    [Layer.absolute](prop_Layer_absolute)
    [Layer.absoluteOrderMode](prop_Layer_absoluteOrderMode)
    [Layer.bringToFront](func_Layer_bringToFront)