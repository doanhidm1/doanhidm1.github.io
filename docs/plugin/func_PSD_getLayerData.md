# PSD.getLayerData

機能/意味
:   レイヤデータの読み出し

タイプ
:   [PSDクラス](class_PSD)のメソッド

構文
:   getLayerData(layer, no)

引数
:   |  |  |
    | --- | --- |
    | layer | 読み出し先レイヤ |
    | no | レイヤ番号 layer\_type が layer\_type\_normal の場合のみ読み込みできます データ内容のほか以下のプロパティが自動的にレイヤに設定されます left 左座標 top 上座標 width 横幅 height 縦幅 type 合成モード opacity 不透明度 visible 表示状態 imageLeft 0になります imageTop 0になります imageWidth width になります imageHeight height になります name name が設定されます |

戻り値
:   なし (void)

説明