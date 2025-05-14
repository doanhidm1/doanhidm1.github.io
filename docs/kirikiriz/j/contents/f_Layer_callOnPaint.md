# Layer.callOnPaint

機能/意味
:   onPaint イベントを呼ぶかどうか

タイプ
:   [Layerクラス](f_Layer)のプロパティ (読み書き可能)

説明
:   [Layer.onPaint](f_Layer_onPaint) イベントを呼ぶかどうかを表します。値を設定することもできます。
    　真を指定すると、次回の画面への描画の直前に onPaint イベントを呼ぶようになります。onPaint イベント
    が処理し終わるとこのプロパティは自動的に偽に戻されます。
    　偽が指定されている状態では onPaint イベントは発生しません。
    　[Layer.update](f_Layer_update) メソッドはこのプロパティを真に設定します。