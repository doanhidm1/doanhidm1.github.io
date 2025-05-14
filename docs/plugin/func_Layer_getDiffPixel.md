# Layer.getDiffPixel

機能/意味
:   レイヤのピクセル比較を行います。

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   getDiffPixel(base, samecol, diffcol)

引数
:   |  |  |
    | --- | --- |
    | base | 差分元となるベース用の画像 |
    | samecol | 同じ場合に塗りつぶす色(0xAARRGGBB)（voidまたは省略なら塗りつぶさない） |
    | diffcol | 違う場合に塗りつぶす色(0xAARRGGBB)（voidまたは省略なら塗りつぶさない） |

戻り値
:   なし (void)

説明
:   （baseはインスタンス自身と同じサイズでないと例外を投げます）