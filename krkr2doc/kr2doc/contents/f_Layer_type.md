# Layer.type

機能/意味
:   レイヤ表示タイプ

タイプ
:   [Layerクラス](f_Layer)のプロパティ (読み書き可能)

説明
:   レイヤの表示タイプを表します。値を設定することもできます。

    * ltOpaque または ltCoverRect を指定すると、ピクセルごとのアルファブレンドが無効になります。ltCoverRectもltOpaqueも同じ意味です。
      [Layer.opacity](f_Layer_opacity) プロパティが 255 の場合は、完全に不透明の矩形として表示される
      事になります。マスク画像は無視されます。このタイプに適した描画方式([Layer.face](f_Layer_face)で指定)はdfOpaqueです。
    * ltAlpha または ltTransparent を指定すると、ピクセルごとのアルファブレンドが有効になります。ltTransparentもltAlphaも同じ意味です。
      マスク画像が透過に用いられます。このタイプに適した描画方式はdfAlphaです。
    * ltAddAlpha を指定すると、ピクセルごとの加算アルファブレンドが有効になります。このタイプに適した描画方式は dfAddAlpha です。
    * ltAdditive を指定すると、加算合成が行われます。マスク画像は無視されます。このタイプに適した描画方式は dfOpaque です。
    * ltSubtractive を指定すると、減算合成が行われます。マスク画像は無視されます。このタイプに適した描画方式は dfOpaque です。
    * ltMultiplicative を指定すると、乗算合成が行われます。マスク画像は無視されます。このタイプに適した描画方式は dfOpaque です。
    * ltDodge を指定すると、覆い焼き合成が行われます。マスク画像は無視されます。このタイプに適した描画方式は dfOpaque です。
    * ltDarken を指定すると、比較(暗)合成が行われます。マスク画像は無視されます。このタイプに適した描画方式は dfOpaque です。
    * ltLighten を指定すると、比較(明)合成が行われます。マスク画像は無視されます。このタイプに適した描画方式は dfOpaque です。
    * ltScreen を指定すると、スクリーン乗算合成が行われます。マスク画像は無視されます。このタイプに適した描画方式は dfOpaque です。

    　この他のレイヤ表示タイプについては[グラフィックシステム](GraphicSystem)を参照してください。

参照
:   [Layer.face](f_Layer_face)