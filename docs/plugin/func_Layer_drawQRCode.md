# Layer.drawQRCode

機能/意味
:   レイヤーのサイズを調整して、指定の値(文字列又は整数値)に準じたQRコードを書き込みます

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   drawQRCode(value, ecLevel, qrVersion, autoExtent, maskPattern)

引数
:   |  |  |
    | --- | --- |
    | value | QRコードにする値(文字列又は整数値) |
    | ecLevel | 誤り訂正レベル(default:0/0(最小)～3(最大)) |
    | qrVersion | 容量サイズグループ(default:0/0～2) |
    | autoExtent | 自動拡張の有無(default:true(値に対してサイズが小さいときは適切なサイズに自動拡張)) |
    | maskPattern | マスキングパターン(default:-1(自動選択)) |

戻り値
:   なし (void)

説明