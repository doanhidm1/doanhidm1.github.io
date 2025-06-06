# Dictionary.forEach

機能/意味
:   引数の関数を、引数の辞書配列の各要素に対して実行します。

タイプ
:   [Dictionaryクラス](class_Dictionary)のメソッド

構文
:   forEach(target:Dictionary, func, args) :variant

引数
:   |  |  |
    | --- | --- |
    | target | 辞書配列 |
    | func | 文字列の場合は配列要素のそのメソッドを、関数の場合は function( value, key, args\* ) の形で呼び出されます。 |
    | args | 呼び出す関数に渡す引数を任意の数指定します。なくても構いません。 |

戻り値
:   呼び出した関数が返した値

説明
:   辞書配列の各要素に対して1回ずつ指定された関数を呼び出します。
    無名関数などコンテキストが null の場合は辞書配列のコンテキストで呼び出されます。
    関数が値を返すと処理が中断され、その値をこの関数の返り値にします。
    関数を文字列で呼び出した時は値を返しても中断せず、全配列要素のメソッドが呼び出されます。