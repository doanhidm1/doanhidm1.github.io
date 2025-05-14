# String.substring

機能/意味
:   文字列の部分文字列を返します

タイプ
:   [Stringクラス](class_String)のメソッド

構文
:   substring(offset:int, count:int=void) :string

引数
:   |  |  |
    | --- | --- |
    | offset | 開始文字位置 |
    | count | 文字数、省略可能。 |

戻り値
:   部分文字列

説明
:   文字列の、offsetからcountの部分文字列を返します。
    元の文字列に影響は与えません。
    countを省略すると、offset以降の文字列がすべて返されます。
    JavaScript の同メソッドとは引数の意味が違うので注意してください。