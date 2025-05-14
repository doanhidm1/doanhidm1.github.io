# Layer.copyExposure

機能/意味
:   総和バッファから画像作成

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   copyExposure(stat)

引数
:   |  |  |
    | --- | --- |
    | stat | : 足きり用の情報辞書／voidの場合は暗黙でstatExposureを実行してその値を使用する 各要素の min～max が 0～255 の画像として自分自身が書き換わる 各要素において min >= maxの場合は常に0xFFで返される |

戻り値
:   なし (void)

説明