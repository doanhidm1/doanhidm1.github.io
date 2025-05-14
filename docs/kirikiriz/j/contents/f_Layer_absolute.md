# Layer.absolute

機能/意味
:   絶対位置

タイプ
:   [Layerクラス](f_Layer)のプロパティ (読み書き可能)

説明
:   同じ親を持つ兄弟レイヤ間での重ね合わせ順序を表します。値が小さいほど奥に表示されます。
    [Layer.order](f_Layer_order) プロパティと違い、同じ兄弟間で値は連続している必要はありません。
    　値を設定すると兄弟レイヤ間での順位を変えることができます。値を設定すると
    親レイヤの [Layer.absoluteOrderMode](f_Layer_absoluteOrderMode) プロパティが真に設定されます。

参照
:   [Layer.order](f_Layer_order)
    [Layer.absoluteOrderMode](f_Layer_absoluteOrderMode)
    [Layer.bringToBack](f_Layer_bringToBack)
    [Layer.bringToFront](f_Layer_bringToFront)