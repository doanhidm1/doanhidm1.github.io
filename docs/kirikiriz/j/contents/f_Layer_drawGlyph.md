# Layer.drawGlyph

機能/意味
:   文字描画

タイプ
:   [Layerクラス](f_Layer)のメソッド

構文
:   drawGlyph(x, y, glyph, color, opa=255, aa=true, shadowlevel=0, shadowcolor=0x000000, shadowwidth=0, shadowofsx=0, shadowofsy=0)

引数
:   |  |  |
    | --- | --- |
    | x | 文字描画を開始する原点の ( 画像位置における ) x 座標をピクセル単位で指定します。 |
    | y | 文字描画を開始する原点の ( 画像位置における ) y 座標をピクセル単位で指定します。 |
    | glyph | 描画するグリフを指定します。 |
    | color | 描画する文字の色を 0xRRGGBB 形式で指定します。 |
    | opa | 描画する文字の不透明度 ( -255 ～ 0 ～ 255 ) を指定します。  　負の数の指定は face が dfAlpha の場合のみに有効で、 この場合は文字の形に不透明度が取り除かれる事になります ( 値が小さいほど 効果が大きくなります )。 |
    | aa | アンチエイリアスを行うかどうかを指定します。  　真を指定するとアンチエイリアスが行われます。偽を指定すると行われません。 |
    | shadowlevel | 影の不透明度を指定します。shadowwidth 引数の値によって適切な値は変動します。  0 を指定すると影は描画されません。 |
    | shadowcolor | 影の色を 0xRRGGBB 形式で指定します。 |
    | shadowwidth | 影の幅 ( ぼけ ) を指定します。 0 がもっともシャープ ( ぼけない ) で、値を大きく すると影をぼかすことができます。 |
    | shadowofsx | 影の位置の x 座標の値をピクセル単位で指定します。 0 を指定すると影は真下に描画されます。 |
    | shadowofsy | 影の位置の y 座標の値をピクセル単位で指定します。 0 を指定すると影は真下に描画されます。 |

戻り値
:   なし (void)

説明
:   レイヤ にグリフを描画します。
    　グリフは、glyph : Array[9] = [ width, height, originx, originy, incx, incy, inc, bitmap(Octet), colors ] の様な形式の配列を指定します。
    　グリフの colors が省略された場合は、256階調であると判断されます。