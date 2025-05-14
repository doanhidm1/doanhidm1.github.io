# PreRenderedFontImage

フォントイメージ（※このクラスは実際には存在しません！）

callbackで返すレイヤオブジェクトに付加する追加情報を定義します。
普通のレイヤオブジェクトに対して，値を代入して渡してください。
レイヤの画像は(0,0)-(blackbox\_x-1,blackbox\_y-1)の領域のα情報のみ参照され，65段階（0～64）にリサンプルされます。

callbackの返り値として同じインスタンスを何度も使いまわしても問題ありません。

# メンバ

メソッド

プロパティ
:   [blackbox\_x](prop_PreRenderedFontImage_blackbox_x) (GLYPHMETRICS.gmBlackBoxX )
    [blackbox\_y](prop_PreRenderedFontImage_blackbox_y) (GLYPHMETRICS.gmBlackBoxY )
    [inc](prop_PreRenderedFontImage_inc) (GetTextExtentPoint32 の返すサイズの SIZE.cx )
    [inc\_x](prop_PreRenderedFontImage_inc_x) (GLYPHMETRICS.gmCellIncX )
    [inc\_y](prop_PreRenderedFontImage_inc_y) (GLYPHMETRICS.gmCellIncY )
    [origin\_x](prop_PreRenderedFontImage_origin_x) (GLYPHMETRICS.gmptGlyphOrigin.x )
    [origin\_y](prop_PreRenderedFontImage_origin_y) (GLYPHMETRICS.gmptGlyphOrigin.y )