# Font.getList

機能/意味
:   フォント名の列挙

タイプ
:   [Fontクラス](f_Font)のメソッド

構文
:   getList(flags)

引数
:   |  |  |
    | --- | --- |
    | flags | フォントをどのように列挙するかを指定します。[Font.doUserSelect](f_Font_doUserSelect)で 指定するものと同一です (ただしこのメソッドには fsfUseFontFaceは指定しても無視されます) |

戻り値
:   フォント名(文字列)が各要素として格納されている配列

説明
:   フォント名を列挙し、配列として返します。