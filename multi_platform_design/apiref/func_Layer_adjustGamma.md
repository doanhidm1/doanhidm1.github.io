# Layer.adjustGamma

機能/意味
:   ガンマ補正

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   adjustGamma(rgamma=1, rfloor=0, rceil=255, ggamma=1, gfloor=0, gceil=255, bgamma=1, bfloor=0, bceil=255)

引数
:   |  |  |
    | --- | --- |
    | rgamma | 赤成分のガンマ値 ( 0.0 ～ 1.0 ～ 9.0 ) を指定します。 |
    | rfloor | 赤成分の出力最低値 ( 0 ～ 255 ) を指定します。 |
    | rceil | 赤成分の出力最大値 ( 0 ～ 255 ) を指定します。 |
    | ggamma | 緑成分のガンマ値 ( 0.0 ～ 1.0 ～ 9.0 ) を指定します。 |
    | gfloor | 緑成分の出力最低値 ( 0 ～ 255 ) を指定します。 |
    | gceil | 緑成分の出力最大値 ( 0 ～ 255 ) を指定します。 |
    | bgamma | 青成分のガンマ値 ( 0.0 ～ 1.0 ～ 9.0 ) を指定します。 |
    | bfloor | 青成分の出力最低値 ( 0 ～ 255 ) を指定します。 |
    | bceil | 青成分の出力最大値 ( 0 ～ 255 ) を指定します。 |

戻り値
:   なし (void)

説明
:   画像に対してガンマ補正を実行します。
    ガンマ値には 1.0 を指定するとガンマ曲線が直線になります。
    出力最低値と出力最高値は各成分の輝度の最低値と最高値を指定するものです。
    最高値に最低値よりも低い値を設定すると画像を反転させることができます。
    このメソッドはLayer.faceプロパティを参照します。
    これが dfAddAlpha の場合、このメソッドは加算アルファ合成用の特別なガンマ補正ルーチンを用います。
    このルーチンは加算アルファ合成のうち、アルファ合成に相当する成分に対してはガンマ補正を行いますが、加算合成に相当する成分に対してはガンマ補正を行いません。