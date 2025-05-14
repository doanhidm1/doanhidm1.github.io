# Layer.drawImageAffine

機能/意味
:   画像のアフィン変換コピー

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   drawImageAffine(src, sleft, stop, swidth, sheight, affine, A, B, C, D, E, F)

引数
:   |  |  |
    | --- | --- |
    | src | コピー元画像(Image/Layer/ファイル名) |
    | sleft | 元矩形の左端 |
    | stop | 元矩形の上端 |
    | swidth | 元矩形の横幅 |
    | sheight | 元矩形の縦幅 |
    | affine | アフィンパラメータの種類(true:変換行列, false:座標指定), |

戻り値
:   更新域情報(RectF)

説明