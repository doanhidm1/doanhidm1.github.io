# Layer.piledCopy

機能/意味
:   レイヤを重ね合わせた画像をコピー

タイプ
:   [Layerクラス](f_Layer)のメソッド

構文
:   piledCopy(dleft, dtop, src, sleft, stop, swidth, sheight)

引数
:   |  |  |
    | --- | --- |
    | dleft | コピー先の矩形の左端位置を ( コピー先レイヤの画像位置における ) ピクセル単位で指定します。 |
    | dtop | コピー先の矩形の上端位置を ( コピー先レイヤの画像位置における ) ピクセル単位で指定します。 |
    | src | コピー元のレイヤオブジェクトを指定します。 |
    | sleft | コピーする矩形の左端位置を ( コピー元レイヤの表示位置における ) ピクセル単位で指定します。 |
    | stop | コピーする矩形の上端位置を ( コピー元レイヤの表示位置における ) ピクセル単位で指定します。 |
    | swidth | コピーする矩形の横幅を ( コピー元レイヤの表示位置における ) ピクセル単位で指定します。 |
    | sheight | コピーする矩形の縦幅を ( コピー元レイヤの表示位置における ) ピクセル単位で指定します。 |

戻り値
:   なし (void)

説明
:   指定されたコピー元レイヤの指定された矩形部分を、子レイヤも含めて重ね合わせ、その
    結果の画像を、自分のレイヤの指定位置にコピーします。
    　このメソッドは、コピー元レイヤやコピー先レイヤの [Layer.face](f_Layer_face) プロパティには
    影響されません。