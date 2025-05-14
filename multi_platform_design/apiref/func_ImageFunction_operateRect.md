# ImageFunction.operateRect

機能/意味
:   矩形演算合成

タイプ
:   [ImageFunctionクラス](class_ImageFunction)のメソッド

構文
:   operateRect(dst, dleft, dtop, src, srcrect=null, cliprect=null, mode=omAuto, face=dfAlpha, opa=255, hda=false)

引数
:   |  |  |
    | --- | --- |
    | dst | 重ね合わせ先の Bitmap オブジェクトを指定します。 |
    | dleft | 演算先の矩形の左端位置を ( 演算先 Bitmap の画像位置における ) ピクセル単位で指定します。 |
    | dtop | 演算先の矩形の上端位置を ( 演算先 Bitmap の画像位置における ) ピクセル単位で指定します。 |
    | src | 演算元の Bitmap オブジェクトを指定します。未指定時全体が対象になります。 |
    | srcrect | 演算する矩形を ( 演算元 Bitmap の画像位置における ) ピクセル単位で Rect オブジェクトで指定します。  未指定時全体が対象になります。 |
    | cliprect | クリッピング矩形を ( 重ね合わせ先 Bitmap の画像位置における ) Rect オブジェクトで指定します。  未指定時クリッピングは行われません。 |
    | mode | 演算のモードを指定します。   * omPsNormal が指定された場合はPhotoshop互換のアルファ合成が行われます。 * omPsAdditive が指定された場合はPhotoshop互換の覆い焼き(リニア)合成が行われます。 * omPsSubtractive が指定された場合はPhotoshop互換の焼き込み(リニア)合成が行われます。 * omPsMultiplicative が指定された場合はPhotoshop互換の乗算合成が行われます。 * omPsScreen が指定された場合はPhotoshop互換のスクリーン合成が行われます。 * omPsOverlay が指定された場合はPhotoshop互換のオーバーレイ合成が行われます。 * omPsHardLight が指定された場合はPhotoshop互換のハードライト合成が行われます。 * omPsSoftLight が指定された場合はPhotoshop互換のソフトライト合成が行われます。 * omPsColorDodge が指定された場合はPhotoshop互換の覆い焼きカラー合成が行われます。 * omPsColorDodge5 が指定された場合はPhotoshopのバージョン5.x 以下と互換の覆い焼きカラー合成が行われます。 * omPsColorBurn が指定された場合はPhotoshop互換の焼き込みカラー合成が行われます。 * omPsLighten が指定された場合はPhotoshop互換の比較(明)合成が行われます。 * omPsDarken が指定された場合はPhotoshop互換の比較(暗)合成が行われます。 * omPsDifference が指定された場合はPhotoshop互換の差の絶対値合成が行われます。 * omPsDifference5 が指定された場合はPhotoshopのバージョン 5.x 以下と互換の差の絶対値合成が行われます。 * omPsExclusion が指定された場合はPhotoshop互換の除外合成が行われます。 * omAdditive が指定された場合は加算合成が行われます。 * omSubtractive が指定された場合は減算合成が行われます。 * omMultiplicative が指定された場合は乗算合成が行われます。 * omDodge が指定された場合は覆い焼き合成が行われます。 * omDarken が指定された場合は比較(暗)合成が行われます。 * omLighten が指定された場合は比較(明)合成が行われます。 * omScreen が指定された場合はスクリーン乗算合成が行われます。 * omAlpha が指定された場合はアルファ合成が行われます。 * omAddAlpha が指定された場合は加算アルファ合成が行われます。 * omOpaque が指定された場合は src のアルファ情報は無視され、src は常に完全不透明であると見なされます。 |
    | face | 描画方式を指定します。   * dfAlpha が指定された場合は画像はアルファチャンネルつき画像と見なされ、描画されます。 * dfAddAlpha が指定された場合は画像は加算アルファチャンネルつき画像として見なされ、描画されます。 * dfOpaque が指定された場合は画像はすべて完全不透明であると見なされ、描画されます。 |
    | opa | 演算の強度 ( 0 ～ 255 ) を指定します。 |
    | hda | アルファチャンネルを保護するかどうかを指定します。 |

戻り値
:   なし (void)

説明
:   指定された演算元 Bitmap の矩形部分を演算先の Bitmap の指定位置に指定のモードで演算合成します。