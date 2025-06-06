# RegExp.replace

機能/意味
:   文字列の置き換えを行い、置き換えが行われた後の文字列を返します

タイプ
:   [RegExpクラス](class_RegExp)のメソッド

構文
:   replace(text:string, replace:string) :string

引数
:   |  |  |
    | --- | --- |
    | text | 対象文字列 |
    | replace | 置き換え文字列 |

戻り値
:   対象文字列に対してマッチングを行い、マッチした部分を置き換え文字列で置き換え、置き換えが行われた後の文字列を返します。

説明
:   置き換え文字列として、文字列ではなく関数を渡すと、置き換え動作のためにその関数が呼ばれるようになります。
    関数は引数をひとつとり、対象文字列の中のマッチした部分をあらわす配列オブジェクトが渡されます ( この配列については exec メソッドを参照してください )。
    対象文字列中のマッチした部分は、関数の戻した文字列に置き換わります。
    このメソッドは start プロパティを無視します。