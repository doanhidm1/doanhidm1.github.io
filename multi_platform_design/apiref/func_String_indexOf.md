# String.indexOf

機能/意味
:   部分文字列の位置を返します

タイプ
:   [Stringクラス](class_String)のメソッド

構文
:   indexOf(text:string, offset:int=void) :int

引数
:   |  |  |
    | --- | --- |
    | text | 部分文字列 |
    | offset | 検索開始位置 |

戻り値
:   0 が返されれば文字列の先頭です、-1 が返されたときは見つからなかったときです。

説明
:   文字列から、textをoffsetから検索し、最初に見つかった位置を返します。
    offsetを省略すると、文字列の先頭からの検索になります。