# Layer.operateRect

機能/意味
:   矩形演算合成

タイプ
:   [Layerクラス](f_Layer)のメソッド

構文
:   operateRect(dleft, dtop, src, sleft, stop, swidth, sheight, mode=omAuto, opa=255)

引数
:   |  |  |
    | --- | --- |
    | dleft | 演算先の矩形の左端位置を ( 演算先レイヤの画像位置における ) ピクセル単位で指定します。 |
    | dtop | 演算先の矩形の上端位置を ( 演算先レイヤの画像位置における ) ピクセル単位で指定します。 |
    | src | 演算元のレイヤオブジェクトを指定します。 |
    | sleft | 演算する矩形の左端位置を ( 演算元レイヤの画像位置における ) ピクセル単位で指定します。 |
    | stop | 演算する矩形の上端位置を ( 演算元レイヤの画像位置における ) ピクセル単位で指定します。 |
    | swidth | 演算する矩形の横幅を ( 演算元レイヤの画像位置における ) ピクセル単位で指定します。 |
    | sheight | 演算する矩形の縦幅を ( 演算元レイヤの画像位置における ) ピクセル単位で指定します。 |
    | mode | 演算のモードを指定します。  omAuto が指定された場合は演算元レイヤの[Layer.type](f_Layer_type)プロパティに従って演算の種類が自動的に決定されます。  omPsNormal が指定された場合はPhotoshop互換のアルファ合成が行われます。  omPsAdditive が指定された場合はPhotoshop互換の覆い焼き(リニア)合成が行われます。  omPsSubtractive が指定された場合はPhotoshop互換の焼き込み(リニア)合成が行われます。  omPsMultiplicative が指定された場合はPhotoshop互換の乗算合成が行われます。  omPsScreen が指定された場合はPhotoshop互換のスクリーン合成が行われます。  omPsOverlay が指定された場合はPhotoshop互換のオーバーレイ合成が行われます。  omPsHardLight が指定された場合はPhotoshop互換のハードライト合成が行われます。  omPsSoftLight が指定された場合はPhotoshop互換のソフトライト合成が行われます。  omPsColorDodge が指定された場合はPhotoshop互換の覆い焼きカラー合成が行われます。  omPsColorDodge5 が指定された場合はPhotoshopのバージョン5.x 以下と互換の覆い焼きカラー合成が行われます。  omPsColorBurn が指定された場合はPhotoshop互換の焼き込みカラー合成が行われます。  omPsLighten が指定された場合はPhotoshop互換の比較(明)合成が行われます。  omPsDarken が指定された場合はPhotoshop互換の比較(暗)合成が行われます。  omPsDifference が指定された場合はPhotoshop互換の差の絶対値合成が行われます。  omPsDifference5 が指定された場合はPhotoshopのバージョン 5.x 以下と互換の差の絶対値合成が行われます。  omPsExclusion が指定された場合はPhotoshop互換の除外合成が行われます。  omAdditive が指定された場合は加算合成が行われます。  omSubtractive が指定された場合は減算合成が行われます。  omMultiplicative が指定された場合は乗算合成が行われます。  omDodge が指定された場合は覆い焼き合成が行われます。  omDarken が指定された場合は比較(暗)合成が行われます。  omLighten が指定された場合は比較(明)合成が行われます。  omScreen が指定された場合はスクリーン乗算合成が行われます。  omAlpha が指定された場合はアルファ合成が行われます。  omAddAlpha が指定された場合は加算アルファ合成が行われます。  omOpaque が指定された場合は src のアルファ情報は無視され、src は常に完全不透明であると見なされます。 |
    | opa | 演算の強度 ( 0 ～ 255 ) を指定します。 |

戻り値
:   なし (void)

説明
:   指定された演算元レイヤの矩形部分を自分のレイヤの指定位置に指定のモードで演算合成します。
    　演算先の ( メソッドを実行する ) レイヤや演算元のレイヤの [Layer.face](f_Layer_face) プロパティの値
    は無視されます。
    　mode に omAuto を指定した場合は、演算元レイヤの[Layer.type](f_Layer_type)プロパティに従って演算の種類が自動的に決定されます。