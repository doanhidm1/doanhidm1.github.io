# Layer.holdAlpha

機能/意味
:   アルファチャンネルを保護するか

タイプ
:   [Layerクラス](f_Layer)のプロパティ (読み書き可能)

説明
:   描画においてアルファチャンネルを保護するかどうかを指定します。値を設定することもできます。
    　デフォルトでは偽です。
    　吉里吉里 2.23 beta 1 以前では、各描画メソッドに hda というパラメータがあり、それがこのプロパティと同じ動作をしていましたが、2.23 beta 2 よりプロパティとして分離されました。
    　いくつかの描画演算では、[Layer.face](f_Layer_face) プロパティが dfOpaque のとき、画像のアルファチャンネル(マスク画像)を保持するかどうかをこのプロパティで指定できます。多くのメソッドでは、このプロパティを偽にした方が高速な描画が可能です。[Layer.type](f_Layer_type) が ltAlpha でも ltAddAlpha でも無い場合は、画像のアルファチャンネルは使用されないので、このプロパティを偽に設定しても問題有りません。ただし、このプロパティが偽だとアルファチャンネルは破壊されます。

    　以下のメソッドはこのプロパティの影響を受けません。
    [Layer.loadImages](f_Layer_loadImages)
    [Layer.loadProvinceImage](f_Layer_loadProvinceImage)
    [Layer.setMainPixel](f_Layer_setMainPixel)
    [Layer.setMaskPixel](f_Layer_setMaskPixel)
    [Layer.setProvincePixel](f_Layer_setProvincePixel)
    [Layer.piledCopy](f_Layer_piledCopy)
    [Layer.adjustGamma](f_Layer_adjustGamma)(常にアルファチャンネルは保護されます)
    [Layer.doGrayScale](f_Layer_doGrayScale)(常にアルファチャンネルは保護されます)
    [Layer.flipLR](f_Layer_flipLR)
    [Layer.flipUD](f_Layer_flipUD)
    [Layer.assignImages](f_Layer_assignImages)

    　以下のメソッドはこのプロパティの影響を受けます。
    [Layer.copyRect](f_Layer_copyRect)
    [Layer.stretchCopy](f_Layer_stretchCopy)
    [Layer.affineCopy](f_Layer_affineCopy)
    [Layer.fillRect](f_Layer_fillRect)
    [Layer.colorRect](f_Layer_colorRect)
    [Layer.drawText](f_Layer_drawText)
    [Layer.pileRect](f_Layer_pileRect)
    [Layer.blendRect](f_Layer_blendRect)
    [Layer.operateRect](f_Layer_operateRect)
    [Layer.stretchPile](f_Layer_stretchPile)
    [Layer.stretchBlend](f_Layer_stretchBlend)
    [Layer.operateStretch](f_Layer_operateStretch)
    [Layer.affinePile](f_Layer_affinePile)
    [Layer.affineBlend](f_Layer_affineBlend)
    [Layer.operateAffine](f_Layer_operateAffine)