# Font

Font クラスは、フォントを管理するためのクラスです。
　[Layer](f_Layer) クラスの [Layer.font](f_Layer_font) プロパティで得られるのがこのクラスのオブジェクトですが、
ユーザがこのクラスからオブジェクトを作成することはできません ( Font というメンバ自体、ユーザが
アクセスすることができません )。

# メンバ

コンストラクタ
:   なし

メソッド
:   [doUserSelect](f_Font_doUserSelect) ( フォント選択ダイアログボックスの表示 )
    [getEscHeightX](f_Font_getEscHeightX) ( 文字の縦方向への X 座標の移動量 )
    [getEscHeightY](f_Font_getEscHeightY) ( 文字の縦方向への Y 座標の移動量 )
    [getEscWidthX](f_Font_getEscWidthX) ( 文字の横方向への X 座標の移動量 )
    [getEscWidthY](f_Font_getEscWidthY) ( 文字の横方向への Y 座標の移動量 )
    [getList](f_Font_getList) ( フォント名の列挙 )
    [getTextHeight](f_Font_getTextHeight) ( 文字列の縦幅を得る )
    [getTextWidth](f_Font_getTextWidth) ( 文字列の横幅を得る )
    [mapPrerenderedFont](f_Font_mapPrerenderedFont) ( レンダリング済みフォントの割り当て )
    [unmapPrerenderedFont](f_Font_unmapPrerenderedFont) ( レンダリング済みフォントの割り当て解除 )

プロパティ
:   [angle](f_Font_angle) ( 文字描画角度 )
    [bold](f_Font_bold) ( ボールド )
    [face](f_Font_face) ( フォント名 )
    [height](f_Font_height) ( フォント高さ )
    [italic](f_Font_italic) ( イタリック )
    [strikeout](f_Font_strikeout) ( 取消線 )
    [underline](f_Font_underline) ( アンダーライン )

イベント
:   なし