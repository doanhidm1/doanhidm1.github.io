# Layer.flipUD

機能/意味
:   上下反転

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   flipUD()

引数

戻り値
:   なし (void)

説明
:   画像の上下反転を行います。
    このメソッドは、Layer.setClip メソッドなどによる描画クリップ矩形の影響を受けません ( 常にレイヤ画像全体が反転します )。
    また、Layer.face プロパティやLayer.holdAlpha プロパティの影響も受けません。