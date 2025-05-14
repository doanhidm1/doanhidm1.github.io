# Appearance.addBrush

機能/意味
:   ブラシの追加

タイプ
:   [Appearanceクラス](class_Appearance)のメソッド

構文
:   addBrush(colorOrBrush, ox, oy)

引数
:   |  |  |
    | --- | --- |
    | colorOrBrush | ARGB色指定またはブラシ情報（辞書） |
    | ox | 表示オフセットX |
    | oy | 表示オフセットY |

戻り値
:   なし (void)

説明
:   ブラシ情報定義
    基本 点指定は [x,y] の配列または %[x:x, y:y] の辞書
    矩形指定は [x,y,width,height] の配列または %[x:x, y:y, width:w, height:h] の辞書
    色指定は ARGB 32bit整数値
    パラメータについては GDI+ のドキュメントを見て研究してください

    type: ブラシ種別 BrushType で指定

    BrushTypeSolidColor の場合 ※直接ARGBで色指定した場合と同じです
    color: 色指定(未指定時は白)

    BrushTypeHatchFill の場合
    hatchStyle: ハッチの種類(未指定時は HatchStyleHorizontal)
    foreColor: 前景色(未指定時は白)
    backColor: 背景色(未指定時は黒)

    BrushTypeTextureFill の場合
    image: 画像指定
    wrapMode: 繰り返しパターン指定(未指定時は WrapModeTile)
    dstRect: テクスチャ領域矩形指定(未指定時は画像全部)

    BrushTypePathGradient の場合
    points: 点指定の配列
    centerColor: 中心色
    centerPoint: 中心点
    focusScale: focus scales指定 [xScale,yScale] または %[xScale:, yScale:]
    surroundColors: 周囲色指定。色の配列
    ---- 以下は BrushTypeLinearGradientでも共通
    blend: ブレンドファクター指定。数値配列で [blendFactors, blendPositions] または辞書
    blendBellShape: ブレンド形状指定(bell形状) [focus, scale]
    blendTriangularShape: ブレンド形状指定(三角形状) [focus, scale]
    gammaCorrection: ガンマ補正を有効にするかどうか true/false
    interpolationColors: [presetColors(色配列), blendPositions(数値配列)]

    BrushTypeLinearGradient の場合
    共通
    color1: 開始色指定
    color2: 終了色指定
    wrapMode: 繰り返しパターン指定(未指定時は WrapModeTile)
    ポイント指定
    point1: 開始点
    point2: 終了点
    ※角度は自動で決まる模様
    矩形指定
    rect: ポイント指定。左上が開始、右下が終了
    angle: 角度指定 (rect指定の場合だけ有効)
    isAngleScalable (角度指定がスケーラブルかどうか)
    mode: モード指定(省略時は LinearGradientModeHorizontal) angle 指定が無い場合に有効