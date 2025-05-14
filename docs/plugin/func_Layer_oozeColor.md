# Layer.oozeColor

機能/意味
:   レイヤの淵の色を透明部分まで引き伸ばします（縮小時に偽色が出るのを防ぐ）

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   oozeColor(level, threshold, fillColor)

引数
:   |  |  |
    | --- | --- |
    | level | 処理を行う回数。大きいほど引き伸ばし領域が増える |
    | threshold | アルファの閾値(1～255)これより低いピクセルへ引き伸ばす |
    | fillColor | 処理領域以外の塗りつぶし色(0xRRGGBB) |

戻り値
:   なし (void)

説明