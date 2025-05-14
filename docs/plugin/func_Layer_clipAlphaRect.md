# Layer.clipAlphaRect

機能/意味
:   レイヤの Alpha CHANNEL を src の Alpha CHANNEL で乗算する

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   clipAlphaRect(dleft, dtop, src, sleft, stop, swidth, sheight, clear)

引数
:   |  |  |
    | --- | --- |
    | dleft | 左端位置 |
    | dtop | 上端位置 |
    | src | 乗算用のαを持つソース画像 |
    | sleft | ソースの左端位置 |
    | stop | ソースの上端位置 |
    | swidth | ソースの横幅 |
    | sheight | ソースの縦幅 |
    | clear | 演算範囲外領域をこの値（opacity）で塗りつぶす 省略時または0-255の値以外の場合は塗りつぶさない |

戻り値
:   なし (void)

説明