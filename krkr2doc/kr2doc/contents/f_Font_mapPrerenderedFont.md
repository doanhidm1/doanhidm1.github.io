# Font.mapPrerenderedFont

機能/意味
:   レンダリング済みフォントの割り当て

タイプ
:   [Fontクラス](f_Font)のメソッド

構文
:   mapPrerenderedFont(fontstorage)

引数
:   |  |  |
    | --- | --- |
    | fontstorage | レンダリング済みフォントストレージを指定します。 |

戻り値
:   なし (void)

説明
:   現在選択されているフォント名に対してレンダリング済みフォントの割り当てを行います。
    　以降、同じ設定のフォントに対しては指定されたレンダリング済みフォントが代わりに使われます。
    　すべてのレイヤに対して設定が有効になります。

参照
:   [Font.unmapPrerenderedFont](f_Font_unmapPrerenderedFont)