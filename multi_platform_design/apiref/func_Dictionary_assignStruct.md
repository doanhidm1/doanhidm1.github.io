# Dictionary.assignStruct

機能/意味
:   辞書配列をコピーします

タイプ
:   [Dictionaryクラス](class_Dictionary)のメソッド

構文
:   assignStruct(src:Dictionary)

引数
:   |  |  |
    | --- | --- |
    | src | コピー元辞書配列 |

戻り値
:   なし (void)

説明
:   引数で指定された他の辞書配列の内容を、そっくりコピーします。
    assign メソッドと違い、メンバに配列あるいは辞書配列があった場合は、再帰的にその内容もコピーします ( assign メソッドの場合は参照がコピーされるだけです )。