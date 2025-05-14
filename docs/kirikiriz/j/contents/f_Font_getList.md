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
    | flags | フォントをどのように列挙するかを指定します。  　次の値のビット論理和による組み合わせ指定します。  fsfFixedPitch  : 固定ピッチフォントのみ列挙します  fsfSameCharSet  : 同じキャラクタセットのフォントのみ列挙します  fsfNoVertical  : 縦書き用フォントを列挙しません  fsfTrueTypeOnly  : TrueType フォントのみ列挙します  fsfIgnoreSymbol  : シンボルキャラセットを除外します  　fsfSameCharSet を指定した場合は、現在選択されているフォントと同じキャラクタセットの フォントが列挙されます。 |

戻り値
:   フォント名(文字列)が各要素として格納されている配列

説明
:   フォント名を列挙し、配列として返します。