# Layer.holdAlpha

機能/意味
:   アルファチャンネルを保護するか

タイプ
:   [Layerクラス](class_Layer)のプロパティ

説明
:   描画においてアルファチャンネルを保護するかどうかを指定します。
    値を設定することもできます。デフォルトでは偽です。
    いくつかの描画演算では、Layer.face プロパティが dfOpaque のとき、画像のアルファチャンネル(マスク画像)を保持するかどうかをこのプロパティで指定できます。
    多くのメソッドでは、このプロパティを偽にした方が高速な描画が可能です。
    Layer.type が ltAlpha でも ltAddAlpha でも無い場合は、画像のアルファチャンネルは使用されないので、このプロパティを偽に設定しても問題有りません。
    ただし、このプロパティが偽だとアルファチャンネルは破壊されます。
    以下のメソッドはこのプロパティの影響を受けません。

    * Layer.loadImages
    * Layer.loadProvinceImage
    * Layer.setMainPixel
    * Layer.setMaskPixel
    * Layer.setProvincePixel
    * Layer.piledCopy
    * Layer.adjustGamma(常にアルファチャンネルは保護されます)
    * Layer.doGrayScale(常にアルファチャンネルは保護されます)
    * Layer.flipLR
    * Layer.flipUD
    * Layer.assignImages

    以下のメソッドはこのプロパティの影響を受けます。

    * Layer.copyRect
    * Layer.stretchCopy
    * Layer.affineCopy
    * Layer.fillRect
    * Layer.colorRect
    * Layer.drawText
    * Layer.operateRect
    * Layer.operateStretch
    * Layer.operateAffine