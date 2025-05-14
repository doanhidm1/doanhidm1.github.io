# Layer.absolute

機能/意味
:   絶対位置

タイプ
:   [Layerクラス](class_Layer)のプロパティ

説明
:   同じ親を持つ兄弟レイヤ間での重ね合わせ順序を表します。
    値が小さいほど奥に表示されます。
    Layer.order プロパティと違い、同じ兄弟間で値は連続している必要はありません。
    値を設定すると兄弟レイヤ間での順位を変えることができます。
    値を設定すると親レイヤの Layer.absoluteOrderMode プロパティが真に設定されます。

参照
:   [Layer.order](prop_Layer_order)
    [Layer.absoluteOrderMode](prop_Layer_absoluteOrderMode)
    [Layer.bringToBack](func_Layer_bringToBack)
    [Layer.bringToFront](func_Layer_bringToFront)