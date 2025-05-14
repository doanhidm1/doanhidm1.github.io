# Appearance.addPen

機能/意味
:   ペンの追加

タイプ
:   [Appearanceクラス](class_Appearance)のメソッド

構文
:   addPen(colorOrBrush, widthOrOption, ox, oy)

引数
:   |  |  |
    | --- | --- |
    | colorOrBrush | ARGB色指定またはブラシ情報（辞書） |
    | widthOrOption | ペン幅またはペン情報（辞書） |
    | ox | 表示オフセットX |
    | oy | 表示オフセットY |

戻り値
:   なし (void)

説明
:   ペン情報定義: widthOrOption が辞書の場合は詳細情報定義になります
    パラメータについては GDI+ のドキュメントを見て研究してください

    width: ペン幅指定
    alignment: アラインメント：省略時は PenAlignmentCenter
    compoundArray: compound array 指定。数値配列
    dashCap: ダッシュの cap style の指定。省略時は DashCapFlat
    dashOffset: ダッシュのオフセット指定。省略時は0
    dashStyle: ダッシュスタイル。配列にするとユーザ定義(数値配列)。デフォルトは DasyStyleSolid
    startCap: 開始位置の cap style の指定。省略時は LineCapFlat，辞書時はAdjustableArrowCap
    endCap: 終了位置の cap style の指定。省略時は LineCapFlat，辞書時はAdjustableArrowCap
    lineJoin: 結合形状指定。 省略時は LineJoinMiter
    miterLimit: miter limit 指定（数値)

    AdjustableArrowCap：LineCapArrowAnchorでは不満なあなたに
    width(矢印幅), height(矢印高さ), filled(trueなら三角形，falseなら三又) が指定が可能