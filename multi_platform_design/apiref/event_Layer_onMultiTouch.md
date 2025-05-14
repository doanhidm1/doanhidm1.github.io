# Layer.onMultiTouch

機能/意味
:   マルチタッチ状態が変化した

タイプ
:   [Layerクラス](class_Layer)のイベント

構文
:   onMultiTouch()

引数

戻り値
:   なし (void)

説明
:   マルチタッチ状態が開始されたり、移動したり、離れた時に発生します。
    座標情報は Window.touchPointCount プロパティと Window.getTouchPoint メソッドで取得できます。
    このイベントが発生するのは、フォーカスのあるレイヤです。

参照
:   [Window.getTouchPoint](func_Window_getTouchPoint)
    [Window.touchPointCount](prop_Window_touchPointCount)