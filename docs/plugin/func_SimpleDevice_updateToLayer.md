# SimpleDevice.updateToLayer

機能/意味
:   レイヤに対して現在の状態を描画する。 バックバッファから、指定されたレイヤの描画領域に対して拡縮コピーされます。 ※レイヤのクリッピング領域は無視されます。

タイプ
:   [SimpleDeviceクラス](class_SimpleDevice)のメソッド

構文
:   updateToLayer(layer, sleft, stop, swidth, sheight)

引数
:   |  |  |
    | --- | --- |
    | layer | 描画先レイヤ |
    | sleft | ソース領域の左上座標X ※以下を省略した場合は全領域 |
    | stop | ソース領域の左上座標X |
    | swidth | ソース領域の横幅 |
    | sheight | ソース領域の縦幅 |

戻り値
:   なし (void)

説明