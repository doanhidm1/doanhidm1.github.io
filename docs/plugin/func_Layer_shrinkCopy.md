# Layer.shrinkCopy

機能/意味
:   縮小コピー

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   shrinkCopy(dleft, dtop, dwidth, dheight, src, sleft, stop, swidth, sheight)

引数
:   |  |  |
    | --- | --- |
    | dleft | コピー先の矩形の左端。小数点指定可。 |
    | dtop | コピー先の矩形の上端。小数点指定可。 |
    | dwidth | コピー先の矩形の横幅。小数点指定可。 |
    | dheight | コピー先の矩形の縦幅。小数点指定可。 |
    | src | コピー元レイヤ |
    | sleft | コピー元の矩形の左端。ピクセル単位。小数点指定不可。 |
    | stop | コピー元の矩形の上端。ピクセル単位。小数点指定不可。 |
    | swidth | コピー元の矩形の横幅。ピクセル単位。小数点指定不可。 |
    | sheight | コピー元の矩形の縦幅。ピクセル単位。小数点指定不可。 |

戻り値
:   なし (void)

説明
:   拡大される（dwidth > swidth || dheight > sheight）場合はエラー。
    縮小アルゴリズムは面積平均法。1/2以下の縮小で affineCopyより高品質。
    stretchCopyと違い Layer.face, holdAlpha は無視。

    ※透明と不透明の境目の部分で偽色（完全透明部分の裏にある色）が出ることがあるので
    あらかじめ layerExSave.dll の Layer.oozeColor() などを使っておくことを推奨