# ImageFunction.colorRect

機能/意味
:   矩形半透明塗りつぶし

タイプ
:   [ImageFunctionクラス](class_ImageFunction)のメソッド

構文
:   colorRect(bmp, value, opa=255, rect=null, face=dfAlpha, cliprect=null)

引数
:   |  |  |
    | --- | --- |
    | bmp | 塗り潰す Bitmap オブジェクトを指定します。 |
    | value | 塗りつぶす色や値を指定します。  この値は、face 引数の値によって意味が変わります。   * dfAlpha : 0xRRGGBB 形式で色を指定してください * dfAddAlpha : 0xRRGGBB 形式で色を指定してください * dfOpaque : 0xRRGGBB 形式で色を指定してください * dfMask : マスク(不透明度)の値 ( 0 ～ 255 ) を指定してください   dfOpaque を指定した場合は、マスク情報は無視されます。  また、dfMask を指定した場合は、色の情報はそのままになります。  dfAlpha の場合でかつ opa が負の場合はこの引数は無視されます。 |
    | opa | 塗りつぶす不透明度 ( -255 ～ 0 ～ 255 ) を指定します。  この引数は、face の値が dfMask や dfProvince の場合は無視されます ( 常に完全不透明 )。  負の数の指定は face が dfAlpha の場合のみに有効で、この場合は value 引数は無視され、画像から不透明度が取り除かれます (-255 を指定すると矩形は完全に透明になります )。 |
    | rect | 塗りつぶす矩形を ( 画像位置における ) ピクセル単位で Rect オブジェクトで指定します。  未指定の場合全体が対象となります。 |
    | face | 描画方式を指定します。   * dfAlpha が指定された場合は画像はアルファチャンネルつき画像と見なされ、描画されます。 * dfAddAlpha が指定された場合は画像は加算アルファチャンネルつき画像として見なされ、描画されます。 * dfOpaque が指定された場合は画像はすべて完全不透明であると見なされ、描画されます。 |
    | cliprect | クリッピング領域を ( Bitmap の画像位置における ) Rect オブジェクトで指定します。  未指定時全体が対象となります。 |

戻り値
:   なし (void)

説明
:   指定された Bitmap 画像の矩形を指定された方法で塗りつぶします。
    ImageFunction.fillRect と異なり、透明度を指定して半透明で塗りつぶすことができます。