# Layer.face

機能/意味
:   描画方式

タイプ
:   [Layerクラス](class_Layer)のプロパティ

説明
:   レイヤへの描画方式を表します。
    値を設定することもできます。

    * dfAlpha または dfBoth を指定すると、画像はアルファチャンネルつき画像と見なされ、描画されます。dfBoth でも dfAlpha でも同じになります。この描画方法に対応するレイヤタイプは ltTransparent または ltAlpha です。
    * dfAddAlpha を指定すると、画像は加算アルファチャンネルつき画像として見なされ、描画されます。この描画方法に対応するレイヤタイプは ltAddAlpha です。
    * dfOpaque または dfMain を指定すると、レイヤの画像はすべて完全不透明であると見なされ、描画されます。この描画方法に対応するレイヤタイプは ltOpaque または ltCoverRect、または ltAdditive のような算術/論理演算を行うレイヤタイプです。
    * dfMask を指定すると、マスク画像(アルファチャンネル)を描画の対象にします。
    * dfProvince を指定すると、領域画像を描画の対象にします。
    * dfAuto を指定すると、現在の Layer.type プロパティに従って描画方式が自動的に決定されます。

    作成された直後のレイヤの描画方式は dfAuto です。
    このプロパティの値によっては操作できないメソッドがあります。

参照
:   [Layer.type](prop_Layer_type)