# Layer.onPaint

機能/意味
:   描画されるとき

タイプ
:   [Layerクラス](class_Layer)のイベント

構文
:   onPaint()

引数

戻り値
:   なし (void)

説明
:   レイヤが実際にウィンドウに描画される直前に呼ばれます。
    このイベントは Layer.callOnPaint プロパティが真の時のみに呼ばれ、Layer.callOnPaint はこのイベントが実行し終わった後自動的に偽に設定されます。

参照
:   [Layer.update](func_Layer_update)