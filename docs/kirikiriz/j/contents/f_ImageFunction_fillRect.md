# ImageFunction.fillRect

機能/意味
:   矩形塗りつぶし

タイプ
:   [ImageFunctionクラス](f_ImageFunction)のメソッド

構文
:   fillRect(bmp, value, rect=null, isalpha=true, cliprect=null)

引数
:   |  |  |
    | --- | --- |
    | bmp | 塗り潰す Bitmap オブジェクトを指定します。 |
    | value | 塗りつぶす色や値を指定します。  　この値は、isalpha の値によって意味が変わります。  true  : 0xAARRGGBB 形式で不透明度と色を指定してください。メインとマスクの両方が塗りつぶされます。  false  : 0xRRGGBB 形式で色を指定してください。 |
    | rect | 塗りつぶす矩形を ( 画像位置における ) ピクセル単位で Rect オブジェクトで指定します。  　未指定の場合全体が対象となります。 |
    | isalpha | アルファチャンネルを持つかどうかを指定します。 |
    | cliprect | クリッピング領域を ( Bitmap の画像位置における ) Rect オブジェクトで指定します。  　未指定時全体が対象となります。 |

戻り値
:   なし (void)

説明
:   指定された Bitmap 画像の矩形を指定された方法で塗りつぶします。