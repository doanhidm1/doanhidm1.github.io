# Layer.flipUD

機能/意味
:   上下反転

タイプ
:   [Layerクラス](f_Layer)のメソッド

構文
:   flipUD()

引数
:   なし

戻り値
:   なし (void)

説明
:   画像の上下反転を行います。
    　このメソッドは、[Layer.setClip](f_Layer_setClip) メソッドなどによる描画クリップ矩形の影響を受けません ( 常にレイヤ画像全体が反転します )。
    　また、[Layer.face](f_Layer_face) プロパティや[Layer.holdAlpha](f_Layer_holdAlpha) プロパティの影響も受けません。