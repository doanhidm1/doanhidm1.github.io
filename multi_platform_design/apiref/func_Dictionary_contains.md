# Dictionary.contains

機能/意味
:   辞書配列に指定された key が存在するか判定します。

タイプ
:   [Dictionaryクラス](class_Dictionary)のメソッド

構文
:   contains(target:Dictionary, key:string) :bool

引数
:   |  |  |
    | --- | --- |
    | target | 存在を確認する辞書配列 |
    | key | 存在を確認するキー |

戻り値
:   キーの有無

説明
:   辞書に指定されたkey存在する場合はtrue、しない場合はfalseを返します。
    コンテキストがある場合は target を省略できます。
    in 演算子でも判定可能です。